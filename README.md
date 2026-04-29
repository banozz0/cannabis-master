# cannabis-master

A Hermes-spec cannabis cultivation skill. Powers BOB, a cannabis cultivation expert agent covering the full grower lifecycle from pre-grow planning through cured flower.

**Status:** v1.1 — production-ready, 12/12 test battery passed.

## What this skill does

Provides cannabis cultivation expertise across:

- **Pre-grow planning** — space, lighting, climate, medium selection, budget allocation
- **Active cultivation** — seeding, cloning, transplanting, training, environment dialing, feeding
- **Diagnosis** — photo-based and text-based troubleshooting for deficiencies, pests, disease, environmental stress
- **Harvest timing** — trichome reading, calyx swell, secondary signal cross-check
- **Post-harvest** — drying, curing, jar management, long-term storage
- **Processing** — wet/dry trim, solventless extraction (rosin, hash, dry sift)
- **Advanced topics** — breeding, pheno-hunting, tissue culture, commercial scaling

Maintains persistent state on user setup and active grow context across sessions.

## Architecture

```
cannabis-master/
├── SKILL.md                          Entry point + 6 operating rules
└── references/
    ├── state/                        Persistent state (3 files)
    │   ├── user-profile.md           Who the user is, their preferences
    │   ├── grow-context.md           Active grow setup
    │   └── grow-log.md               Append-only grow journal
    ├── knowledge/                    Reference knowledge (26 files)
    │   ├── 00-fundamentals.md        Core principles
    │   ├── 01-genetics-strains.md
    │   ├── 02-environment.md
    │   ├── 03-lighting.md
    │   ├── 04-medium-{soil,coco,hydro,living-soil}.md
    │   ├── 05-water-quality.md
    │   ├── 06-nutrients-{synthetic,organic}.md
    │   ├── 07-deficiencies.md
    │   ├── 08-pests.md
    │   ├── 09-disease.md
    │   ├── 10-training.md
    │   ├── 11-propagation.md
    │   ├── 12-flowering.md
    │   ├── 13-harvest.md
    │   ├── 14-drying.md
    │   ├── 15-curing.md
    │   ├── 16-trimming.md
    │   ├── 17-extraction-basics.md
    │   ├── 18-breeding.md
    │   ├── 19-tissue-culture.md
    │   ├── 20-commercial-ops.md
    │   └── 21-troubleshooting-tree.md   Master diagnostic routing
    └── workflows/                    Procedural recipes (6 files)
        ├── onboarding.md             First-session state population
        ├── diagnose-from-photo.md    Visual diagnosis with confidence gating
        ├── troubleshoot-grow.md      Text-based diagnosis (MEDIUM cap)
        ├── build-feed-schedule.md    Custom per-grow feed planning
        ├── harvest-readiness.md      Trichome read + timing call
        └── new-grow-setup.md         Pre-grow planning for first-time growers
```

Total: 36 files.

## Design principles

**Confidence framework.** Diagnoses are gated at HIGH (photo + complete intake), MEDIUM (one or the other), or LOW (ambiguous text-only). Never single-answer; always top-3 ranked with confirm-it / rule-it-out criteria.

**Photo gate.** Visual diagnosis requires white-light photos. Blurple LED photos rejected with retake instructions. Multi-sample required for harvest reads (top + mid + bottom).

**State discipline.** All workflows write state with canonical pattern (`last_updated_by: agent` + `source_workflow: <name>`). Diff shown to user before save (Schema Rule 6). Template entries flagged so agent never confuses examples for user history.

**Source tier labeling.** All cited sources tagged Tier 1 (peer-reviewed), Tier 2 (manufacturer), or Tier 3 (master growers). Tier 1 format: `Author (Year) — *Journal* — finding`.

**Hard refusals.** No hydrocarbon extraction recipes (BHO blasting, butane purging). Redirects to solventless alternatives. No medical, legal, or dosing advice.

## Installation in Hermes

```bash
# 1. Install Hermes if not already installed
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash

# 2. Clone this skill into the cultivation category of your profile
git clone <this-repo-url> ~/.hermes-bob/skills/cultivation/cannabis-master

# 3. Set the profile env var and launch
export HERMES_HOME=~/.hermes-bob
hermes
```

The skill auto-loads when user messages match the description.

## Usage examples

```
"my plants have yellow leaves on the bottom in week 5 of flower"
→ troubleshoot-grow.md workflow
→ Top-3 ranked, photo requested for HIGH confidence

"is this ready to harvest yet" + bud photo
→ harvest-readiness.md workflow
→ Trichome %s + secondary signals + recommendation with confidence

"help me build a feed schedule for athena pro on coco rdwc"
→ build-feed-schedule.md workflow
→ Identifies coco/RDWC contradiction, requests clarification before generating

"i want to start growing for the first time, budget €800"
→ new-grow-setup.md workflow
→ Region-aware, climate-aware, constraint-matched recommendations
```

## Build provenance

This skill was built collaboratively using Claude Code (file authoring) and Claude.ai (architecture + audit). Each file was drafted, audited, fixed, and approved before moving to the next. The full build comprised 11 rounds across state schemas, knowledge files, master tree, and workflows, followed by a 12-check pre-ship audit and a 12-prompt test battery.

## Versions

**v1.1 (current)**
- VPD late-flower range narrowed to 1.2-1.5 kPa with adjusted setpoint guidance
- grow-log.md template entries isolated with explicit agent instruction to ignore as user history
- Skill description rewritten with symptom-language coverage for auto-trigger reliability
- diagnose-from-photo.md retrofitted to canonical state-write pattern

**v1.0**
- Initial 36-file build, 12/12 test battery passed

## Compatibility

- Hermes Agent (primary target)
- Anthropic Skills API via Claude.ai (separate deploy version: `cannabis-master-claude`)

## License

MIT
