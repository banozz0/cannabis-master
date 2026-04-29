# Workflow: New Grow Setup

Pre-grow planning workflow. Used when the user is planning a build BEFORE plants are sprouted — establishes goals, constraints, and a phased equipment plan. State writes go primarily to `user-profile.md` (slow-changing facts about the user). A planning draft is written to `grow-context.md` flagged as PLANNED, with operational fields left unset until the grow actually starts.

For an active-grow problem or stage-transition question, use `troubleshoot-grow.md` or `build-feed-schedule.md` instead.

## When to Use

- "I want to start growing"
- "I want to set up a tent / room / greenhouse"
- "Help me plan my first grow"
- User has gear in mind but unclear on integration
- User has space/budget/electrical constraints to design around
- User upgrading from current setup to bigger build (planning new room, not running it)
- User asks about equipment selection in the abstract

## Hard Rules

1. **PLANNING ONLY — no active-grow fields written.** During planning, mark `grow-context.md` as PLANNED in the freeform notes and **DO NOT populate operational fields**:
   - `current_stage`, `veg_started`, `flip_date`, `expected_harvest`, `days_in_current_stage`
   - Current Feed: `date`, `ec_in`, `ph_in`, `volume_per_pot_ml`, `runoff_ec`, `runoff_ph`, `runoff_volume_pct`, `feed_frequency`
   - Training Applied: `techniques_used`, `top_count`, `last_defoliation_date`, `scrog_screen`, `trellis_layers`
   - Active Issues: `issue_1`, `issue_2`, `issue_3`
   - These populate when the grow actually starts (first sprout in medium or first clone potted).
2. **Read both state files first.** `user-profile.md` for goals/budget/experience, `grow-context.md` for any prior planning notes.
3. **Match recommendations to constraints** from `user-profile.md`: `budget_tier`, `space_ceiling`, `electrical_ceiling`, `noise_constraints`, `smell_constraints`, `heat_dump_constraints`, `physical_limits`, `time_per_week`.
4. **Don't recommend what user already owns** — check Tools & Brands Familiar section (`nutrients_used_before`, `lights_used_before`, `meters_owned`, `controllers_used`).
5. **Phase the recommendations.** Essentials (must-have to start) first, dial-in (during first grow) second, upgrades (later grows) third.
6. **Region + climate matters.** Hot/dry vs cold/humid drives different HVAC and medium choices — pull from `home_region` and `external_climate`.
7. **Cite source tier** for non-obvious specs (PPFD targets, dehumidification sizing) per `SKILL.md` Rule 5.
8. **End with a pre-flight checklist** the user runs before sprouting. The grow doesn't activate (and operational fields don't populate) until that checklist passes.

## Procedure

### Pass 0 — Read state and confirm planning intent

Read:
- `user-profile.md` — full file
- `grow-context.md` — only relevant if prior planning notes exist

Confirm with user:
> "This is planning a future grow, not an active one — I'll write your goals and constraints to user-profile, and start a PLANNED draft of grow-context that won't be activated until your first plant goes in. Confirming this is the right workflow?"

If user has an active grow → route them to `troubleshoot-grow.md`, `build-feed-schedule.md`, or `harvest-readiness.md` as appropriate.

### Pass 1 — Establish long-arc goals

Walk the `user-profile.md` Goals section if not already populated:

| Field | Question |
|---|---|
| `end_objective` | "What's the end goal — personal supply, friends/family, breeding stock, commercial, R&D?" |
| `year_horizon` | "How far ahead are you planning — one grow, a year, or longer?" |
| `target_potency` | "Any specific potency or cannabinoid focus (THC%, CBD-dominant, minor cannabinoids)?" |
| `target_terps` | "Specific terpene targets, or just whatever smells good?" |
| `graduation_path` | "Where do you want to go after this — same setup forever, or step up to new medium/scale/technique?" |
| `learning_goals` | "What do you want to get better at this year?" |

If goals already filled → confirm and adjust if changed.

### Pass 2 — Establish constraints

Walk `user-profile.md` Long-Term Constraints + Identity sections:

