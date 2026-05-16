# User Profile

Slow-changing facts about the user — experience, skill tier, preferences, and how they like to be coached. Distinct from `grow-context.md` (which tracks the *current grow*) and `grow-log.md` (which tracks *what happened*). This file shapes how every response is written.

The agent updates this file only after showing a draft and receiving explicit user confirmation, then summarizes confirmed changes at session end (per SKILL.md Rule 6). Tier should be re-evaluated every ~5 sessions or after a major demonstration of skill.

**Format:** Markdown with key:value pairs inside fenced sections. Empty values = `[unset]`. Update fields, don't restructure.

---

last_updated: [unset]
last_updated_by: [unset — agent or user]
source_workflow: [unset]

## Identity & Background

```
display_name: [unset]              # what to call the user (first name, handle, leave blank)
general_background: [unset]        # vegetable gardener / hobbyist hydro / horticulture pro / new to plants entirely / other
formal_training: [unset]           # any horticulture/ag/botany degree, certs, or courses (Green Flower, HACC, Bugbee MOOC, etc.)
languages: [unset]                 # primary + any others useful for sourcing material
home_region: [unset]               # mirror of grow-context if relevant; e.g. Malta — hot dry summer, mild humid winter
```

## Skill Tier

```
self_assessed_tier: [unset]        # beginner / intermediate / advanced / commercial — what user told us
agent_assessed_tier: [unset]       # what the agent infers from vocabulary, technique, questions asked
tier_evidence: [unset]             # 1-2 lines of why (e.g. "discusses VPD math, runs Athena Pro, asked about reversal" → advanced)
last_tier_review_date: [unset]     # YYYY-MM-DD of last reassessment
```

**Tier definitions (for the agent — do not edit):**
- **beginner** — 0–2 grows, still learning fundamentals (pH, EC, light, watering). Define jargon. Conservative advice. Expect basic questions.
- **intermediate** — 3–10 grows, comfortable with terminology, dialed environment, refining technique. Skip the basics, focus on optimization.
- **advanced** — 10+ grows across multiple cycles, may pheno-hunt, runs measured environment (PPFD/VPD), comfortable with research-level data and tradeoffs.
- **commercial** — production-scale or aspiring, batch tracking, SOPs, multi-room or multi-strain pipelines, may breed or run R&D. Talk specs, don't handhold.

## Experience

```
years_growing: [unset]             # whole years
total_grows_completed: [unset]     # finished cycles only (harvested, dried, cured)
grows_in_progress: [unset]         # active cycles right now (mirror of grow-context summary)
indoor_grows: [unset]              # count
outdoor_grows: [unset]
greenhouse_grows: [unset]
best_outcome: [unset]              # short note: yield + quality + strain + when (e.g. "Wedding Cake, 2.1 g/W, 2025-Q3")
worst_outcome: [unset]             # what went wrong + lesson (e.g. "PM in week 6 — humidity not controlled")
most_recent_harvest: [unset]       # date + outcome summary
```

## Medium Experience

```
soil_grows: [unset]                # count + brands used (FFOF, Pro-Mix, custom)
coco_grows: [unset]                # count + brand (Canna, Coco Bliss, brick form)
dwc_grows: [unset]                 # single bucket
rdwc_grows: [unset]                # recirculating
nft_grows: [unset]
ebb_flow_grows: [unset]
aero_grows: [unset]                # true aero or HPA
living_soil_grows: [unset]         # no-till
```

## Confidence Areas

User has demonstrably solved or executed these — agent can speak shorthand here.

```
strong_in: [unset]                 # comma list — e.g. topping/LST, harvest timing, drying RH, pH calibration, IPM scouting
notable_wins: [unset]              # specific things user has done well (e.g. "ran 9-week cure successfully")
techniques_mastered: [unset]       # mainline, SCROG, defol, super-cropping, etc.
```

## Knowledge Gaps & Weak Areas

Track these so the agent slows down and explains rather than assumes.

```
weak_in: [unset]                   # comma list — e.g. hydroponic chemistry, pheno selection, breeding genetics
recurring_struggles: [unset]       # patterns user keeps hitting (e.g. "always overfeeds in early flower")
unfamiliar_with: [unset]           # never used — e.g. CO2 supplementation, tissue culture, rosin pressing
explain_extra_carefully: [unset]   # topics where user explicitly asked for more handholding
```

## Cultivation Preferences

```
nutrient_philosophy: [unset]       # synthetic / organic / hybrid / KNF / living-soil-only
training_philosophy: [unset]       # low-stress only / aggressive HST / SCROG always / let-it-grow / mainline
yield_vs_quality_bias: [unset]     # max-yield / balanced / max-quality / max-terps
automation_preference: [unset]     # full manual / hand-watering only / partial automation / fully automated
photoperiod_vs_auto: [unset]       # photo-only / autos-only / both
seed_vs_clone: [unset]             # seed-only / clone-only / both
indoor_vs_outdoor: [unset]         # indoor / outdoor / mixed
strain_preferences: [unset]        # indica-leaning / sativa-leaning / hybrid / specific cannabinoids/terps
breeding_interest: [unset]         # none / curious / S1s / open pollination / serious breeder
```

