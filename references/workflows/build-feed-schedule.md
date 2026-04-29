# Workflow: Build Feed Schedule

Generate a custom feed schedule (per-stage EC, pH, frequency, supplements) based on the user's stored grow context. Pulls medium, nutrient_line, water source, and stage from `grow-context.md` and adapts the manufacturer's base schedule to the user's actual setup.

This workflow consumes state, applies medium-specific routing, adjusts for water input, and produces a per-stage table the user can follow with explicit adjustment triggers for when to deviate.

## When to Use

- User asks "what feed schedule should I run?"
- User has a new nutrient line and wants a starter plan
- User reports symptoms that trace to feed mismatch (over/under, lockout, EC creep)
- User entering a stage transition (veg → flower, late flower → flush/ripening)
- User running custom mix and wants validation
- Pre-flip planning ("I'm flipping in 5 days, need a flower schedule")

## Hard Rules

1. **Never ship a schedule without reading `grow-context.md` first.** Numbers depend on `medium`, `source` (water), `input_ec`, and `current_stage`.
2. **Manufacturer schedule is the START, not the answer.** Adapt for water, plant size, environment, genetics.
3. **State target ranges, never single fixed numbers.** "1.6-2.0 EC" not "1.8 EC" — environments vary.
4. **Use the user's PPM scale from `ppm_scale` field** (Sensors / Monitoring section). Never mix 500 and 700 scales in one schedule.
5. **Living soil → no EC schedule.** If `medium` field = "living soil", route to `06-nutrients-organic.md` and deliver an amendment + tea schedule, not an EC curve.
6. **Always include the ramp-up.** Plants don't go from seedling to peak EC in one feed.
7. **Account for input water EC.** Final EC at the root = `input_ec` + added nutrient EC.
8. **Cite the source schedule** (mfg or peer-reviewed) and flag where you adjusted from baseline.

## Procedure

### Pass 0 — Read state and verify completeness

Pull these fields from `grow-context.md` (exact schema names):

| Section | Field | Why needed |
|---|---|---|
| Medium & Containers | `medium`, `medium_brand`, `container_size`, `total_plant_count` | Drives feed approach + volume |
| Water Source | `source`, `input_ec`, `input_ph`, `alkalinity`, `ro_system` | Adjusts peak target + Cal-Mg need |
| Nutrient Line | `brand`, `schedule_followed`, `silica`, `cal_mg`, `beneficials`, `ph_down`, `ph_up` | Base schedule + supplements |
| Sensors / Monitoring | `ppm_scale`, `ec_meter`, `ph_meter` | Number scale + measurement trust |
| Current Feed | `feed_frequency`, `ec_in`, `ph_in`, `volume_per_pot_ml` | Current routine baseline |
| Stage Tracking | `current_stage`, `veg_started`, `flip_date` | Where in the timeline |
| Active Grow | `strain_1`, `seed_or_clone`, `photoperiod_or_auto` | Strain heaviness, auto vs photo timing |

If any required field is `[unset]` and material to the schedule:
- For `medium`, `brand`, `source`, `current_stage` → STOP, ask user to fill before generating
- For `input_ec`, `alkalinity` → ask, or assume RO defaults with caveat
- For `silica`, `cal_mg`, `beneficials` → ask if user wants them included
- For `total_plant_count`, `container_size` → ask, or compute volume per pot only

### Pass 1 — Classify medium and route

Four primary paths based on `medium` field value:

**A. SYNTHETIC IN INERT MEDIA** (`medium` = coco / coco-perlite / rockwool / DWC / RDWC / aero)
- Daily fertigation typical
- pH window: 5.5-6.3, optimal 5.8
- Cal-Mg mandatory if `source` = RO
- Tighter EC range (peak ~2.0-2.6 in flower)
- Load `06-nutrients-synthetic.md` and `04-medium-coco.md` (or `04-medium-hydro.md`)