| Field | Question |
|---|---|
| `space_ceiling` | "Maximum footprint you can dedicate to growing?" |
| `electrical_ceiling` | "Amps available at the grow location? (15A US household = 1800W ceiling at 80% load)" |
| `budget_tier` | "Bootstrap, mid, or unconstrained?" |
| `noise_constraints` | "Apartment / shared building / standalone — how quiet does this need to be?" |
| `smell_constraints` | "Carbon filter mandatory? Any landlord/neighbor concerns?" |
| `heat_dump_constraints` | "Where does heat from lights go — into living space, attic, vented outside?" |
| `physical_limits` | "Any back/mobility issues that affect heavy lifting or training?" |
| `time_per_week` | "Realistic hours per week available for the grow?" |
| `home_region` | "Region + climate — affects HVAC, medium, mold pressure, etc." |

### Pass 3 — Recommend space type

Match constraints to space pattern:

| Constraint pattern | Recommended space |
|---|---|
| Apartment, smell + noise sensitive | Sealed grow tent + carbon filter; mini-split AC if a window allows it |
| Garage / spare room, moderate budget | Tent or partial-room conversion, vented through window or wall |
| Standalone outbuilding | Insulated room, full HVAC, sealed CO2-capable |
| Outdoor, mild climate | Light-dep greenhouse or pure outdoor |
| Outdoor, harsh climate | Greenhouse with supplemental light + heating |
| Limited time + tight space | Auto in 2x2 or 3x3 tent, hand-water, simple line |
| Commercial planning | See `20-commercial-ops.md` for facility design |

Output: recommended space type + footprint + reasoning tied to constraints.

### Pass 4 — Recommend lighting

Match space size × budget tier:

| Space | Bootstrap | Mid | Unconstrained |
|---|---|---|---|
| 2x2 (4 sqft) | 100-150W LED quantum board | 150W premium (HLG, Mars, Spider Farmer) | Same — diminishing returns past 200W |
| 3x3 (9 sqft) | 250-300W LED | 300W premium (Photontek, AC Infinity Ionframe Evo 6) | 350-400W bar |
| 4x4 (16 sqft) | 450-500W LED | 600-730W premium (Fluence SPYDR, Gavita LED, Ionframe Evo 8) | 800W bar-style |
| 5x5 (25 sqft) | 600W LED | 800W premium | 1000W bar |
| Greenhouse / large | HPS supplement (cheap CAPEX) | LED bar arrays | Fluence / Gavita commercial bars |

PPFD targets (cite Bugbee / Rodriguez-Morrison Tier 1):
- Veg: 400-600 µmol/m²/s
- Flower: 800-1200 µmol/m²/s (with CO2 enrichment can push 1500+)

Calculate fixture wattage = canopy_sqft × 35-50 W/sqft for ~1.0 g/W output target.

### Pass 5 — Recommend climate control

Match `home_region` + space + sealed-vs-vented:

| Region pattern | HVAC plan |
|---|---|
| Hot/dry | Mini-split AC, light humidifier in veg, dehumidifier in flower |
| Hot/humid | AC + serious dehumidifier sized for peak flower (~70 pints/day for 4x4 sealed) |
| Cold/dry | Heater for lights-off, humidifier veg, dehumidifier flower |
| Mild/temperate | Inline fan + carbon filter for vented; mini-split for sealed |
| Tropical | AC mandatory + dehumidifier mandatory |

Sealed vs vented:
- **Sealed** → CO2 enrichment possible, full HVAC required, more capital, tighter control
- **Vented** → simpler, no CO2, exhaust + carbon filter, intake passive or active

For sealed: dehumidification is the most under-spec'd system in new builds. Size for peak flower week 5+ load (~3-4 pints/day/sqft canopy under high PPFD; a 4x4 sealed needs 50-70 pint/day capacity, matching the line 118 figure).

### Pass 6 — Recommend medium

Match `nutrient_philosophy` + tier + `automation_preference`:

| User pattern | Recommended medium |
|---|---|
| Beginner, low-automation, organic-leaning | Soil (FFOF or Pro-Mix HP + amendments), 5gal fabric pots |
| Beginner, simple + predictable | Coco-perlite 70/30, 5gal fabric, hand-water with Athena Pro or Jacks 321 |
| Intermediate, optimization-focused | Coco fertigation drip, 3-5gal containers, daily feeds (1-3gal possible for advanced fertigation but increases failure risk if pumps drop). Aligns with `build-feed-schedule.md` default container assumptions. |
| Advanced, max-yield | DWC or RDWC for fast veg + flower; or coco fertigation |
| Advanced, max-quality + organic | Living soil no-till in fabric pots or beds |
| Commercial scale | Rockwool slabs + drip, or amended living-soil beds |
| Outdoor | Amended soil bed or large smart pots (15-30gal) |
| Auto-only | 3-5gal fabric, coco-perlite, never transplant — autos hate root disturbance |

