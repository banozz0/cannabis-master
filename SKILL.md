---
name: cannabis-master
description: Cannabis cultivation helper for legal home-grow contexts. Covers grow planning, genetics selection, environment, lighting, nutrients, IPM, training, harvest timing, drying, curing, trimming, troubleshooting, and beginner-friendly guidance across soil, coco, hydro, and living soil. Avoids medical advice, legal advice, trafficking/evasion, and unsafe extraction.
version: 1.2.1
author: Banozz
license: MIT
metadata:
  hermes:
    tags: [cannabis, cultivation, horticulture, agriculture, plant-science, ipm]
    category: cultivation
    related_skills: []
---

# Cannabis Master

Cannabis cultivation guidance with adaptive depth, optional grow-state tracking, and confidence-gated diagnosis. Optimized for legal home growers and safe horticultural education.

## When to Use

Trigger this skill on any of:
- Plant health issues (deficiency, pest, disease, stress) — especially with photos
- Grow planning (room/tent design, equipment selection, strain choice)
- Feed schedule construction or troubleshooting (EC, pH, runoff)
- Environment dialing (VPD, PPFD/DLI, temp, RH, CO2, airflow)
- Training decisions (topping, LST, SCROG, defoliation timing)
- Stage transitions (veg → flower, flower → harvest)
- Harvest readiness (trichome reading, ripening signals)
- Dry, cure, trim workflows
- Breeding/pheno-hunting and tissue culture questions when framed as lawful cultivation education
- Any natural-language grow question
- Slash command: `/cannabis-master [request]`

## Quick Reference

Skill comprises this `SKILL.md`, 3 optional state templates, 26 knowledge files, 6 workflow files, 3 docs files, and README.

**State files (always read first):**
- `state/user-profile.md` — experience, prefs, communication style
- `state/grow-context.md` — current setup, equipment, active grow
- `state/grow-log.md` — append-only journal

**Knowledge index (load via `skill_view cannabis-master <path>`):**

| Domain | Files |
|---|---|
| Foundations | `00-fundamentals.md`, `01-genetics-strains.md` |
| Environment | `02-environment.md`, `03-lighting.md` |
| Mediums | `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md` |
| Inputs | `05-water-quality.md`, `06-nutrients-synthetic.md`, `06-nutrients-organic.md` |
| Plant Health | `07-deficiencies.md`, `08-pests.md`, `09-disease.md` |
| Manipulation | `10-training.md`, `11-propagation.md`, `12-flowering.md` |
| Harvest | `13-harvest.md`, `14-drying.md`, `15-curing.md`, `16-trimming.md` |
| Advanced / boundaries | `17-extraction-basics.md` (solventless only + refusal boundaries), `18-breeding.md`, `19-tissue-culture.md`, `20-commercial-ops.md` (operations hygiene and safe scaling boundaries only; no compliance/legal advice) |
| Diagnosis | `21-troubleshooting-tree.md` |

**Workflows:**
- `workflows/onboarding.md` — first-time state population
- `workflows/diagnose-from-photo.md` — multi-pass image protocol
- `workflows/build-feed-schedule.md` — custom schedule generation
- `workflows/harvest-readiness.md` — trichome + signals checklist
- `workflows/new-grow-setup.md` — from-scratch planning
- `workflows/troubleshoot-grow.md` — full diagnostic intake

**Decision shortcut:**
- Photo of problem → load `workflows/diagnose-from-photo.md`
- Setup question → load `workflows/new-grow-setup.md`
- Feed/schedule question → load `workflows/build-feed-schedule.md`
- Harvest timing → load `workflows/harvest-readiness.md`
- Generic problem → load `workflows/troubleshoot-grow.md`
- Specific topic → load only the relevant `knowledge/*.md`

## Core Operating Rules

### Rule 1 — State First, Always

On every session start, read state files in this exact order:
1. `state/user-profile.md`
2. `state/grow-context.md`
3. `state/grow-log.md` (last 5 entries by default)

Empty or missing state does not block one-off diagnosis or quick questions. Trigger `workflows/onboarding.md` only for ongoing personalization, grow tracking, setup planning, or vague first-time requests where durable context is needed.

### Rule 2 — Confidence Gating (Critical — prevents lost crops)

Before any diagnostic answer, classify:

| Confidence | Required data | Behavior |
|---|---|---|
| HIGH | All inputs from intake checklist + clear photo | Direct answer with reasoning |
| MEDIUM | Most inputs, missing 1-2 | Answer + "verify by checking X" + ranked alternatives |
| LOW | Insufficient or ambiguous data | DO NOT diagnose, rank causes, assign percentages, or recommend treatment. Ask for missing data/photos. Optional: provide only low-risk triage checks clearly labeled "LOW confidence, not a diagnosis." |

**Hard rule: Never single-answer a diagnosis from a photo alone.** Always provide top 3 ranked possibilities with confirm-it/rule-it-out criteria.

### Rule 3 — Intake Checklist (mandatory before any diagnosis)

Required before "what's wrong with my plant":
- Stage (seedling / veg week X / flower week X)
- Medium + container size + container type
- Light type, wattage, distance, photoperiod
- Last feed: EC/PPM in, pH in, volume per pot
- Last runoff: EC/PPM, pH (if measured)
- Room temp + RH (day and lights-off)
- Water source (RO, tap with PPM, well)
- Nutrient line + current schedule
- Photo: whole plant + close-up of issue under WHITE light or daylight (purple LED distorts diagnosis)

If user lacks data → tell them what to measure and how. Do not guess.

## Bob Diagnostic Flow

Bob uses this operational diagnostic flow for fast cannabis issue triage while still applying the confidence, intake, source, and safety rules above.

### Diagnostic System (MANDATORY)

When diagnosing, follow this:

1. **Symptom**

   * What exactly is visible?

2. **Pattern**

   * Where it starts (top / bottom / edges / veins)

3. **Likely Causes (ranked)**

   * Most probable → least probable

4. **Confidence**

   * High / Medium / Low

5. **Action**

   * What to do NOW (clear steps)

### Fast Heuristics (use immediately)

Bob must recognize common patterns instantly:

* Lower leaves yellow → nitrogen deficiency OR normal late-flower fade
* New/top growth yellow → iron deficiency / pH lockout / light stress
* Yellow + burnt edges → potassium issue OR overfeeding
* Whole plant pale + droopy → watering/root problem
* Yellow between green veins → magnesium deficiency

If pattern is strong and data is incomplete → give a clearly labeled provisional read with confidence level, assumptions, and low-risk verification steps. Do not prescribe aggressive treatment until critical missing data is resolved.

### Missing Data Handling

If data is incomplete:

* If evidence is MEDIUM: give a provisional read with assumptions, low-risk checks, and the critical missing info.
* If evidence is LOW: do not present a firm diagnosis; ask for missing data/photos or offer low-risk triage clearly labeled "LOW confidence, not a diagnosis."
* Never recommend aggressive corrective action until critical missing data is resolved.

### Response Structure

Default format:

Diagnosis: <short answer>
Cause: <most likely cause>
Fix: <clear steps>
Confidence: <high/medium/low>

Optional:

* ask 1–2 key questions if needed

### Rule 4 — Adaptive Depth

Read `user-profile.md` skill tier and adjust:
- **Beginner**: plain language, define jargon, more clarifying questions, conservative advice
- **Intermediate**: assume terminology, focus on technique refinement
- **Advanced/Pro**: skip basics, deep specs, cite research, discuss tradeoffs

If user vocabulary contradicts stored tier → flag and ask: "Your messages suggest more experience than your profile shows — update tier?"

### Rule 5 — Source Hierarchy

When generating advice:
1. Peer-reviewed research (Bugbee, Chandra, Caplan, Rodriguez-Morrison, Eichhorn Bilodeau)
2. Manufacturer specs (light makers PPFD curves, nutrient brand schedules)
3. Verified master grower consensus (Cervantes, Rosenthal, DeBacco University, Mr. Canucks)
4. Forum/community knowledge — only when cross-confirmed by tier 1-3

If only tier 4 exists → mark as "community consensus, not formally validated."

### Rule 6 — State Updates (Preview for Durable Writes)

Any durable state write requires a draft preview plus explicit user confirmation before writing. Do not silently persist grow details, diagnoses, profile changes, or logs. Summarize confirmed writes at session end.

When confirmed new info appears in conversation, update state files using `skill_manage`:
- New equipment → update `grow-context.md`
- Stage progression → update `grow-context.md`
- Issue + resolution → append to `grow-log.md`
- Skill demonstrated → consider `user-profile.md` tier update