**B. SYNTHETIC IN AMENDED SOIL** (`medium` = soil mix / FFOF / FFHF / promix-bx)
- Looser cadence (1-on-1-off, or when dry)
- pH window: 6.0-7.0, optimal 6.3-6.8
- Lower peak EC (soil buffers, ~1.4-2.0 in flower)
- Watch runoff EC creep
- Load `06-nutrients-synthetic.md` + `04-medium-soil.md`

**C. ORGANIC LIVING SOIL** (`medium` = living soil / no-till / KIS organic)
- NO pH adjustment (biology handles it)
- NO EC-based feeding
- Top-dress + compost teas + plain dechlorinated water
- Skip the EC curve format entirely
- Load `06-nutrients-organic.md` + `04-medium-living-soil.md`
- Output is amendment cadence + tea schedule

**D. BOTTLE-ORGANIC IN COCO/SOIL** (`brand` = BioBizz / BioCanna / Roots Organics)
- pH window: 5.8-6.5
- Mfg-recommended dosing (less aggressive than synthetic)
- Load `06-nutrients-organic.md`

### Pass 2 — Establish baseline from manufacturer schedule

Pull the relevant mfg schedule for `brand`. Common lines and typical peak EC ranges (coco/hydro, 500-scale PPM):

| Line | Veg peak EC | Flower peak EC | Notes |
|---|---|---|---|
| Athena Pro | 2.0-2.4 | 2.4-3.0 | Aggressive; needs Cal-Mg add for RO |
| Canna Coco A+B | 1.6-1.8 | 1.8-2.0 | Conservative; line-locked for coco |
| GH Flora Trio | 1.4-1.8 | 1.8-2.2 | Old-school 3-part; flexible |
| Jacks 321 | 1.2-1.6 | 1.6-2.0 | Cheap, simple, Cal already integrated |
| MegaCrop | 1.4-1.8 | 1.8-2.2 | One-part, mid-tier |
| Mills | 1.4-1.6 | 1.6-1.8 | Conservative, organic-leaning |
| Advanced Nutrients | 1.4-1.8 | 1.8-2.2 | pH Perfect line — pH self-adjusts (claimed) |
| House & Garden | 1.6-1.8 | 1.8-2.2 | Mid-tier Dutch line |
| BioBizz (organic) | mfg ml/L | mfg ml/L | Don't translate to EC; follow ml/L dose |

Above are coco/hydro ranges. Soil = subtract ~0.4 EC from peaks. EC values are absolute (mS/cm) — same on any meter. PPM display differs by scale: EC 1.6 = 800 ppm on 500-scale, 1120 ppm on 700-scale. If user works in ppm not EC, convert per their `ppm_scale` field.

### Pass 3 — Adjust for water input

From `input_ec`:
- Final EC at root = `input_ec` + nute-added EC
- Example: `input_ec` = 0.4, target peak = 2.0 → mix nutes to add 1.6 EC = 2.0 final
- If `input_ec` > 0.6 (hard tap, high mineral) → warn about long-term mineral accumulation; suggest RO if available

From `source` and `alkalinity`:
- `source` = RO + `medium` = coco → Cal-Mg MANDATORY
- `source` = RO + `medium` = hydro/DWC → Cal-Mg MANDATORY
- `source` = tap with `alkalinity` > 100 ppm CaCO3 → likely no separate Cal-Mg needed; Ca/Mg already present
- `source` = well → test profile; varies wildly

For `ph_down` choice:
- Phosphoric acid (H3PO4) — most common, neutral effect
- Nitric acid (HNO3) — adds N during pH down (boost in veg)
- Sulfuric acid (H2SO4) — adds S
- Citric acid — organic but unstable, only for very small adjustments

For `ph_up`:
- Potassium hydroxide (KOH) standard
- Don't use citric for pH up (doesn't work)

### Pass 4 — Generate stage-appropriate ramp curve

