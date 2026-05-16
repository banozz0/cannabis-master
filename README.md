# cannabis-master

A public Hermes skill for **legal home-grow cannabis cultivation education**.

Bob helps growers plan a setup, troubleshoot plant-health issues, improve IPM, dial lighting/environment/nutrients, time harvest, and handle drying/curing safely. The skill is practical enough for experienced growers, but conservative and beginner-safe by default.

**Status:** 1.2.2 — Public release.

## What Bob does

- **Setup planning** — tents/rooms, lighting, climate, medium, budget, equipment priorities
- **Plant-health troubleshooting** — deficiencies, pests, disease, watering/root issues, environmental stress
- **IPM** — prevention, monitoring, identification, quarantine, sanitation, and label-compatible interventions
- **Nutrition and irrigation** — pH/EC, runoff, feed schedules, soil/coco/hydro/living-soil differences
- **Training and stage changes** — topping, LST, SCROG, defoliation, veg-to-flower decisions
- **Harvest timing** — trichome checks, calyx swell, pistil/senescence cross-checks
- **Post-harvest** — trimming, drying, curing, storage, and solventless-only safety boundaries
- **Advanced cultivation education** — propagation, breeding concepts, pheno-hunting, clean-stock/tissue-culture concepts, and operations hygiene for lawful small grows

## What Bob does **not** do

Bob must refuse or redirect requests for:

- Medical advice, therapeutic claims, dosing, consumption effects, or impairment guidance
- Jurisdiction-specific legal advice, licensing advice, compliance determinations, or legal risk calls
- Trafficking, distribution, diversion, smuggling, evasion, or stealth for illegal activity
- Unsafe extraction guidance, including hydrocarbon/solvent extraction recipes, purge parameters, equipment buildouts, or operating procedures
- Unsafe chemical/lab procedures, including home protocols for hazardous reversal/polyploidy/tissue-culture chemicals

For these topics, Bob redirects to qualified professionals or back to safe cultivation, drying/curing, trimming, storage, or solventless safety boundaries.

## Installation in Hermes

```bash
# Install Hermes if needed
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash

# Clone this skill
git clone https://github.com/banozz0/cannabis-master.git

# Install the skill into your Hermes skills directory
mkdir -p ~/.hermes/skills/cultivation
cp -R cannabis-master ~/.hermes/skills/cultivation/cannabis-master

# Start Hermes
hermes
```

Then ask a cultivation question naturally, or explicitly load/use the skill with `/cannabis-master` if your Hermes interface supports skill slash commands.

If you maintain skills in a separate repository, add that directory through Hermes external skill directory configuration rather than hard-coding a profile-local path.


## Quick start examples

```text
"I'm planning my first legal home grow with a 3x3 tent and €800 budget."
→ new-grow-setup.md
→ phased setup plan, pre-flight checklist, optional state draft after confirmation

"My lower leaves are yellowing in week 5 flower."
→ troubleshoot-grow.md
→ confidence-labeled top causes, missing-data checklist, low-risk next checks

"Is this plant ready to harvest?" + white-light bud photos
→ harvest-readiness.md
→ trichome/signal checklist, confidence rating, harvest-window recommendation

"Help me build a coco feed schedule using RO water and Athena Pro."
→ build-feed-schedule.md
→ EC/pH ranges, ramp-up, runoff checks, state update only after confirmation

"I found tiny moving dots under the leaves."
→ 08-pests.md + diagnosis workflow
→ IPM-first triage: isolate, identify, monitor, then choose label-compatible controls
```

## Safety and confidence model

- **HIGH confidence:** complete intake + clear white-light photos where relevant.
- **MEDIUM confidence:** enough evidence to act cautiously, with explicit gaps and verification steps.
- **LOW confidence:** insufficient or ambiguous data. Bob should not give a firm diagnosis or aggressive treatment; he can ask for missing data or offer low-risk triage clearly labeled as low confidence.

All durable state writes require a draft preview and explicit user confirmation. Bob does not silently persist grow details, diagnoses, profile facts, or logs.

## Skill structure

```text
cannabis-master/
├── SKILL.md                          Entry point, routing, operating rules, boundaries
├── state/                            Optional persistent state templates
│   ├── user-profile.md               User experience, preferences, goals
│   ├── grow-context.md               Active or planned grow setup
│   └── grow-log.md                   Append-only grow journal
├── knowledge/                        Reference knowledge
│   ├── 00-fundamentals.md            Core principles
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
│   ├── 17-extraction-basics.md       Solventless boundaries + unsafe extraction refusals
│   ├── 18-breeding.md
│   ├── 19-tissue-culture.md
│   ├── 20-commercial-ops.md          Operations hygiene, not legal/commercial consulting
│   └── 21-troubleshooting-tree.md
├── workflows/                        Task-specific procedures
│   ├── onboarding.md
│   ├── diagnose-from-photo.md
│   ├── troubleshoot-grow.md
│   ├── build-feed-schedule.md
│   ├── harvest-readiness.md
│   └── new-grow-setup.md
└── docs/                             Release notes, boundaries, examples
```

Skill package: 39 skill files plus this README and LICENSE.

## Source and citation style

The skill prefers:

1. Peer-reviewed horticulture/cannabis research where available
2. Manufacturer labels/spec sheets for product-specific use
3. Extension/IPM guidance for pests, pathogens, sanitation, and pesticide-label discipline
4. Experienced-grower consensus only when clearly labeled and cross-checked

Non-obvious advice should be confidence-labeled and source-tiered rather than presented as universal certainty.

## Versions

**1.2.2 (current)**
- Freeze-check patch: refreshed release metadata, confirmed public safety/readiness boundaries, and removed stale repair-scope wording from readiness notes.

**1.2.1**
- Final public-release polish: clearer README onboarding, consistent safety boundaries, reduced commercial/unsafe wording in setup/onboarding docs, and publishability validation.

**1.2.0**
- Public-release polish: removed profile-local install paths, tightened legal/medical/trafficking/evasion/extraction boundaries, made state writes opt-in, and replaced solvent extraction detail with solventless-only guidance.

**1.1.1**
- Repaired state-write policy, LOW confidence gating, stale path references, and live grow-log examples.
- Added readiness and monetization boundary docs.

**1.1**
- VPD late-flower range narrowed to 1.2-1.5 kPa with adjusted setpoint guidance.
- Grow-log template entries isolated with explicit agent instruction to ignore as user history.
- Skill description rewritten with symptom-language coverage for auto-trigger reliability.
- Diagnose-from-photo workflow retrofitted to canonical state-write pattern.

**1.0**
- Initial skill build.

## Compatibility

- Hermes Agent

## License

MIT
