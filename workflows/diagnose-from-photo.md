# Workflow: Diagnose From Photo

Multi-pass image analysis protocol for plant health diagnosis. Used when user submits a photo of a problem.

## When to Use

- User uploads photo with health concern
- User describes a symptom and references "looks like..."
- Diagnosis confidence in conversation drops below HIGH

## Readiness Note

Photo diagnosis requires a vision-capable active model/path. If vision is unavailable, request the full text intake and route to `troubleshoot-grow.md`; do not imply image analysis happened.

## Hard Rules

1. **Never single-answer from a photo.** Always rank top 3 possibilities.
2. **Reject purple/blurple LED photos.** Demand white light or daylight retake.
3. **Skip diagnosis if intake checklist incomplete.** Ask first, diagnose second.
4. **Cite confidence level explicitly** in every diagnostic response.

## Procedure

### Pass 0 — Photo Quality Gate

Before analyzing content, check:

| Check | Action if fails |
|---|---|
| Lighting (white/daylight, not purple LED) | Request retake under phone flashlight, sunlight, or with light briefly switched to white mode |
| Focus (issue area sharp) | Request closer, focused shot |
| Coverage (whole plant + close-up of issue) | Request both shots — context AND detail |
| Underside of leaf visible (for pest/spotting) | Request leaf-flip photo |
| Trichome shots in macro (for harvest readiness) | Request jeweler's loupe or macro lens shot |

If gate fails → respond with what's needed, do NOT proceed.

### Pass 1 — Whole Plant Context

Identify from the wide shot:
- Stage (seedling / veg / early flower / mid flower / late flower / ripening)
- Overall structure (healthy bushy / stretched / stunted / wilted / drooping / clawing)
- Color uniformity (whole plant affected vs localized)
- Position of issue (lower / middle / upper canopy → mobile vs immobile nutrient hint)
- Substrate visible? (soil/coco/hydro indicators)

### Pass 2 — Issue Close-Up Analysis

For the close-up shot, document:
- Color (yellow / brown / purple / red / black / white / pale)
- Pattern (interveinal / margin / tip / spotting / blotching / streaking)
- Distribution (one leaf / one branch / whole plant / new growth / old growth)
- Texture (crispy / mushy / waxy / fuzzy / spotted / glossy)
- Underside (pests, eggs, mold, mildew)
- Stem/petiole color and condition
- Any pests visible (size, color, movement, webbing, frass, honeydew)

### Pass 3 — Cross-Reference Knowledge

Load relevant knowledge files based on Pass 2 findings:

| Pass 2 indicator | Load |
|---|---|
| Yellowing, color changes, pattern issues | `knowledge/07-deficiencies.md` |
| Spots, fuzz, mildew, rot | `knowledge/09-disease.md` |
| Pests visible, webbing, eggs, damage holes | `knowledge/08-pests.md` |
| Wilting/drooping with no color change | `knowledge/04-medium-*.md` (watering issue) |
| Burnt tips, clawing, dark green | `knowledge/06-nutrients-*.md` (toxicity) |
| Heat/light stress (taco, bleach, foxtail) | `knowledge/02-environment.md` + `knowledge/03-lighting.md` |

Cross-reference against `state/grow-context.md`:
- Recent feed changes?
- Environment within range for stage?
- Stage matches symptom timing?

### Pass 4 — Generate Ranked Differential

Output exactly this structure:

```
DIAGNOSIS — Confidence: [HIGH / MEDIUM]

Top 3 possibilities (ranked):

1. [MOST LIKELY CAUSE] — [X]% confidence
   Why: [evidence from photo + grow context]
   Confirms it: [specific test/check]
   Rules it out: [specific finding]
   
2. [SECOND POSSIBILITY] — [Y]% confidence
   Why: [evidence]
   Confirms it: [test]
   Rules it out: [finding]

3. [THIRD POSSIBILITY] — [Z]% confidence
   Why: [evidence]
   Confirms it: [test]
   Rules it out: [finding]

ROOT CAUSE INVESTIGATION:
Even if symptom is X, check Y first because [pH/water/genetics often underlying].

IMMEDIATE ACTION (low-risk, high-value):
[1-3 steps that don't risk making it worse]

DO NOT DO YET:
[Reactive moves to avoid until cause confirmed — e.g., don't flush, don't add Cal-Mg blindly]

CONFIRM-OR-PIVOT IN 24-72H:
- If [outcome A] → confirmed #1, proceed with [treatment]
- If [outcome B] → pivot to #2
- If worse → escalate, post update photo
```

