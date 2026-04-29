# Workflow: Troubleshoot Grow

Non-photo diagnostic workflow. Used when user reports a problem in text form without a photo attached, or when the problem is described in terms that don't require visual confirmation (quantitative environment data, equipment failure, observed pest activity). Companion to `diagnose-from-photo.md` — that workflow handles all visual diagnosis.

This workflow runs the intake checklist plus the symptom routing in `21-troubleshooting-tree.md`, then produces a confidence-gated ranked diagnosis. **Without visual confirmation, confidence caps at MEDIUM** unless the symptom is text-unambiguous. Ambiguous symptoms route explicitly to `diagnose-from-photo.md` rather than guess.

## When to Use

- User reports a problem in text only (no photo attached or available)
- User refused or can't take a photo right now (lighting, location, time)
- Problem is described quantitatively (out-of-range numbers, equipment failure)
- Follow-up after a prior photo session where user reports a text update ("the spots got bigger")
- User wants to walk through symptoms before deciding whether to photograph

## Hard Rules

1. **Confidence caps at MEDIUM by default.** HIGH requires a photo (route to `diagnose-from-photo.md`) or an unambiguous text pattern from the table below.
2. **Run full intake checklist (SKILL.md Rule 3).** Without visual confirmation, the intake data must be MORE complete than for photo diagnosis, not less.
3. **AMBIGUOUS symptoms → REQUEST PHOTO and route to `diagnose-from-photo.md`.** Do not guess. Color changes, droop, generic "looks weird," "spots," "curling" — these need visual.
4. **UNAMBIGUOUS symptoms (table below) → proceed with diagnosis but cap MEDIUM.** Examples: webbing + dots = spider mites; quantitative environment out of range; equipment failure described.
5. **Always provide top 3 ranked possibilities** with confirm-it / rule-it-out criteria — same as photo workflow.
6. **State the data delta explicitly.** What additional info (photo, runoff measurement, microscope inspection) would lift confidence to HIGH.
7. **Never let the workflow become a "just give me a guess" shortcut** that bypasses photo-gating. If the user pushes for HIGH confidence on an ambiguous symptom without a photo, hold the cap and explain why.
8. **Never single-answer a diagnosis from text alone.** Top 3 ranking is mandatory.

## Unambiguous Text Patterns (MEDIUM achievable without photo)

| User text | Diagnosis (MEDIUM cap) |
|---|---|
| "Webbing in canopy + tiny moving dots" | Spider mites — `08-pests.md` |
| "White cottony lumps in leaf nodes" | Mealybugs — `08-pests.md` |
| "Tiny black flying gnats around soil surface" | Fungus gnats — `08-pests.md` |
| "Caterpillar frass + holes chewed in buds" | Budworms / caterpillars — `08-pests.md` |
| "RH 80% sustained in flower week 5+" | Environment out of range — mold/PM risk → `02-environment.md` + `09-disease.md` |
| "Temp hit 95°F sustained under lights" | Heat stress confirmed by environment → `02-environment.md` |
| "Overwatered — heavy pot, drooping no color change, recent water" | Overwatering — substrate confirmed → `04-medium-*.md` |
| "AC died 6 hours, leaves curled up since" | Heat stress from equipment failure → `02-environment.md` |
| "Just up-potted yesterday, droopy today" | Transplant shock — normal 24-48h → `11-propagation.md` |
| "pH meter reads 4.5 at runoff" | pH crash quantitatively confirmed → `05-water-quality.md` |
| "Runoff EC 5.0, fed at 1.8" | Salt buildup quantitatively confirmed → `05-water-quality.md` |
| "Light leak during dark cycle, plants reverting" | Re-veg from photoperiod break → `12-flowering.md` |
| "Slugs visible chewing leaves outdoor" | Slug damage → `08-pests.md` |
| "Pump died overnight, DWC plants wilted" | Root anaerobic exposure / transient stress → `04-medium-hydro.md` |
| "Cured jar smells like ammonia after 3 days" | Cure failure — Aw too high → `15-curing.md` |
| "Hay smell after 5-day dry" | Over-dried during dry phase → `14-drying.md` |
| "Stalled at popcorn buds week 6" + heavy stress event reported | Stress-driven flowering halt → `12-flowering.md` |