Default ramp for synthetic in coco, full mfg schedule, 500-scale PPM, peak 2.4 EC reference:

| `current_stage` | Week | EC range | pH | Frequency | Volume/pot (5gal) |
|---|---|---|---|---|---|
| seedling | 0 | 0.4-0.6 | 5.8 | every 3-4 days | 100-200 ml |
| seedling | 1 | 0.6-0.8 | 5.8 | when dry | 200-400 ml |
| veg-week-2 | 2 | 1.0-1.2 | 5.8 | daily small | 400-600 ml |
| veg-week-3 | 3 | 1.2-1.5 | 5.8 | daily, 10-20% runoff | 600-1000 ml |
| veg-week-4+ | 4+ | 1.5-1.8 | 5.8 | daily, sometimes 2x | 1-2 L |
| flip / preflower | 0 | 1.6-1.8 | 5.8 | daily | 1-2 L |
| flower-week-1 (stretch) | 1 | 1.8-2.0 | 5.9 | daily | 1.5-2 L |
| flower-week-2 (stretch) | 2 | 2.0-2.2 | 5.9 | daily | 1.5-2 L |
| flower-week-3 (bud) | 3 | 2.2-2.4 | 6.0 | daily, peak feed | 2-3 L |
| flower-week-4 (bud) | 4 | 2.2-2.4 | 6.0 | daily | 2-3 L |
| flower-week-5 (bud) | 5 | 2.0-2.4 | 6.0 | daily | 2-3 L |
| flower-week-6 | 6 | 1.8-2.2 | 6.0-6.1 | daily, ramping down | 2-3 L |
| flower-week-7 | 7 | 1.4-1.8 | 6.1 | daily, lighter | 1.5-2 L |
| ripening / late | 8-9 | 1.0-1.4 (or plain water) | 6.1 | reduced, optional flush 7-10 days | varies |

Adjust by:
- Strain heaviness (heavy feeders push higher; light feeders cap lower)
- `container_size` (smaller = more frequent, less concentrated)
- Environment (high VPD = more transpiration = more total water but same EC)
- Plant size (small plants need less volume, same EC)
- `photoperiod_or_auto` = auto → compress timeline; lower peaks; autos finish ~10-12 weeks total

For soil (path B) → subtract 0.4 EC from each row, run pH 6.3-6.8, frequency drops to 1-on-1-off or when dry.

For autoflowers (`photoperiod_or_auto` = auto):
- Compress total timeline to 10-12 weeks
- Cap peak EC at 1.6-1.8 (autos burn easier than photos)
- pH window same as photo
- No defined "flip" — stage transitions internally; watch pre-flowers for veg→flower marker
- Skip the flower-week-3-4 peaks above; hold cap at 1.8

For living soil (path C) → ignore the table entirely. Output instead:
- Top-dress schedule (e.g. week 4 of veg, week 2 of flower, week 5 of flower)
- Tea cadence (compost tea weekly veg, fungal tea early flower, bloom tea mid)
- Plain water between (RO or dechlorinated tap, no pH adjustment)

### Pass 5 — Add supplements per stage

Based on `silica`, `cal_mg`, `beneficials` fields:

**Silica** (if `silica` = Y or recommended):
- 0.5-1 ml/L from veg start through flower week 4
- **Add to water FIRST before any other nutes** (raises pH; pH down after Si is mixed)
- Skip if `medium` = living soil

**Beneficials** (if `beneficials` lists mycos/bacillus/trichoderma):
- Mycorrhizae: apply at transplant or first feed of new container
- Bacillus subtilis: weekly through veg, optional through flower
- Trichoderma: at transplant + monthly
- **Stop bacillus 3-4 weeks before harvest if testing for TYM panel** (commercial/legal markets) — spore counts can elevate microbial counts. For home growers, not a safety concern; can run through harvest.