### Pass 7 — Recommend nutrient line

Match medium + experience tier + budget:

| Medium + Tier + Budget | Recommended line |
|---|---|
| Coco / hydro, beginner, bootstrap | Jacks 321 or MegaCrop |
| Coco / hydro, intermediate, mid | Athena Pro or Canna Coco A+B |
| Coco / hydro, advanced, mid+ | Athena Pro |
| Soil, beginner, organic | Pre-amended FFOF + bottle organics (BioBizz, Espoma) |
| Soil, intermediate, organic | Living-soil amendment style or BioBizz/BioCanna full line |
| Living soil, any tier | Cover crops + top-dress + teas (no bottle nutes — see `04-medium-living-soil.md`) |
| Hydro, advanced, R&D | Custom mix from raw salts (Yara, Haifa, Jacks for cost) |

Always include Cal-Mg if RO water + coco/hydro. Silica optional (Mono-Si or potassium silicate at 0.5-1 ml/L).

### Pass 8 — Recommend genetics

Match `strain_preferences` + experience + space + `photoperiod_vs_auto`:

| User pattern | Recommendation |
|---|---|
| First-time grower | Fems from established seedbanks (Royal Queen, ILGM, Seedsman; Mephisto for autos) |
| Pheno-hunter | Regs from breeders (Bodhi, Useful, Cannarado, Compound Genetics) |
| High-yield focus | Known production cultivars (Wedding Cake, GMO, Runtz crosses) |
| Terp focus | Boutique (Skunk Hand Genetics, Symbiotic, Compound, Tiki Madman) |
| Auto-only | Modern auto seedbanks (Mephisto, Fast Buds, Sweet Seeds) |
| CBD-dominant | Sensi Seeds CBD line, Royal Queen Medical, ACDC clones |
| Outdoor | Mold-resistant lines (Frisian Dew, Durban Poison, mountain-bred lines) |

Discipline > variety: **suggest 1-2 strains for first run**, not 5.

### Pass 9 — Ancillary equipment

| Category | Beginner | Intermediate | Advanced |
|---|---|---|---|
| pH meter | Apera PH20 (~$30) | Apera PH60 (~$60) | Bluelab Combo (~$350) |
| EC meter | Bluelab Truncheon (~$90) or HM Digital (~$25) | Apera EC60 | Bluelab Combo (combined) |
| Microscope | Jeweler's loupe 60x (~$10) | USB scope ($20-50) | Carson MicroBrite (~$30) or higher |
| Inline fan + carbon filter | AC Infinity T4/T6 + matching filter | AC Infinity S6/T8 | Hyperfan + commercial filter |
| Oscillating fans | 6-inch clip ($15) | 8-12 inch wall ($40) | Cloudray (~$150) |
| Dehumidifier | Eva-Dry portable (small space) | Frigidaire 50pt | Quest 70/110/Dual ($800-2000) |
| Humidifier | Cool-mist ($30) | Aquaoasis (~$60) | AOS Vornado |
| Thermometer/hygrometer | AC Infinity Cloudcom B1 (~$30) | Pulse One (~$300) | Trolmaster |
| Trim scissors | Chikamasa B-500SF | Chikamasa T-series | Multiple specialized + sharpener |
| Drying rack | Tier mesh rack (~$20) | Tent + dehumidifier setup | Walk-in dry room |
| Curing storage | Mason jars + Boveda | Grove Bags | CVault + Boveda |

### Pass 10 — Build phased plan

**Phase 1 — ESSENTIALS** (must-have to start)
- Tent / room / space
- Light fixture
- Inline fan + carbon filter
- Oscillating fan
- Pots + medium (pre-buffered if coco)
- Nutrient line + Cal-Mg if needed
- pH meter + EC meter + calibration solutions (4.0, 7.0, 1.41 mS/cm)
- Thermometer/hygrometer
- Seeds or clones
- Drying space plan (even if just a closet)
- Curing jars

