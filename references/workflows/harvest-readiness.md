# Workflow: Harvest Readiness

Determine optimal harvest timing through trichome maturity + ripening signal cross-check. Used when user asks "is it time?" or "when do I chop?". Pulls strain, flip date, and current stage from `grow-context.md`, then walks the trichome + signal protocol and outputs a confidence-gated recommendation.

This is the timing **decision gate**, not the harvest execution itself. Execution lives in `13-harvest.md`. This workflow says GO, WAIT, or STAGGER.

## When to Use

- User asks "is my plant ready?" / "when do I chop?"
- User submits a trichome macro photo
- Days in flower approaching `expected_harvest`
- User wonders about pre-harvest signals (yellowing, smell intensity, calyx swell)
- User torn between earlier (heady) vs later (sedating) chop window
- Outdoor grow with weather pressure approaching (frost, storm, mold pressure)

## Hard Rules

1. **Trichome reading is the PRIMARY signal.** Calendar days, pistils, leaf fade, calyx swell are secondary confirmation only.
2. **Require WHITE-LIGHT MACRO photos of trichomes ON CALYXES** (not sugar leaves — sugar leaf trichomes mature ahead of calyx trichomes; reading sugar leaf gives a false-early signal). Reject blurple LED photos.
3. **Multi-point sampling required.** Top cola, mid-canopy, lower buds — they mature at different rates. One-spot reads mislead.
4. **Strain timing is a guideline, NOT a deadline.** Some plants need 1-2 weeks past breeder estimate. Trichomes overrule the calendar.
5. **State the % clear / cloudy / amber breakdown explicitly** in every reading.
6. **Match recommendation to user's stated effect preference** (heady / balanced / sedating). Don't impose your default.
7. **Outdoor → factor weather forecast** (frost, storms, mold pressure) into the timing call.
8. **Never decide on a single photo.** Always rank recommendation against alternatives with confidence.

## Procedure

### Pass 0 — Read state

Pull from `grow-context.md`:

| Section | Field | Use |
|---|---|---|
| Stage Tracking | `current_stage`, `flip_date`, `expected_harvest`, `days_in_current_stage` | Days-in-flower + breeder window |
| Active Grow | `strain_1`, `strain_2`, `strain_3`, `seed_or_clone`, `photoperiod_or_auto` | Strain timing reference |
| Sensors / Monitoring | `microscope` | Confirm user has 60x+ tool |
| Space | `location`, `external_climate` | Outdoor weather factor |
| Active Issues | `issue_1`-`issue_3` | Mold/pest pressure may force early chop |

Decision after read:
- If `current_stage` is well before harvest range (e.g., flower-week-3) → respond that it's premature; explain trichome curve and revisit date
- If `microscope` is `[unset]` or magnification < 60x → request macro photo or recommend a jeweler's loupe ($10-30)
- If `photoperiod_or_auto` = auto → use sprout date, not flip date, for timing context

### Pass 1 — Photo quality gate

Reject and request retake if any fails:

| Check | Pass criteria |
|---|---|
| Light | White light or daylight (NOT purple/blurple LED) |
| Magnification | Trichome stalks visibly resolved (60x+ loupe, USB scope, or phone macro) |
| Subject | Trichomes ON CALYX, not sugar leaf or trim |
| Sample points | Top cola + mid + lower bud (3+ photos) |
| Focus | Trichome heads in sharp focus |

If gate fails → respond with what's missing, do NOT proceed to reading.

### Pass 2 — Trichome read

For each sample point, estimate rough percentages:

| Trichome state | Appearance | Meaning |
|---|---|---|
| **CLEAR** | Glassy, transparent, hollow-looking | Immature; THC still building |
| **CLOUDY / MILKY** | White, opaque, full | Peak THC; harvest window |
| **AMBER** | Honey-orange to dark brown | THC degraded to CBN; sedating, less psychoactive |

Standard windows by effect preference:

| Preference | Cloudy : Amber target | Notes |
|---|---|---|
| Heady / racy / energetic | ~90% cloudy / 5-15% amber | Earlier chop; preserves THC peak |
| Balanced | ~70-80% cloudy / 20-30% amber | Most popular; mixed effect |
| Sedating / couchlock | ~50-70% cloudy / 30-50% amber | Later chop; CBN-shifted |

Past 50% amber → over-ripe; significant THC → CBN conversion; harvest immediately.
Less than 10% cloudy → NOT ready regardless of pistil/days.

### Pass 3 — Cross-check secondary signals

