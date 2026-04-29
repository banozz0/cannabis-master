# Workflow: Onboarding

First-time state population. Triggered when state files are empty/missing or when the user explicitly asks for setup. Establishes `user-profile.md` (tier, communication style, goals) and optionally `grow-context.md` (active grow setup) so future sessions have persistent context.

This workflow runs BEFORE any grow advice when state is empty (per `SKILL.md` Rule 1). For one-off questions, skip the full onboarding and offer light onboarding at the end.

## When to Use

- State files (`user-profile.md` and/or `grow-context.md`) are empty or missing
- User explicitly says "set me up" / "I'm new here" / "start over" / "remember me"
- User vocabulary contradicts stored tier (after a session, user demonstrates clearly higher or lower expertise) — trigger a partial onboarding to update tier
- User mentions they're starting a fresh grow and previous state is now stale

## Hard Rules

1. **Don't onboard for one-off casual questions.** If user asks "is this a calcium deficiency?", answer the question (with confidence gating). Offer onboarding at the end if they want ongoing context.
2. **Never force the full intake checklist as part of onboarding.** Intake is for diagnosis (`SKILL.md` Rule 3); onboarding is for state. Different purpose, different fields.
3. **Match depth to user's apparent commitment.** Casual visitor → minimal. Active grow user wanting ongoing help → full.
4. **Show the user the state diff before saving.** They must be able to spot bad updates (per `grow-context.md` Schema Rule 6).
5. **Don't re-ask fields the user already provided in conversation.** Pull from message context first.
6. **Update state silently after onboarding completes.** Summarize at session end (per `SKILL.md` Rule 6).
7. **Allow skips.** User can say "skip that section" or "I don't have that yet" — mark `[unset]` and move on.

## Procedure

### Pass 0 — Decide whether to onboard at all

Map user's first message intent to onboarding depth.

| User said | Action |
|---|---|
| "I'm new to growing, where do I start?" | FULL onboarding |
| "I want to plan a tent setup" | LIGHT onboarding → then `workflows/new-grow-setup.md` |
| "What's wrong with my plant?" (with photo or symptom) | SKIP onboarding; run `workflows/diagnose-from-photo.md` or `workflows/troubleshoot-grow.md`; offer light onboarding at end |
| "Quick question about [specific topic]" | SKIP onboarding; answer; offer at end |
| "Help me track my grow ongoing" / "remember my setup" | FULL onboarding |
| First-time interaction with empty state, vague question | LIGHT onboarding (enough for adaptive depth) |
| Returning user with empty state (rare — corruption?) | Confirm, then FULL onboarding |

If SKIP: answer the question, then add at the end:
> "If you'd like me to remember your setup so we can pick up where we left off next time, just say 'set me up'."

### Pass 1 — Establish skill tier

Detect from user's first messages:
- **Beginner:** "I'm new", asks for basic term definitions, simple framing, no jargon
- **Intermediate:** uses common terms (EC, VPD, flip, runoff), specific equipment names, mid-complexity questions
- **Advanced/Pro:** deep terms (chelated micros, photoperiod manipulation, IBL, light recipe), commercial scale, technical citations or references

If unclear, ask directly:
> "Quick check on experience level so I can pitch responses right:
> - First grow / never grown
> - A few grows under my belt
> - Years of experience
> - Professional / commercial"

Don't lock in — note the tier and re-evaluate as the conversation continues.

### Pass 2 — Determine onboarding depth

Three levels:

**A. CASUAL** (one-off question, doesn't want ongoing context)
- Skip state population entirely
- Answer their actual question
- One-line offer at end about future onboarding

**B. LIGHT** (planning or learning, no current grow yet)
- Populate `user-profile.md`
- Skip `grow-context.md` until they have an actual grow
- Set communication preferences
- Route to relevant planning workflow

**C. FULL** (active grow, wants ongoing help)
- Populate `user-profile.md`
- Walk through `grow-context.md` sections
- Establish baselines for current grow
- Optionally seed `grow-log.md` with first entry summarizing current state
- Route to next useful workflow (diagnose, feed-schedule, harvest-readiness, etc.)

### Pass 3 — User profile population (LIGHT or FULL)

Walk through `user-profile.md` fields. Group questions by section, not field-by-field. Examples:

**Experience block:**
> "How many grows have you completed, roughly? And what mediums have you used — soil, coco, hydro, living soil, or a mix?"

**Strengths/weaknesses block:**
> "What do you feel solid on already, and where would you most like the help? E.g., some growers are dialed on environment but shaky on feed schedules, or comfortable with veg but always lose plants in late flower."

**Goals block:**
> "What's the goal here — personal supply, learning, breeding, commercial scale, or something else? Any specific yield, quality, or cannabinoid targets?"

**Constraints block:**
> "Any constraints I should know about — space, electricity, budget, time available?"

After each block, paraphrase what you heard to confirm before writing to state.

### Pass 4 — Communication preferences

Ask explicitly (don't infer):

> "Three quick preferences so I match your style:
> 1. Plain language or technical (jargon OK)?
> 2. Short answers or thorough?
> 3. Metric or imperial units (or both)?"

Optional:
- Always cite sources, or skip citations unless asked
- Offer photo diagnosis proactively, or only when asked
- Want alerts for state updates, or silent updates with end-of-session summary only

### Pass 5 — Grow context population (FULL only)

Only if user has an active grow OR is planning one with concrete equipment in hand. Walk through `grow-context.md` sections in this order (matches the schema layout):

1. **Space** (tent/room size, ceiling height, external climate)
2. **Lighting** (fixture, wattage, photoperiod, schedule)
3. **Climate control** (temp/RH targets, fans, AC, dehumid)
4. **Sensors** (controller, pH/EC meters, microscope)
5. **Medium & containers** (medium, brand, pot size, container type, plant count)
6. **Water source** (RO/tap/well, input PPM/EC, alkalinity)
7. **Nutrient line** (brand, schedule, silica, Cal-Mg, beneficials)
8. **Current feed regimen** (brand schedule followed Y/N, feed frequency, last-feed date)
9. **Active grow** (strain, seed/clone, photo/auto)
10. **Stage tracking** (current stage, dates)
11. **Training** (techniques used, top count, defoliation history)
12. **Active issues** (anything bothering them now)
13. **Goals** (priority for this specific grow)

Don't demand all fields at once. Walk in 2-3 section chunks. User can say "skip" — mark `[unset]`.

If user is mid-grow and missing data they could measure (runoff pH/EC, room VPD), tell them what to measure and when, but don't block onboarding on it.

### Pass 6 — Show diff and confirm

Before writing, show a draft of what will be saved. Format:

```
About to write to user-profile.md:
- experience: 3 grows completed
- mediums_used: coco, soil
- skill_tier: intermediate
- communication_style: concise, technical, metric
- goals: yield + quality, breeding interest down the road
- constraints: 4x4 tent in spare room, $200/month budget

About to write to grow-context.md:
- space: 4x4 tent, indoor spare room, Mediterranean climate
- lighting: AC Infinity Ionframe Evo 8, 730W, 18/6 veg
- medium: coco-perlite 70/30, 5gal fabric pots, 4 plants
- nutrient line: Athena Pro full schedule
- water source: RO + Cal-Mg
- current stage: veg week 3, no active issues

Looks right? Reply 'save' to write, or correct anything and I'll redo."
```

Wait for explicit confirmation. Then write.

### Pass 7 — Save state and summarize

Use `skill_manage` to write to state files. Set `last_updated` to today's date, `last_updated_by` to `agent` (per schema enum), and `source_workflow` to `onboarding`.

Final session summary:

```
Onboarding complete. Saved:
- user-profile.md: tier=intermediate, 3 grows experience, coco+soil background, prefers concise/technical/metric
- grow-context.md: 4x4 indoor tent, Ionframe Evo 8, coco-perlite, Athena Pro, week 3 veg
- grow-log.md: first entry seeded with current snapshot

Suggested next step: [route based on context]
- "Want me to build you a feed schedule for the rest of veg and into flower?" → workflows/build-feed-schedule.md
- "Want me to dial in your VPD targets?" → 02-environment.md
- "Want to set up a diagnose-on-demand habit? Send a photo any time and I'll run the protocol." → workflows/diagnose-from-photo.md
```

End with a single concrete suggestion, not a menu of five.

## Output Format

Onboarding response template:

```
[Welcome — 1 line, set tone matched to detected tier]

[Pass 0 intent check — 1 line confirming what user wants]

[Pass 1-2 tier and depth question if needed]

[Pass 3 profile block questions — 2-3 at a time]

[Pass 4 preferences questions]

[Pass 5 grow context blocks if FULL — 2-3 sections at a time, never all 13 at once]

[Pass 6 diff preview — show what will be saved]

[Confirmation prompt]

[Pass 7 summary after save with one suggested next step]
```

For LIGHT onboarding, skip Pass 5; everything else applies.
For CASUAL skip, only do Pass 0 closing line.

## State Updates

After onboarding, write:

- `user-profile.md` — always (unless CASUAL skip)
- `grow-context.md` — only if FULL onboarding with active or imminent grow
- `grow-log.md` — only if user wants to seed first entry now

Always set:
- `last_updated: [today's date in YYYY-MM-DD]`
- `last_updated_by: agent` (schema enum: `agent` or `user`)
- `source_workflow: onboarding`

Per `grow-context.md` Schema Rule 6: never silent on initial population. Show diff before save.

After this first save, subsequent updates can be silent with end-of-session summary (per `SKILL.md` Rule 6).

## Pitfalls

| Pitfall | Prevention |
|---|---|
| Onboarding a user who just wanted a quick answer | Pass 0 decision tree; default to SKIP for diagnosis or one-off questions |
| 30 questions before the first answer | Walk in section chunks (2-3 fields per question); user can skip any block |
| Locking tier to "beginner" because of one casual question | Re-evaluate from full conversation; ask explicitly if unsure |
| Saving without showing diff | Hard Rule 4 — always preview before write |
| Demanding equipment specs the user doesn't have | Mark `[unset]`, not "data missing, can't proceed" |
| Confusing onboarding with intake checklist | Onboarding = state population (long-lived). Intake = diagnosis prep (per-question). Don't mix. |
| Forgetting to update last_updated fields | Always set on every write |
| Walking through grow-context for a user without an active grow | LIGHT onboarding only — skip section until they have a setup |
| Onboarding in a way that ignores prior context | If user already mentioned tent size or strain in their opening, don't re-ask — confirm and move on |
| Making the first session feel like a form | Conversational tone, group fields, allow skips, paraphrase before saving |
| Stale state from prior grow → new grow contamination | If user starts new grow, archive old `grow-context.md` to `grow-log.md` first, then re-onboard grow-context |

## Verification

Before sending the final onboarding response, check:

- [ ] Pass 0 — did I match depth to user's actual intent?
- [ ] Pass 1 — tier detected or asked?
- [ ] Pass 3 — profile fields collected without demanding what they don't have?
- [ ] Pass 4 — communication preferences explicit?
- [ ] Pass 5 — grow context only if FULL? Sections walked in chunks, not all at once?
- [ ] Pass 6 — diff shown before save?
- [ ] Pass 7 — `last_updated` + `last_updated_by` set?
- [ ] Did I route to a useful next-step workflow?
- [ ] Did I avoid mixing onboarding with the intake checklist?
- [ ] Did I respect the user's pacing (skip allowed, no badgering)?

If any answer is no → fix before sending.

## References

- State schemas: `references/state/user-profile.md`, `references/state/grow-context.md`, `references/state/grow-log.md`
- Confidence gating (post-onboarding): `SKILL.md` Rule 2
- Intake checklist (separate from onboarding): `SKILL.md` Rule 3
- Adaptive depth: `SKILL.md` Rule 4
- Source hierarchy: `SKILL.md` Rule 5
- State updates rule: `SKILL.md` Rule 6
- Next-step workflow targets:
  - `workflows/new-grow-setup.md` — planning a fresh build
  - `workflows/build-feed-schedule.md` — custom feed plan
  - `workflows/diagnose-from-photo.md` — photo-based diagnosis
  - `workflows/harvest-readiness.md` — harvest timing
  - `workflows/troubleshoot-grow.md` — non-photo diagnosis
- Knowledge files for tier calibration: `00-fundamentals.md` (beginner), `21-troubleshooting-tree.md` (intermediate routing), `20-commercial-ops.md` (advanced)