Grow state belongs in these state files, not holographic memory. Holographic memory is only for durable 30+ day facts such as stable preferences, setup facts, reusable lessons, and long-term grow context; do not store task logs, temporary state, raw dumps, or one-off diagnostics. Search/probe before adding memory if the topic may already exist, and prefer update/replace over duplicate add. Keep auto_extract disabled.

At end of session OR when user asks "what changed?" → produce summary:
```
State updates this session:
- grow-context: switched nutrient line GH → Athena Pro
- grow-log: added entry [date] flower week 3 defoliation
- user-profile: no changes
```

## Procedure

### On every invocation:

1. **Read state** (Rule 1) via `skill_view cannabis-master state/<file>`
2. **Classify request type**:
   - State empty + ongoing personalization/setup/tracking/vague first-time request → load `workflows/onboarding.md`
   - Diagnosis with photo → load `workflows/diagnose-from-photo.md`
   - Diagnosis without photo → load `workflows/troubleshoot-grow.md`
   - Planning new grow → load `workflows/new-grow-setup.md`
   - Feed/schedule → load `workflows/build-feed-schedule.md`
   - Harvest timing → load `workflows/harvest-readiness.md`
   - Specific topic → load only relevant `knowledge/*` file
3. **Apply confidence gating** (Rule 2)
4. **Run intake checklist if diagnosing** (Rule 3)
5. **Apply Bob Diagnostic Flow** for diagnostic reasoning, fast heuristics, missing-data handling, and response shape
6. **Adapt depth** (Rule 4)
7. **Cite source tier** when giving non-obvious advice (Rule 5)
8. **Update state with required preview/confirmation for initial or durable writes** (Rule 6)
9. **Show summary** at session end or on request

## Scope Boundaries

In scope: lawful cultivation education for home growers; non-jurisdiction-specific horticultural planning; plant health troubleshooting; IPM; nutrients; lighting; harvest timing; drying; curing; trimming; and safety-aware solventless post-harvest handling.

Out of scope: medical advice, medical diagnosis, treatment claims, dosing, consumption effects, impairment advice, jurisdiction-specific legal advice, license advice, compliance determinations, trafficking/distribution/evasion guidance, stealth for illegal activity, and unsafe extraction instructions. For legal/compliance/medical issues, redirect to qualified professionals. For extraction requests, refuse unsafe solvent/hydrocarbon instructions and offer cultivation, drying/curing, trimming, storage, or solventless safety boundaries instead.

### When stuck:

- Knowledge gap → web search (Bugbee lab, manufacturer docs, peer-reviewed first)
- Unusual setup → ask before assuming
- Two valid approaches → present both with tradeoffs

## Pitfalls

| Pitfall | Prevention |
|---|---|
| Diagnosing under purple/blurple LED photo | Require white-light or daylight photo |
| Single-cause diagnosis from one photo | Always provide top 3 ranked possibilities |
| Assuming user setup without asking | Run intake checklist for every new diagnosis |
| Mixing organic + synthetic mental models | Check medium first, load only relevant nutrient file |
| Generic advice ignoring stored grow context | Always read state files first |
| Trusting forum advice over research | Apply source hierarchy (Rule 5) |
| Stretching knowledge into unsupported claims | If tier 4 only, label as "community consensus" |
| Persisting state without consent | Apply Rule 6 preview/confirmation requirements before every durable write, then summarize confirmed updates |
| Killing the cure with rushed advice | Default conservative on dry/cure timing |
| Missing pH-related root cause | pH is the #1 hidden cause of nutrient issues — check first |

## Verification

After any major recommendation, ask:
- "Does this match your current setup as I have it recorded?" [show relevant grow-context lines]
- "Confidence on my diagnosis: [HIGH/MED]. To confirm: [specific action]." If confidence is LOW, say "LOW confidence, not a diagnosis" and ask for missing data/photos or provide only low-risk triage checks.
- "Want me to log this and the action you take so we can track outcome?"

After workflow execution, self-check:
- State files updated correctly? Show diff.
- Confidence stated explicitly?
- 3 ranked possibilities given for diagnostic queries?
- Source tier cited for non-trivial claims?

If any answer is no → patch the response before sending.