| Signal | Reading |
|---|---|
| Pistils 70-90% orange/brown | Approaching ripeness; not definitive alone |
| Pistils 100% receded/dried | Often past peak in modern hybrids |
| Calyx swelling (fattened, almost-closed shape) | Late ripening signal; pairs with mature trichomes |
| Lower leaf fade (yellow / autumn colors) | NORMAL late-flower ripening — not a deficiency |
| Bud no longer densifying | Final maturation phase |
| Smell at strongest | Peak terpene preservation; do NOT wait beyond this |
| Trichome maturity uniform across plant | Whole-plant chop one go |
| Trichome maturity differs top vs lower | Staggered harvest — top first, lowers 5-10 days later |
| Trichome maturity disconnect from calyx swell | Possible stress (foxtail / re-veg) — investigate before chop |

### Pass 4 — Strain timing context

Pull `strain_1`-`strain_3` and look up typical flower duration:

| Strain class | Flower length | Notes |
|---|---|---|
| Indica-dominant modern hybrid | 8-9 weeks from flip | Most fast-finishers |
| Balanced hybrid | 9-10 weeks | Most modern commercial cultivars |
| Sativa-leaning hybrid | 10-12 weeks | Patience required |
| Heavy sativa / Haze / classic OG | 11-14 weeks | Don't trust 9-week claim from breeder |
| Autoflower (modern) | 8-10 weeks total from sprout | Use sprout date, not flip |
| Autoflower (slow / sativa-leaning) | 10-12 weeks total | Some lines drag out |

Compare `days_in_current_stage` (or days from `flip_date`) to expected window. If trichomes appear ready well BEFORE expected window → suspect false signal; recheck second photo from a different sample point.

### Pass 5 — Outdoor / weather factor

If `location` or `external_climate` indicates outdoor:

| Forecast condition | Action |
|---|---|
| Frost within 5-7 days | Harvest if 70%+ cloudy; accept slight early-chop loss vs total loss |
| Multi-day rain/storms | Harvest if reasonable maturity; bud rot risk overrides ideal trichome read |
| Late-season caterpillar damage | Check daily; chop at first severe damage |
| Heavy nighttime humidity (>75%) | Heightened bud rot watch; chop if maturity is in window |
| Stable dry forecast 10+ days | Wait for ideal trichome read |

Indoor → weather doesn't apply; trichome maturity drives timing entirely.

### Pass 6 — Generate recommendation

Output one of:

| Recommendation | Trigger |
|---|---|
| **HARVEST NOW** | Trichome read in user's preferred window + signals confirm |
| **HARVEST IN N DAYS** | Close to window; give specific recheck date and what to look for |
| **WAIT, NOT READY** | <50% cloudy or under 70% on user's preferred range |
| **STAGGER (top first)** | Top mature, lower buds need 5-10 more days |
| **HARVEST EARLY (weather)** | Outdoor + forecast forces early chop |

Always include:
- Confidence level (HIGH / MEDIUM / LOW)
- What user should do in the meantime (if WAIT)
- Recheck date (if WAIT or IN N DAYS)
- Reference to `13-harvest.md` for execution if HARVEST NOW
- Reference to `14-drying.md` for what's next

### Pass 7 — State update (if user adopts)

`grow-context.md`:
- `last_updated`: today
- `last_updated_by`: agent
- `source_workflow`: harvest-readiness
- `current_stage`: update if action taken (e.g. → "harvest day 0" or "ripening week 1")

`grow-log.md` append:
```
## [DATE] — Harvest readiness check
Stage: [current_stage], days from flip: [N]
Trichome read: [X% clear / Y% cloudy / Z% amber] across [N sample points]
Pistils: [%]; calyx swell: [Y/N]
Strain timing context: [strain class + expected window]
Recommendation: [HARVEST NOW / IN N DAYS / WAIT / STAGGER / EARLY-WEATHER]
Confidence: [HIGH/MED/LOW]
User decision: [chop / wait / stagger]
```

## Output Format

```
HARVEST READINESS — [strain_1]

Setup recap (from grow-context.md):
- Strain(s): [strain_1] / [strain_2] / [strain_3]
- Photo or auto: [photoperiod_or_auto]
- Flip date: [flip_date]
- Days in flower: [calculated from flip_date or days_in_current_stage]
- Breeder estimate: [expected_harvest]
- Current stage: [current_stage]
- Location: [location] [outdoor: + external_climate]

Photo evaluation:
- Light quality: [PASS / FAIL — reason]
- Sample points evaluated: [N]
- Subject: [trichomes on calyx / sugar leaf — confirm calyx]

Trichome read (averaged across samples):
- Clear: [X%]
- Cloudy: [Y%]
- Amber: [Z%]

Secondary signals:
- Pistils: [%]
- Calyx swell: [Y/N/partial]
- Leaf fade: [normal / unusual]
- Smell: [building / peak / past peak]

Strain context: [strain class + typical flower length] — you're at day [N] of expected [range].

[If outdoor:]
Weather factor: [forecast summary, mold/frost pressure]

RECOMMENDATION: [HARVEST NOW / IN N DAYS / WAIT / STAGGER TOP-DOWN / HARVEST EARLY (WEATHER)]

CONFIDENCE: [HIGH / MEDIUM / LOW]
Reason: [explanation referencing trichome + signals + strain timing]

By effect preference:
- HEADY → [match to current trichome read; chop now / wait N days]
- BALANCED → [same]
- SEDATING → [same]

NEXT STEPS:
- [Specific action: cut now / recheck on date / dial environment]
- [If WAIT: what to do in meantime — typically nothing, watch trichomes]
- [If HARVEST: load 13-harvest.md for execution and 14-drying.md for next stage]

Want me to log this read and your decision? [Y/N]
```