## Ambiguous Patterns (REQUEST PHOTO, route to `diagnose-from-photo.md`)

| User text | Why ambiguous |
|---|---|
| "Leaves are turning yellow" | N vs Mg vs Fe vs S vs disease vs ripening — visual pattern essential |
| "Plant looks weird" | Catch-all; need visual |
| "Spots on leaves" | Septoria vs PM vs nute def vs nute tox vs pest damage |
| "Curling leaves" | Heat vs salt vs nute tox vs herbicide drift — pattern matters |
| "Leaves drooping" | Over vs under water vs root rot — substrate + visual confirm |
| "Buds look weird" | Foxtail vs nanners vs bud rot vs PM — visual |
| "Plant looks unhappy" | No diagnostic info |
| "Trichomes look ready" | Trichome read MUST have macro photo — see `harvest-readiness.md` |
| "There's something on the leaves" | Visual required |
| "Color seems off" | Visual required |
| "Plant is stunted" | Genetic vs HLVd vs root vs nute vs cold — visual + intake |
| Anything described as a "color" without specific pattern | Visual essential |

## Procedure

### Pass 0 — Read state and assess data completeness

Read:
- `user-profile.md` — pull tier and communication preferences for response calibration
- `grow-context.md` — full file; note which intake fields are populated vs `[unset]`

Note which fields the user already provided in this conversation vs which are missing.

### Pass 1 — Run intake checklist (mandatory)

Per `SKILL.md` Rule 3, required before diagnosis:

| Field | Source |
|---|---|
| Stage | `current_stage` from grow-context |
| Medium + container size + container type | `medium`, `container_size`, `container_type` |
| Light type, wattage, distance, photoperiod | `type`, `wattage_at_wall`, `hang_height_cm`, `photoperiod` |
| Last feed: EC in, pH in, volume per pot | `ec_in`, `ph_in`, `volume_per_pot_ml` |
| Last runoff: EC, pH (if measured) | `runoff_ec`, `runoff_ph` |
| Room temp + RH (day and lights-off) | `temp_day_target`, `temp_night_target`, `rh_day_target`, `rh_night_target` |
| Water source | `source`, `input_ec`, `input_ph` |
| Nutrient line + current schedule | `brand`, `schedule_followed` |
| Anything changed in past 5-7 days | Ask user — most "sudden problems" trace to a change |

If 3+ fields are unknown AND material to the symptom → **request the missing data first, do not diagnose**. Tell user what to measure and how.

### Pass 2 — Classify symptom (unambiguous vs ambiguous)

Match user's symptom description against the **Unambiguous Text Patterns** table.

- **Match** → proceed to Pass 4
- **No match / partial match** → Pass 3 (ambiguous routing)

Borderline cases (e.g., "leaves yellow with green veins" partially matches Mg) → still treat as ambiguous and request photo. Better to escalate than guess wrong.

### Pass 3 — Ambiguous routing (request photo, offer LOW fallback)

Tell user explicitly:

> "Without seeing the [color change / spots / curl / weirdness], I can't responsibly diagnose past LOW confidence. The symptom you described has 4-6 possible causes that look different in person.
>
> → To get to MEDIUM/HIGH confidence: send a photo and I'll run the `diagnose-from-photo` protocol.
> → Photo requirements: white light or daylight (not blurple LED), focused, whole-plant shot + close-up of the issue area.
>
> If a photo isn't possible right now, I can walk you through the troubleshooting tree at LOW confidence — top 3 possibilities, each with confirm-it/rule-it-out criteria you can check yourself. Reply 'low ok' to proceed that way, or send the photo for HIGH."

If user accepts LOW route → continue to Pass 4 with confidence capped at LOW. Note explicitly in the diagnosis.

If user sends photo → exit this workflow, route to `diagnose-from-photo.md`.