**PK boost / bloom enhancer** (line-specific):
- Athena, Canna, Mills → built into base, NO additional PK boost needed
- GH Trio, MegaCrop, Jacks → can add a PK booster (Big Bud, KoolBloom, etc.) weeks 2-6 of flower at mfg dose
- Don't double-PK — toxicity locks micros

**Cal-Mg standalone** (if `cal_mg` field unset and water/medium combo demands it):
- `source` = RO + `medium` = coco/hydro → 1 ml/L throughout veg + flower
- `source` = tap, hard → likely none; test alkalinity first
- Watch leaf signals: interveinal yellowing on lower leaves (Mg) or new-growth distortion (Ca)

### Pass 6 — Format the per-stage plan

See Output Format below.

### Pass 7 — State update (only if user adopts)

Update `grow-context.md`:
- `last_updated`: today's date
- `last_updated_by`: agent
- `source_workflow`: build-feed-schedule
- `schedule_followed` (Nutrient Line section): "custom built [date]"
- `## Notes > freeform`: append "Custom schedule built [date], peak veg EC [range], peak flower EC [range], full plan in grow-log entry [date]"

Append `grow-log.md` entry:
```
## [DATE] — Schedule built ([current_stage])
Generated custom feed schedule for [strain_1] in [medium].
Source: [brand] mfg schedule, adapted for [input_ec] EC water and [container_size] containers.
Peak veg: [EC range] @ pH [range]
Peak flower: [EC range] @ pH [range]
Supplements: [list]
Adjustment triggers logged.
```

If user is just asking for a draft → no state update.

## Output Format

```
FEED SCHEDULE — [user's grow]

Setup recap (from grow-context.md):
- Medium: [medium] / [medium_brand]
- Containers: [container_size], [total_plant_count] plants
- Water: [source], input_ec [input_ec], input_ph [input_ph]
- Nutrient line: [brand] (schedule: [schedule_followed])
- Cal-Mg: [cal_mg]
- Silica: [silica]
- Beneficials: [beneficials]
- PPM scale: [ppm_scale]
- Current stage: [current_stage]

Source schedule: [mfg name + version date]
Adapted for: [list specific deltas — e.g. "RO water adds Cal-Mg requirement; 5gal containers reduce volume per feed"]

PER-STAGE PLAN (PPM scale: [500 or 700])

| Stage | Week | EC | pH | Volume/pot | Frequency | Supplements |
|---|---|---|---|---|---|---|
| seedling | 0 | 0.4-0.6 | 5.8 | 200ml | every 3 days | Cal-Mg |
| seedling | 1 | 0.6-0.8 | 5.8 | 300ml | when dry | Cal-Mg + Si |
| veg | 2 | 1.0-1.2 | 5.8 | 500ml | daily small | Cal-Mg + Si + bacillus |
| ... | ... | ... | ... | ... | ... | ... |

CONFIDENCE: [HIGH/MEDIUM/LOW]
- Reason: [explanation — fields all present? non-standard setup? assumptions made?]

ADJUSTMENT TRIGGERS — when to deviate from this plan:
- Runoff EC drifts > 0.5 above input EC → reduce input EC by 0.2 next feed
- Tip burn appears (margin yellow/brown) → drop EC 0.2, check pH
- Pale lower leaves week 4+ veg → increase EC 0.2
- Interveinal yellowing lower (Mg) → add Cal-Mg standalone
- New growth distortion (Ca) → check airflow + Cal-Mg dose
- pH at runoff drifts > 0.5 from target → flush + reset
- Stretch beyond expected → check DLI before raising EC

LOG TARGETS — record per feed:
- Date
- EC in / EC runoff
- pH in / pH runoff
- Volume per pot
- Visual plant note (1 line)

Want me to save this as your active schedule and log the first entry? [Y/N]
```

## State Updates

If user accepts:

`grow-context.md`:
- `last_updated`: [today YYYY-MM-DD]
- `last_updated_by`: agent
- `source_workflow`: build-feed-schedule
- `schedule_followed`: "custom built [date]"
- Optionally update `silica`, `cal_mg`, `beneficials` if user added them