### Pass 5 — State Update

`grow-context.md`:
- `last_updated`: today
- `last_updated_by`: agent
- `source_workflow`: diagnose-from-photo
- Update `issue_1` (or next available `issue_N` slot) with short description + status (active / monitoring / resolved)

`grow-log.md` append:
```
## [DATE] — [stage] — Issue: [short description]
Source workflow: diagnose-from-photo (visual diagnosis)
Photo quality: [pass — white light / focus / coverage / underside or macro details]
Confidence: [HIGH / MEDIUM]
Top diagnosis: [#1 possibility]
Top 3 considered: [#1 / #2 / #3]
Action plan: [user's chosen action]
Follow-up: [recheck date]
```

Show the draft entry to the user for confirmation before saving (per `grow-context.md` Schema Rule 6 — diff-before-save). Do not update silently on first entry.

If user is just exploring or didn't accept any action → no state update; offer to log later.

## Pitfalls

| Pitfall | Prevention |
|---|---|
| Purple LED photo making yellow look brown | Reject + request white light |
| Diagnosing pH lockout as deficiency | Always check pH/EC runoff before naming a deficiency |
| Confusing N toxicity (clawing) with overwatering (drooping) | Check leaf rigidity + soil moisture, not just shape |
| Calling early flower foxtailing "heat stress" on pure sativa | Check genetics — sativas naturally foxtail |
| Misreading silica spots as PM | PM is fuzzy + spreads; silica is dry + isolated |
| Treating septoria as nute issue | Septoria = round brown spots with yellow halo, lower leaves first |
| Confirming bias (locking in first hypothesis) | Force ranking 3 possibilities every time |
| Missing HLVd (looks like generic stunting + leaf deformity) | If multiple plants from clones show stunting + duck-foot leaves → suspect HLVd, recommend testing |

## Verification

Before sending the diagnosis:
- [ ] Photo quality gate passed?
- [ ] Top 3 possibilities ranked with confidence %?
- [ ] Each possibility has confirm-it AND rule-it-out criteria?
- [ ] Immediate action listed AND it's low-risk?
- [ ] "Do not do yet" list included?
- [ ] Follow-up timing specified?
- [ ] `grow-context.md` state-write fields set (`last_updated`, `last_updated_by: agent`, `source_workflow: diagnose-from-photo`)?
- [ ] `grow-context.md` `issue_N` slot updated with short description + status?
- [ ] `grow-log.md` entry drafted for user confirmation before save?

If any check fails → fix before responding.

## References

- Knowledge:
  - `knowledge/07-deficiencies.md` — color/pattern symptoms
  - `knowledge/08-pests.md` — pest patterns
  - `knowledge/09-disease.md` — disease patterns
  - `knowledge/02-environment.md`, `knowledge/03-lighting.md` — heat/light stress
  - `knowledge/04-medium-*.md` — medium-specific watering symptoms
  - `knowledge/06-nutrients-synthetic.md`, `knowledge/06-nutrients-organic.md` — nutrient toxicity
  - `knowledge/21-troubleshooting-tree.md` — symptom routing branches
- Workflows:
  - `troubleshoot-grow.md` — text-only counterpart for non-photo cases
- State (exact field names referenced):
  - `grow-context.md` → `current_stage`, `medium`, `issue_1`/`issue_2`/`issue_3`, plus all intake-relevant fields
  - `grow-log.md` → append-only diagnostic entry per Pass 5
- Rules:
  - `SKILL.md` Rule 2 — confidence framework (HIGH/MED/LOW; LOW is not a diagnosis)
  - `SKILL.md` Rule 3 — intake checklist (mandatory before diagnosis)
  - `SKILL.md` Rule 5 — source hierarchy
  - `SKILL.md` Rule 6 — preview required for initial/durable diagnostic state writes; later low-risk updates summarized at session end
  - `grow-context.md` Schema Rule 6 — diff-before-save on initial state writes