### Pass 4 — Walk troubleshooting tree

Use `21-troubleshooting-tree.md` branches based on symptom category:

| Symptom category | Branch |
|---|---|
| Color | A — Color/Discoloration |
| Shape (curl, taco, twist) | B — Shape & Structure |
| Vigor (slow, stunted, fast) | C — Growth & Vigor |
| Smell | D — Smell & Odor |
| Pest visible | E — Pest |
| Disease visible | F — Disease |
| Bud-specific | G — Bud-Specific |
| Numbers off (pH, EC, runoff) | H — Numbers |
| Environment off | I — Environment |
| Roots | J — Root Issue |
| Whole-plant systemic | K — Systemic |
| Multi-plant pattern | L — Multi-Plant Pattern |
| Autoflower-specific | L+ — Autoflower-Specific |

Cross-reference grow-context state for confirmation:
- "Your runoff EC is X, your input was Y → salt buildup confirmed"
- "Your medium is coco + RO water and `cal_mg` is unset → Ca/Mg deficiency likely; runoff EC < input also supports"
- "Recent change: switched water source 4 days ago → high probability the new water profile drove this"

### Pass 5 — Generate top 3 ranked possibilities

Always 3, ranked by likelihood given symptom + intake data + state context. Each entry:
- % confidence
- **Why** — evidence from symptom + intake + grow-context
- **Confirms it** — specific test/check the user can run (measure runoff, lift pot, inspect underside, etc.)
- **Rules it out** — specific finding that would eliminate this possibility

### Pass 6 — Confidence statement (capped MEDIUM, occasionally LOW)

State explicitly:
- **Confidence: MEDIUM** (text-unambiguous match + complete intake)
- **Confidence: LOW** (ambiguous symptom + user declined photo, OR intake incomplete)
- **Confidence: HIGH is not available without a photo for this symptom** (state this when user pushes back on the cap)

Cite source tier where applicable per `SKILL.md` Rule 5.

### Pass 7 — Action plan

Three-part structure:

**IMMEDIATE ACTION** (low-risk, high-value steps):
- 1-3 actions that don't risk making the problem worse if the diagnosis is wrong
- Examples: check runoff pH/EC, lift pot to assess weight, inspect leaf undersides with loupe, lower humidity if too high

**DO NOT DO YET** (reactive moves to avoid until cause confirmed):
- Don't flush blindly
- Don't add Cal-Mg without confirming it's needed
- Don't spray foliar without confirming pest/disease ID
- Don't crank EC up
- Don't change multiple variables at once

**CONFIRM-OR-PIVOT IN 24-72H**:
- "If runoff pH still drifts → confirmed #1 (lockout), proceed with reset flush"
- "If new growth normalizes → confirmed #2 (transient), no further action"
- "If symptom worsens → escalate, send photo, reload diagnose-from-photo"

### Pass 8 — Data delta to lift confidence

Always include explicit "what would lift confidence" section:
- "Send photo of [specific area] under white light → lifts to HIGH"
- "Measure [specific value: runoff EC / leaf temp / RH at canopy] → tightens ranking"
- "Loupe inspection of leaf undersides → confirms or rules out pest"

### Pass 9 — State update

`grow-context.md`:
- `last_updated`: today
- `last_updated_by`: agent
- `source_workflow`: troubleshoot-grow
- Update `issue_1` (or next available `issue_N` slot) with short description + status (active / monitoring)

`grow-log.md` append:
```
## [DATE] — [stage] — Issue: [short description]
Source workflow: troubleshoot-grow (text-only diagnosis)
Confidence: [MEDIUM / LOW]
Top diagnosis: [#1 possibility]
Top 3 considered: [#1 / #2 / #3]
Intake completeness: [HIGH / MED / LOW]
Action plan: [user's chosen action]
Follow-up: [recheck date]
Photo escalation offered: [Y/N — outcome if Y]
```

Show the draft entry to the user for confirmation before saving.

## Output Format