## State Updates

If user adopts HARVEST NOW:
- `grow-context.md`:
  - `last_updated`: today
  - `last_updated_by`: agent
  - `source_workflow`: harvest-readiness
  - `current_stage`: "harvest day 0"
- `grow-log.md`: append entry per Pass 7 template

If user adopts WAIT:
- `grow-log.md`: append the read + recheck date
- No `current_stage` change

If user is just exploring → no state update.

## Pitfalls

| Pitfall | Prevention |
|---|---|
| Trichome read on sugar leaves, not calyxes | Always specify ON CALYX; sugar-leaf trichomes mature earlier and mislead toward early chop |
| Chopping based on pistils alone | Pistils are secondary; trichome rules. Many strains show 100% receded pistils while trichomes still cloudy |
| Trusting breeder day-count over trichome read | Genotype × environment variance is huge; trichomes are ground truth |
| Single-point reading | Top, middle, bottom mature differently — always multi-sample |
| Imposing your preferred effect on user | Ask preference; let them decide on the cloudy:amber ratio |
| Skipping photo gate when user is impatient | Bad photo → bad call → lost crop quality. Hold the line on photo quality. |
| Waiting past 50% amber | THC has degraded significantly to CBN; harvest now |
| Ignoring weather forecast outdoor | Frost / storm / mold pressure overrides ideal trichome read |
| Confusing late-flower leaf fade with deficiency | Lower-leaf fade weeks 7+ is normal ripening, NOT a chop signal alone |
| Chopping while smell is still building | Peak terps appear in last 1-2 weeks; weak smell = likely not done |
| Misreading foxtail or re-veg as ripening | Stress-driven calyx growth without trichome maturity — investigate |
| Ignoring `photoperiod_or_auto` field | Autos use sprout date, photos use flip date — different timing math |
| Recommending chop without referencing `13-harvest.md` for execution | Always link to next workflow/file |

## Verification

Before sending:
- [ ] `grow-context.md` was read?
- [ ] Photo quality gate evaluated (white light, macro, calyx-mounted)?
- [ ] Multiple sample points present (top, mid, bottom)?
- [ ] Trichome %s explicit (clear / cloudy / amber)?
- [ ] Secondary signals cross-checked (pistils, calyx swell, leaf fade, smell)?
- [ ] Strain timing context cited (strain class + expected flower length)?
- [ ] Outdoor weather factored if applicable?
- [ ] User's effect preference asked or referenced?
- [ ] Recommendation specific (NOW / N DAYS / WAIT / STAGGER / EARLY-WEATHER)?
- [ ] Confidence level stated?
- [ ] If HARVEST NOW → linked to `13-harvest.md` and `14-drying.md`?
- [ ] If WAIT → recheck date specified?
- [ ] State update offered with explicit Y/N?

If any answer is no → fix before sending.

## References

- Knowledge:
  - `13-harvest.md` — harvest execution (cutting, hanging, room sanitization)
  - `01-genetics-strains.md` — strain timing variance, sativa vs indica vs auto
  - `12-flowering.md` — flower stages and ripening signals
  - `09-disease.md` — botrytis pressure for outdoor weather calls
  - `14-drying.md` — next stage after harvest
  - `21-troubleshooting-tree.md` — bud-specific symptom routing (foxtail / re-veg / nanners)
- State (exact field names):
  - `grow-context.md` → `current_stage`, `flip_date`, `expected_harvest`, `days_in_current_stage`, `strain_1`, `strain_2`, `strain_3`, `seed_or_clone`, `photoperiod_or_auto`, `microscope`, `location`, `external_climate`, `issue_1`, `issue_2`, `issue_3`
- Rules:
  - `SKILL.md` Rule 2 — confidence framework (HIGH/MED/LOW)
  - `SKILL.md` Rule 3 — intake (photo quality, multi-sample required)
  - `SKILL.md` Rule 4 — adaptive depth (calibrate explanation to user tier)
  - `SKILL.md` Rule 6 — silent state updates with end-of-session summary