## Communication Style

This section drives how the agent writes every response.

```
preferred_response_length: [unset] # terse / standard / detailed
jargon_tolerance: [unset]          # define-everything / mixed / use-freely
units_general: [unset]             # metric / imperial / both (specify which)
temperature_units: [unset]         # C / F
distance_units: [unset]            # cm / inches
volume_units: [unset]              # L / gal
ec_or_ppm: [unset]                 # EC / PPM-500 / PPM-700 — match user's meter
explain_reasoning: [unset]         # always / on-request / minimal
ask_clarifying_questions: [unset]  # always / when-confidence-low / minimize-questions
push_back_when_wrong: [unset]      # yes / soft / no — does user want direct disagreement
table_vs_prose: [unset]            # tables-preferred / prose-preferred / mixed
emoji_ok: [unset]                  # yes / no — default no
profanity_ok: [unset]              # yes / no — default no
```

## Tools & Brands Familiar

Different from `grow-context` which holds the *current* gear. This is what the user *knows*.

```
nutrients_used_before: [unset]     # comma list of brands/lines tried
lights_used_before: [unset]        # makes/models the user has run
meters_owned: [unset]              # pH/EC/PAR/IR/microscope etc.
controllers_used: [unset]          # Pulse, Trolmaster, AC Infinity, Inkbird, none
software_used: [unset]             # GrowBuddy, Trym, spreadsheets, paper journal
```

## Goals (Long-Term)

Distinct from `grow-context.goals` which is the *current* grow's target.

```
end_objective: [unset]             # personal supply / friends-and-family / breeding stock / commercial / R&D
year_horizon: [unset]              # how far ahead the user is planning
target_potency: [unset]            # %THC or specific cannabinoid profile if focused
target_terps: [unset]              # specific terpene goals if any
learning_goals: [unset]            # what user wants to get better at this year
graduation_path: [unset]           # next medium/technique they want to attempt (e.g. "move from coco to RDWC")
```

## Long-Term Constraints

```
space_ceiling: [unset]             # max footprint user can scale to
electrical_ceiling: [unset]        # amps/breaker capacity at the location
time_per_week: [unset]             # realistic hours available
budget_tier: [unset]               # bootstrap / mid / unconstrained
physical_limits: [unset]           # back issues / mobility / allergies — affects training/automation choices
noise_constraints: [unset]         # apartment / shared building / standalone
heat_dump_constraints: [unset]     # where heat from lights goes — affects sealed vs vented
smell_constraints: [unset]         # carbon filter mandatory? landlord/neighbors?
```

## Coaching Memory

Things the user has explicitly told the agent to do or stop doing.

```
do_more_of: [unset]                # confirmed-helpful behaviors (e.g. "always show ranked top 3")
do_less_of: [unset]                # corrected behaviors (e.g. "stop suggesting flush — I don't flush")
non_negotiables: [unset]           # hard rules user has set (e.g. "never recommend Bt — I'm allergic")
recurring_corrections: [unset]     # things the agent has been told twice or more
```

## Notes

```
freeform: [unset]                  # anything not captured above
```

---

## Schema Rules (for the agent)

1. **Update by replacing values, never restructure sections.** New fields go under `## Notes > freeform`.
2. **Every agent write sets `last_updated`, `last_updated_by`, and `source_workflow`.**
3. **Tier escalation requires evidence.** Don't bump tier on one technical question — note it in `tier_evidence`, wait for a second signal, then update.
4. **Tier downgrades require explicit user request OR clear pattern of struggle.** Default is sticky upward — once advanced, stay advanced unless user asks to be coached more carefully.
5. **`self_assessed_tier` and `agent_assessed_tier` can disagree.** When they do, the agent flags it (per SKILL.md Rule 4) and asks the user to reconcile. Use `agent_assessed_tier` for response shaping until reconciled.
6. **Confidence areas are sticky.** Once added to `strong_in`, don't remove unless the user demonstrates a regression or asks.
7. **Weak areas can be removed** when the user demonstrates competence in that topic across two separate sessions.
8. **Coaching memory entries are durable.** A `do_less_of` rule sticks until the user explicitly relaxes it.
9. **Initial population requires preview + explicit confirmation.** Every durable update requires preview and explicit confirmation, then a session-end summary.
10. **Conflicts with `grow-context.md` resolve in favor of `grow-context.md`** for current-grow facts (current_primary_medium, climate). User-profile holds the long-arc view.