```
TROUBLESHOOT — [issue summary, 1 line]

Setup recap (from grow-context.md):
- Stage: [current_stage]
- Medium: [medium] / [medium_brand], [container_size]
- Light: [type] @ [wattage_at_wall], [hang_height_cm]
- Last feed: EC [ec_in], pH [ph_in], [volume_per_pot_ml]
- Runoff: EC [runoff_ec], pH [runoff_ph]
- Temp/RH: [temp_day_target] / [rh_day_target] (day), [temp_night_target] / [rh_night_target] (night)
- Water: [source], input EC [input_ec], pH [input_ph]
- Nutrient line: [brand] / [schedule_followed]
- Recent changes: [list or "none reported"]

Intake completeness: [HIGH / MED / LOW based on field coverage]

SYMPTOM CLASSIFICATION: [UNAMBIGUOUS / AMBIGUOUS]

[If AMBIGUOUS — request photo first:]

Symptom is ambiguous from text alone. Possible causes include:
- [cause 1]
- [cause 2]
- [cause 3]
- [cause 4]
Each looks different in person.

→ Send a photo and I'll run diagnose-from-photo for HIGH confidence.
→ Photo requirements: white light or daylight, focused, whole plant + close-up of issue area.

If a photo isn't possible right now, reply "low ok" and I'll walk the troubleshooting tree at LOW confidence with confirm-it/rule-it-out criteria you can check yourself.

[If UNAMBIGUOUS or user accepted LOW route:]

DIAGNOSIS — Confidence: [MEDIUM / LOW]

Top 3 possibilities (ranked):

1. [MOST LIKELY] — [X]% confidence
   Why: [evidence from symptom + intake + grow-context cross-check]
   Confirms it: [specific test or check]
   Rules it out: [specific finding]

2. [SECOND] — [Y]% confidence
   Why: [evidence]
   Confirms it: [test]
   Rules it out: [finding]

3. [THIRD] — [Z]% confidence
   Why: [evidence]
   Confirms it: [test]
   Rules it out: [finding]

ROOT CAUSE INVESTIGATION:
Even if the surface symptom is X, check Y first because [pH/water/genetics often underlying].

IMMEDIATE ACTION (low-risk, high-value):
1. [step]
2. [step]
3. [step if applicable]

DO NOT DO YET:
- [reactive move 1 to avoid]
- [reactive move 2 to avoid]

CONFIRM-OR-PIVOT IN 24-72H:
- If [outcome A] → confirmed #1, proceed with [treatment]
- If [outcome B] → pivot to #2
- If worse → escalate, send photo, reload diagnose-from-photo

DATA DELTA TO LIFT CONFIDENCE:
- Send photo of [specific area] under white light → lifts to HIGH
- Measure [specific value] → tightens ranking
- [Other escalation as relevant]

LOG ENTRY DRAFT (for grow-log.md):
[draft entry per Pass 9 template]

Want me to log this and the action you take? [Y/N]
```

## State Updates

After diagnosis:

`grow-context.md`:
- `last_updated`: today
- `last_updated_by`: agent
- `source_workflow`: troubleshoot-grow
- `issue_1` (or next slot): "[short description] — active, [date]"

`grow-log.md`:
- Append issue + diagnosis + action plan + follow-up date entry per Pass 9 template

If user takes the action and reports back at follow-up:
- Update `issue_1` to "resolved" or "monitoring" or pivot to new diagnosis
- Append resolution entry to grow-log

If user is just exploring or didn't accept any action → no state update; offer to log later.

## Pitfalls