`grow-log.md`: append schedule-built entry as shown in Pass 7.

If user is just exploring → no state update; tell them they can save later.

## Pitfalls

| Pitfall | Prevention |
|---|---|
| Generating schedule without reading `grow-context.md` | Hard Rule 1; Pass 0 always reads first |
| Mixing 500 and 700 ppm scales | Pull `ppm_scale` from Sensors / Monitoring section; lock to one scale |
| Living soil user given EC schedule | Hard Rule 5; route to organic file with amendment plan |
| Single fixed numbers ("EC 2.4") | Always ranges per Hard Rule 3 |
| Ignoring `input_ec` in peak target | Pass 3 — peak EC includes water, not just nutes |
| Cal-Mg blind add to hard tap water | Test `alkalinity` first; can over-deliver Ca and lock K |
| Carrying veg N levels into flower | Stage-appropriate ramp; reduce N at flip |
| Recommending PK boost when base already has it | Check the line — Athena/Canna/Mills have it built in |
| Schedule for autoflower same as photo | Compress timeline + lower peaks if `photoperiod_or_auto` = auto |
| Recommending tap-water schedule for RO user | Always pull `source` first; RO needs Cal-Mg + supplemental micros |
| Forgetting silica must be added FIRST | Pass 5 supplement order; Si raises pH if added to mixed feed |
| Flushing 14+ days "to improve flavor" | Debunked; finish at lighter feed, rely on cure (per `21-troubleshooting-tree.md` flush guidance) |
| Schedule built without `current_stage` | Demand stage from state or ask; can't ramp without knowing where the plant is |

## Verification

Before sending:
- [ ] `grow-context.md` was read?
- [ ] All required fields present (or asked for if missing)?
- [ ] Medium routed correctly (synthetic / soil / living / bottle-organic)?
- [ ] `ppm_scale` matched user's meter throughout?
- [ ] EC ranges, never point numbers?
- [ ] `input_ec` accounted for in peak target?
- [ ] Cal-Mg recommendation matches `source` + `medium`?
- [ ] Supplements aligned with line capabilities (no double-PK)?
- [ ] Silica add-first warning included if Si is in plan?
- [ ] Source mfg schedule cited?
- [ ] Adjustment triggers listed (when to deviate)?
- [ ] Confidence level stated?
- [ ] Log targets specified?
- [ ] State update offered (with explicit Y/N)?

If any answer is no → fix before sending.

## References

- Knowledge:
  - `06-nutrients-synthetic.md` — line-specific schedules
  - `06-nutrients-organic.md` — organic + living soil amendment cadence
  - `04-medium-coco.md`, `04-medium-soil.md`, `04-medium-hydro.md`, `04-medium-living-soil.md` — medium-specific feeding mechanics
  - `05-water-quality.md` — pH math, ppm scales, alkalinity
  - `07-deficiencies.md` — symptom triggers for adjustment
  - `12-flowering.md` — flower-stage feed transitions
  - `21-troubleshooting-tree.md` — flush guidance and EC-mismatch routing
- State (exact field names referenced):
  - `grow-context.md` → `medium`, `medium_brand`, `container_size`, `total_plant_count`, `source`, `input_ec`, `input_ph`, `alkalinity`, `ro_system`, `brand`, `schedule_followed`, `silica`, `cal_mg`, `beneficials`, `ph_down`, `ph_up`, `ppm_scale`, `feed_frequency`, `current_stage`, `strain_1`, `photoperiod_or_auto`
- Rules:
  - `SKILL.md` Rule 2 — confidence framework
  - `SKILL.md` Rule 3 — intake checklist (separate from this workflow's state read)
  - `SKILL.md` Rule 5 — source hierarchy (cite mfg + tier when adapting)
  - `SKILL.md` Rule 6 — silent state updates with end-of-session summary