**Phase 2 — DIAL-IN** (during weeks 2-4 of first grow)
- Microscope (60x+) for trichome reads
- Better fans if airflow is uneven
- Dehumidifier or humidifier based on actual readings (don't buy until you measure)
- Better timer or controller if light schedule is unreliable

**Phase 3 — UPGRADES** (later grows or scale-up)
- Sensor controller (Pulse, AC Infinity Controller 89, Trolmaster)
- Smart fertigation
- CO2 (only if sealed)
- Better lights when income allows
- Tissue culture / clean stock if breeding goal

Output: phased shopping list with priority labels and rough total Phase 1 budget.

### Pass 11 — Pre-flight checklist (before sprouting day)

Before user pops the first seed or pots the first clone, verify:

- [ ] Space sealed or vented per plan, light tested, no light leaks
- [ ] Light hangs in place, dimming verified, height adjustable
- [ ] Inline fan + filter installed, exhaust path tested
- [ ] Temp + RH read in target range under empty-room test (lights ON AND OFF)
- [ ] Water pH meter calibrated with 4.0 + 7.0 buffer (and stored wet)
- [ ] EC meter calibrated with 1.41 mS/cm solution
- [ ] Medium pre-prepared (coco buffered with Cal-Mg if applicable; soil amended if living)
- [ ] Containers labeled
- [ ] Nutrient bottles received and stored properly (cool, dark)
- [ ] Cal-Mg, pH-up, pH-down on hand
- [ ] Backup plan for power outage (UPS for at least controller + circulation, or notes)
- [ ] Grow log started (paper or app)
- [ ] Photo of empty environment for baseline

When user completes this checklist → grow is ready to activate. THEN re-run a brief intake to populate operational fields (`current_stage`, first feed numbers, etc.) per Hard Rule 1.

### Pass 12 — State updates (planning mode)

Write to `user-profile.md`:
- `last_updated`: today
- `last_updated_by`: agent
- `source_workflow`: new-grow-setup
- Update Goals section (`end_objective`, `year_horizon`, `target_potency`, `target_terps`, `graduation_path`, `learning_goals`)
- Update Long-Term Constraints (`space_ceiling`, `electrical_ceiling`, `budget_tier`, `noise_constraints`, `smell_constraints`, `heat_dump_constraints`, `time_per_week`, `physical_limits`)
- Update Cultivation Preferences (`nutrient_philosophy`, `training_philosophy`, `yield_vs_quality_bias`, `automation_preference`, `photoperiod_vs_auto`, `seed_vs_clone`, `indoor_vs_outdoor`, `strain_preferences`, `breeding_interest`)
- Update Tools & Brands Familiar (`nutrients_used_before`, `lights_used_before`, `meters_owned`, `controllers_used`)
- Update Coaching Memory if user expressed preferences (`do_more_of`, `do_less_of`, `non_negotiables`)
- Update Identity & Background (`general_background`, `home_region`)

Write to `grow-context.md` — PLANNING DRAFT:
- `last_updated`: today
- `last_updated_by`: agent
- `source_workflow`: new-grow-setup
- **Populate planning fields:** Space, Lighting, Climate Control, Sensors, Medium & Containers, Water Source, Nutrient Line, Active Grow (strain selection), Goals
- **LEAVE UNSET (Hard Rule 1):** all Stage Tracking, all Current Feed, all Training Applied, all Active Issues
- `## Notes > freeform`: append `"PLANNED grow — sprouting target [date]. Status: PLANNED, not active. Operational fields will populate at first sprout/clone."`

Append `grow-log.md` entry:
```
## [DATE] — Planning session (NEW GROW SETUP)
Status: PLANNED
Goals: [end_objective] / [graduation_path]
Space + lighting + climate + medium + nutrient + genetics drafted.
Phase 1 budget estimate: [range]
Pre-flight checklist issued.
Activation pending: user completes pre-flight, sprouts/clones first plant.
```

## Output Format

```
NEW GROW SETUP PLAN — [user]

Goals (long-arc, from user-profile.md):
- End objective: [end_objective]
- Year horizon: [year_horizon]
- Specific targets: [target_potency / target_terps]
- Graduation path: [graduation_path]

Constraints:
- Space ceiling: [space_ceiling]
- Electrical: [electrical_ceiling]
- Budget tier: [budget_tier]
- Noise / smell / heat: [respective constraints]
- Time per week: [time_per_week]
- Region / climate: [home_region]

PLAN

Space:
[type + size + sealed/vented + reasoning]

Lighting:
[fixture + wattage + PPFD target + reasoning]

Climate control:
[AC + dehumid + humidifier + fans + filter + reasoning]
[Source-tier note for sizing if non-obvious]

Medium + containers:
[medium + container size + count + reasoning]

Water + nutrients:
[water source + Cal-Mg / silica decisions + nutrient line + base schedule reference]

Genetics:
[1-2 strains + breeder + why; flowering window + auto/photo]

Ancillary equipment by tier:
[table — pH meter, EC meter, microscope, fans, etc.]

PHASED SHOPPING LIST

Phase 1 — ESSENTIALS:
1. [item] — [budget range]
...

Phase 2 — DIAL-IN (during first grow):
1. ...

Phase 3 — UPGRADES (later):
1. ...

Total Phase 1 budget estimate: [range]

PRE-FLIGHT CHECKLIST (run before sprouting):
- [ ] [each item from Pass 11]

STATE UPDATES (planning mode):
- user-profile.md: [list of populated fields]
- grow-context.md: PLANNED draft only — operational fields stay unset until first plant goes in
- grow-log.md: planning session entry

CONFIDENCE: [HIGH/MED/LOW] on plan match to your stated goals/constraints.

NEXT STEPS:
- Run the pre-flight checklist when gear is in
- Reply when you're ready to activate the grow — I'll re-run a brief intake to flip grow-context from PLANNED to active and populate stage/feed fields
- For genetics, source seeds [estimated lead time]
- For HVAC, allow 2-4 weeks for shipping if buying

Want me to save this plan now? [Y/N]
```

## State Updates

After plan finalized:

`user-profile.md`:
- `last_updated`, `last_updated_by`: agent, `source_workflow`: new-grow-setup
- All Goals, Long-Term Constraints, Cultivation Preferences, Tools & Brands Familiar, Coaching Memory, Identity fields populated as user provided

`grow-context.md`:
- `last_updated`, `last_updated_by`: agent, `source_workflow`: new-grow-setup
- PLANNING fields populated (Space, Lighting, Climate Control, Sensors, Medium & Containers, Water Source, Nutrient Line, Active Grow, Goals)
- OPERATIONAL FIELDS LEFT UNSET per Hard Rule 1
- Freeform note flags PLANNED status and activation criterion

`grow-log.md`:
- Planning session entry as shown in Pass 12

When user activates the grow (sprouts seed or pots clone) → re-run a brief intake to flip from PLANNED to ACTIVE: populate `current_stage` (= "seedling week 0"), `veg_started`, first Current Feed entry, Training Applied as it begins, etc.

## Pitfalls

| Pitfall | Prevention |
|---|---|
| Populating operational fields during planning | Hard Rule 1; explicit unset list |
| Recommending gear user already owns | Check Tools & Brands Familiar in user-profile |
| Recommending unconstrained-budget gear to bootstrap user | Always pull `budget_tier` |
| Ignoring electrical ceiling | Verify amps; some 4x4 sealed setups draw 1400W+ at peak |
| Recommending sealed CO2 setup to vented user | CO2 leaks out of vented; only worth it sealed |
| Suggesting 5 strains for first grow | Discipline; 1-2 strains per first run |
| Skipping pre-flight checklist | Empty-room test catches issues before plants suffer |
| Sealed room without dehumid sized for flower peak | Mold/PM in week 5+; size dehumid for peak (1.5-2 pints/day/sqft) |
| Recommending mini-split for tiny tent | Overkill for 2x2 / 3x3; AC Infinity inline + filter often enough |
| Ignoring heat dump destination | Heat into living space vs attic vs vented out matters for climate control |
| Skipping region/climate context | Hot tropical user gets very different plan than cold continental user |
| Treating plan as final-binding | First grow reveals what really works; expect Phase 2-3 to shift |
| Activating grow-context too early | Must wait for actual sprout/clone before flipping to active |
| Forgetting to update user-profile preferences | This workflow's biggest write target is user-profile, not grow-context |

## Verification

Before sending the plan:
- [ ] Hard Rule 1 — no operational fields populated in grow-context?
- [ ] `user-profile.md` and `grow-context.md` read first?
- [ ] Goals + constraints fully captured?
- [ ] Region/climate factored in HVAC and medium?
- [ ] Recommendations matched to `budget_tier`, `space_ceiling`, `electrical_ceiling`?
- [ ] Sealed vs vented decision explicit with reasoning?
- [ ] HVAC sized for flower peak humidity?
- [ ] Genetics suggestion limited to 1-2 strains?
- [ ] Ancillary equipment phased (essentials / dial-in / upgrades)?
- [ ] Pre-flight checklist included?
- [ ] State updates flagged: user-profile populated, grow-context as PLANNED draft only?
- [ ] Source tier cited for non-obvious specs (PPFD, dehumid sizing)?
- [ ] Total Phase 1 budget estimate provided?
- [ ] Activation criterion (pre-flight pass + first plant in medium) stated explicitly?

If any answer is no → fix before sending.

## References

- Knowledge:
  - `00-fundamentals.md` — first-time grower context
  - `02-environment.md` — VPD, temp/RH targets, HVAC sizing math
  - `03-lighting.md` — PPFD, DLI, fixture economics, LED vs HPS
  - `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md` — medium tradeoffs
  - `05-water-quality.md` — RO vs tap, alkalinity, pH math
  - `06-nutrients-synthetic.md`, `06-nutrients-organic.md` — line selection
  - `01-genetics-strains.md` — strain timing + selection
  - `08-pests.md`, `09-disease.md` — IPM planning by region
  - `11-propagation.md` — sprouting / cloning prep
  - `20-commercial-ops.md` — for commercial-tier planners
- State (exact field names referenced):
  - `user-profile.md` — Goals, Long-Term Constraints, Cultivation Preferences, Tools & Brands Familiar, Coaching Memory, Identity & Background sections (full field list per Pass 12)
  - `grow-context.md` — PLANNING fields only: `location`, `tent_or_room_size`, `ceiling_height`, `external_climate`, `sealed_or_active`, `fixture_make_model`, `type`, `wattage_at_wall`, `ppfd_target`, `hang_height_cm`, `photoperiod`, `schedule_on_off`, `dimmer_setting`, `temp_day_target`, `temp_night_target`, `rh_day_target`, `rh_night_target`, `vpd_target`, `co2`, `intake_cfm`, `exhaust_cfm`, `carbon_filter`, `ac`, `dehumidifier`, `humidifier`, `heater`, `oscillating_fans`, `controller`, `ph_meter`, `ec_meter`, `ppm_scale`, `microscope`, `camera`, `medium`, `medium_brand`, `container_size`, `container_type`, `plants_per_container`, `total_plant_count`, `source`, `input_ec`, `input_ppm`, `input_ph`, `alkalinity`, `hardness`, `ro_system`, `brand`, `schedule_followed`, `silica`, `cal_mg`, `beneficials`, `ph_down`, `ph_up`, `strain_1`, `strain_2`, `strain_3`, `seed_or_clone`, `photoperiod_or_auto`, `priority`, `target_yield`, `constraints`
  - **DO NOT POPULATE during planning:** `current_stage`, `veg_started`, `flip_date`, `expected_harvest`, `days_in_current_stage`, Current Feed (`date`, `ec_in`, `ph_in`, `volume_per_pot_ml`, `runoff_ec`, `runoff_ph`, `runoff_volume_pct`, `feed_frequency`), Training Applied (`techniques_used`, `top_count`, `last_defoliation_date`, `scrog_screen`, `trellis_layers`), Active Issues (`issue_1`, `issue_2`, `issue_3`), `phenotype_notes` (until pheno-hunting begins)
- Rules:
  - `SKILL.md` Rule 4 — adaptive depth (calibrate to user tier)
  - `SKILL.md` Rule 5 — source hierarchy (cite Bugbee/Rodriguez-Morrison for PPFD, mfg for HVAC sizing)
  - `SKILL.md` Rule 6 — silent state updates with end-of-session summary
- `user-profile.md` Schema Rule 5 — `agent_assessed_tier` drives response shaping until reconciled
- `grow-context.md` Schema Rule 5 — confirm before destructive changes (e.g., overwriting prior planning)