| Pitfall | Prevention |
|---|---|
| Diagnosing ambiguous symptom from text alone | Hard Rule 3: route to `diagnose-from-photo.md`; never guess |
| Stating HIGH confidence without photo | Hard Rule 1: cap MEDIUM regardless of how confident the text feels |
| Skipping intake checklist because user is impatient | Hard Rule 2: intake more thorough without visual, not less |
| Single-answer diagnosis | Hard Rule 5: top 3 always |
| Letting confidence drift up over conversation | Hold the cap unless new evidence (photo, measurement) arrives |
| Failing to specify what would lift confidence | Pass 8 DATA DELTA section is mandatory |
| Routing to photo workflow without listing photo requirements | Always include white-light + focus + whole-plant + close-up specifics |
| Becoming a "give me a guess" shortcut | Hard Rule 7: photo-gating discipline holds |
| Forgetting recent-change question | Always include "anything changed in past 5-7 days" in intake — most sudden issues trace there |
| Confusing intake checklist (per-question) with onboarding (state-population) | Different purposes; intake is for diagnosis, onboarding is for long-arc state |
| Recommending action without confirm-or-pivot timing | Pass 7 always includes 24-72h recheck criteria |
| Logging without showing user the draft entry | Show draft before save (per `grow-log.md` schema) |
| Ignoring grow-context state when ranking possibilities | Cross-reference always — RO + coco + no Cal-Mg → Ca/Mg likely |
| Treating MEDIUM as good enough when it's the cap | Always offer the photo escalation path explicitly |
| Walking ambiguous symptom at LOW without user explicitly opting in | Pass 3 requires "low ok" or equivalent before proceeding |

## Verification

Before sending:
- [ ] `grow-context.md` and `user-profile.md` were read?
- [ ] Intake checklist run (or missing fields explicitly requested first)?
- [ ] Symptom classified as UNAMBIGUOUS or AMBIGUOUS against the table?
- [ ] If ambiguous → photo requested AND `diagnose-from-photo.md` route offered?
- [ ] If ambiguous + user opted into LOW → confidence capped at LOW (not MEDIUM)?
- [ ] If unambiguous → confidence stated as MEDIUM (not HIGH)?
- [ ] Top 3 possibilities ranked with confirm-it / rule-it-out criteria?
- [ ] IMMEDIATE / DO NOT DO YET / CONFIRM-OR-PIVOT structure used?
- [ ] DATA DELTA section listing what would lift confidence?
- [ ] Source tier cited where applicable?
- [ ] `grow-log.md` entry drafted for user to confirm before save?
- [ ] State update offered with explicit Y/N?
- [ ] Photo escalation path explicitly preserved (never closed off)?

If any answer is no → fix before sending.

## References

- Knowledge:
  - `21-troubleshooting-tree.md` — symptom routing branches A through L+
  - `07-deficiencies.md` — nutrient symptoms (cross-reference for color/pattern)
  - `08-pests.md` — pest patterns (some unambiguous from text)
  - `09-disease.md` — disease patterns
  - `02-environment.md` — temp/RH/VPD thresholds
  - `05-water-quality.md` — pH and EC interpretation
  - `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md` — medium-specific symptom mechanics
  - `12-flowering.md` — bud-specific symptom interpretation
  - `14-drying.md`, `15-curing.md` — post-harvest symptom routing
- Workflows:
  - `diagnose-from-photo.md` — REQUIRED escalation path for ambiguous symptoms
  - `build-feed-schedule.md` — if root cause is feed mismatch
  - `harvest-readiness.md` — if symptom is late-flower / ripeness related
  - `onboarding.md` — if state files empty before diagnosis can run
- State (exact field names referenced):
  - `grow-context.md` → all intake-relevant fields per Pass 1 table; `issue_1`-`issue_3` for active issue tracking
  - `user-profile.md` → tier (`agent_assessed_tier`) for response calibration
- Rules:
  - `SKILL.md` Rule 2 — confidence framework (HIGH / MED / LOW)
  - `SKILL.md` Rule 3 — intake checklist (this workflow's backbone)
  - `SKILL.md` Rule 4 — adaptive depth (calibrate to user tier)
  - `SKILL.md` Rule 5 — source hierarchy (cite when applicable)
  - `SKILL.md` Rule 6 — silent state updates with end-of-session summary
- **Hard rule callout:** Confidence cap MEDIUM is non-negotiable. The photo workflow exists to lift to HIGH. If the user wants higher confidence, they need to send the photo. Do not let conversational pressure erode the cap.
