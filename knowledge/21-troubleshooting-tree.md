# 21 — Master Troubleshooting Tree

Master diagnostic flowchart routing any symptom or grow-room concern to the right knowledge file. Used when the user's complaint doesn't cleanly map to one topic, or when the agent needs to pick a starting branch from a vague intake. Pair with `SKILL.md` Rule 2 (confidence gating) and Rule 3 (intake checklist).

This file is the routing layer. It does not duplicate diagnostic content from deeper files — it points there. The destination file does the heavy lifting.

Cross-reference (every branch routes to one or more of these):
- Foundations and lifecycle → `00-fundamentals.md`
- Genetics and strain expression → `01-genetics-strains.md`
- Environment (temp, RH, VPD, CO2) → `02-environment.md`
- Lighting → `03-lighting.md`
- Medium-specific symptoms → `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md`
- Water quality and pH → `05-water-quality.md`
- Nutrients (synthetic and organic) → `06-nutrients-synthetic.md`, `06-nutrients-organic.md`
- Deficiencies and toxicities → `07-deficiencies.md`
- Pests → `08-pests.md`
- Diseases → `09-disease.md`
- Training → `10-training.md`
- Propagation → `11-propagation.md`
- Flowering → `12-flowering.md`
- Harvest → `13-harvest.md`
- Drying → `14-drying.md`
- Curing → `15-curing.md`
- Trimming → `16-trimming.md`
- Workflow files → `workflows/*`

## How to Use This File

1. Read user complaint — what worried them first?
2. Match complaint to the **Master Branch Selector** below
3. Walk down the tree, gathering data per intake checklist (`SKILL.md` Rule 3)
4. At each leaf node, jump to the cited knowledge file
5. Apply confidence gating (`SKILL.md` Rule 2) before stating a diagnosis
6. Always rank top 3 possibilities for symptom-based diagnoses (never single-answer)
7. If the tree leads to multiple branches, run the **Multi-Symptom Patterns** table at the end

---

## ALWAYS CHECK FIRST (Universal Pre-Diagnostic)

Before walking ANY branch, verify these four. Most "deficiencies" are pH, most "pests" are environment, most "diseases" are humidity.

1. **pH at runoff or res** — see `05-water-quality.md` and `07-deficiencies.md` pH map
   - Soil 6.0-7.0; coco/hydro 5.5-6.3; living soil 6.0-7.0 (no manual adjust)
   - Outside range → 90% chance the problem is lockout, not deficiency
2. **EC at runoff or res** — see `05-water-quality.md`
   - Compare runoff EC vs input EC; large gap = salt buildup or under-feeding
3. **Substrate moisture** — see `04-medium-*.md`
   - Over/underwater mimics nearly every nutrient and disease symptom
4. **Recent change** — equipment, feed, environment, light height, schedule
   - 80%+ of "sudden problems" trace to a change in the prior 3-7 days

If any of these four are unknown → tell user what to measure before diagnosing.

---

## MASTER BRANCH SELECTOR

Pick the branch that matches the user's primary complaint. If they describe multiple, walk each in priority order (most acute first).

| User says... | Walk branch |
|---|---|
| "Leaves are turning [color]" | A — Color/Discoloration |
| "Leaves are curling/twisting/wilting" | B — Shape & Structure |
| "Plant won't grow / stunted / slow" | C — Growth & Vigor |
| "Smells weird / no smell" | D — Smell & Odor |
| "I see bugs / webs / dots / movement" | E — Pest |
| "Spots / fuzz / mold / rot" | F — Disease |
| "Buds are [weird]" | G — Bud-Specific |
| "Numbers don't make sense" (pH, EC, runoff) | H — Numbers |
| "Environment is off" (temp, RH, VPD) | I — Environment |
| "Roots look [weird]" | J — Root Issue |
| "Whole plant is wilting/dying" | K — Systemic |
| "Multiple plants affected the same way" | L — Multi-Plant Pattern |
| "I'm planning a grow / setup question" | → `workflows/new-grow-setup.md` |
| "Feed schedule question" | → `workflows/build-feed-schedule.md` |
| "Harvest timing question" | → `workflows/harvest-readiness.md` |
| "I have a photo to diagnose" | → `workflows/diagnose-from-photo.md` |

---

## A — COLOR / DISCOLORATION

```
WHERE on the plant is the color change?

LOWER / OLDER LEAVES first:
├── Uniform yellow whole leaf → likely N deficiency → 07-deficiencies.md (N section)
├── Yellow with purple stems / dark before yellow → P deficiency → 07-deficiencies.md (P)
├── Tip burn moving inward + margin yellow → K deficiency or salt buildup → 07-deficiencies.md (K) + 05-water-quality.md (EC)
├── Interveinal yellow, green veins → Mg deficiency → 07-deficiencies.md (Mg)
├── Brown/black spots irregular → likely disease → 09-disease.md (Septoria, leaf spot)
├── Reddish/purple petioles + yellowing → could be P def OR cold root zone → 02-environment.md + 07-deficiencies.md (P)
└── Late flower (week 7+) gradual fade lower-up → NORMAL ripening → 13-harvest.md

UPPER / NEW LEAVES first:
├── Uniform yellow → S deficiency or major pH lockout → 07-deficiencies.md (S) + 05-water-quality.md
├── Interveinal yellow with sharp green veins → Fe deficiency, almost always pH lockout → 07-deficiencies.md (Fe) + 05-water-quality.md (CHECK pH FIRST)
├── Interveinal yellow with brown spots → Mn deficiency → 07-deficiencies.md (Mn)
├── Distorted, twisted, hooked, brown new shoots → Ca deficiency or B deficiency → 07-deficiencies.md (Ca, B)
├── Short internodes, rosette pattern → Zn deficiency → 07-deficiencies.md (Zn)
├── Bronze/silver sheen on new growth → Cu deficiency or thrip damage → 07-deficiencies.md (Cu) + 08-pests.md (thrips)
└── Bleached/white top leaves → light burn → 03-lighting.md

WHOLE PLANT yellowing:
├── Sudden over hours → root rot or major pH crash → 09-disease.md (Pythium) + 05-water-quality.md
├── Slow over weeks all leaves → underfeeding (organic depletion) or generalized N → 06-nutrients-*.md + 07-deficiencies.md
└── In flush / late flower → designed fade → 13-harvest.md

PURPLE / RED:
├── Stems only, plant otherwise green → genetic anthocyanin → 01-genetics-strains.md (NOT a problem)
├── Purpling with cold nights (<60°F) → cold-induced anthocyanin → 02-environment.md
├── Purpling + actual P deficiency symptoms (dark before yellow, brown spots) → P deficiency → 07-deficiencies.md (P)
└── Whole-plant red/purple → genetic, late flower, cold → 01-genetics-strains.md + 12-flowering.md

DARK GREEN / GLOSSY:
├── Claw shape (tips curl down) → N toxicity → 07-deficiencies.md (N tox)
├── Brittle dark leaves → N tox or low transpiration → 07-deficiencies.md + 02-environment.md (RH)
└── Black-green with PM dust → could be PM masking color → 09-disease.md (PM)

WHITE / BLEACHED:
├── Top canopy bleached, lower normal → light burn → 03-lighting.md
├── Random patches white-speckled → thrips or spider mites → 08-pests.md
├── Whole-plant pale → severe Fe/N or root issue → 07-deficiencies.md + 09-disease.md
└── Dust on leaves white → PM (powdery mildew) → 09-disease.md (PM)
```

---

## B — SHAPE & STRUCTURE

```
LEAVES CURLING:

Down (claw):
├── N toxicity → 07-deficiencies.md (N tox)
├── Overwatering → 04-medium-*.md
├── Heat stress (top of canopy) → 02-environment.md
└── pH crashed → 05-water-quality.md

Up (taco):
├── Heat above ~85°F at canopy → 02-environment.md
├── K deficiency (with margin yellowing) → 07-deficiencies.md (K)
├── Light too close (top only) → 03-lighting.md
└── Low humidity (<35% RH) high VPD → 02-environment.md

Edges curl + crispy:
├── Heat + low RH → 02-environment.md
├── Light burn → 03-lighting.md
└── Salt buildup (margin tip burn) → 05-water-quality.md (EC)

DROOPING (no color change):
├── Underwater → 04-medium-*.md
├── Overwater → 04-medium-*.md (check substrate weight, lift pot)
├── Recently transplanted → normal 24-48h → 11-propagation.md
└── Root issue → 09-disease.md (Pythium / root rot)

TWISTED / DISTORTED NEW GROWTH:
├── Ca deficiency (most likely) → 07-deficiencies.md (Ca)
├── Broad mite or russet mite damage → 08-pests.md (mites)
├── Heat damage past tolerance → 02-environment.md
├── HLVd-induced "duck-foot" → 09-disease.md (HLVd)
└── Herbicide drift exposure → 02-environment.md (toxic exposure)

WILTING:
├── Sudden, no color change → root rot or major pH crash → 09-disease.md (Pythium) + 05-water-quality.md
├── Gradual + yellowing → N deficiency or general decline → 07-deficiencies.md
└── Hot day only, recovers at night → heat stress, transpiration outpaces uptake → 02-environment.md

STRETCHING (long internodes):
├── In veg → low light → 03-lighting.md (PPFD)
├── Early flower normal stretch → 12-flowering.md
└── Excessive flower stretch → genetic (sativa) or low DLI → 01-genetics-strains.md + 03-lighting.md

NO STRETCH / SHORT:
├── Genetic (indica/auto) → 01-genetics-strains.md
├── Light too close + intense → 03-lighting.md
└── Stunted from root issue → 09-disease.md
```

---

## C — GROWTH & VIGOR

```
SLOW / STUNTED but otherwise OK color:

Seedling stage:
├── Normal first week → 11-propagation.md
├── Cold (<70°F) → 02-environment.md
├── Damping off (collapsed stem) → 09-disease.md (Pythium)
└── Compaction in seedling soil → 04-medium-*.md

Veg stage:
├── Root-bound → up-pot → 11-propagation.md
├── Underfeeding → 06-nutrients-*.md
├── Low DLI → 03-lighting.md
├── pH lockout → 05-water-quality.md
├── Cold root zone → 02-environment.md (target 65-75°F media)
├── HLVd "dudding" → 09-disease.md (HLVd)
└── Genetic runt → 01-genetics-strains.md (cull or up-pot)

Flower stage:
├── Slow flower development → check DLI, temp differential, P/K levels → 03-lighting.md + 02-environment.md + 07-deficiencies.md
├── Stalled at "popcorn" → typically genetic or stress → 12-flowering.md + 01-genetics-strains.md
└── Late-flower stop → normal as ripening, OR root failure → 12-flowering.md + 09-disease.md

EXCESSIVELY FAST / TALL:
├── Stretch in early flower up to 100% normal → 12-flowering.md
├── Sativa heritage → 01-genetics-strains.md
└── Too high N in flower → 07-deficiencies.md (N tox in flower)

ONE PLANT IN GROUP STUNTED:
├── HLVd (single plant or cluster from clones) → 09-disease.md (HLVd)
├── Genetic variation in pack → 01-genetics-strains.md (normal)
├── Root issue or pot-bound → 11-propagation.md
└── Localized environment (corner, dead spot) → 02-environment.md
```

---

## D — SMELL & ODOR

```
NO SMELL / WEAK SMELL:

In flower week 4+:
├── Genetic low-terp pheno → 01-genetics-strains.md
├── Root zone too cold (terps need warmth) → 02-environment.md
├── S deficiency (terpenes use S) → 07-deficiencies.md (S)
└── Light intensity too low (terps respond to UV/intensity) → 03-lighting.md

In flower week 6-8:
├── Low RH in flower (terps preserve at 50-60%) → 02-environment.md
├── Genetic → 01-genetics-strains.md
└── Late stage flush stripping smell → 12-flowering.md

SMELL OFF / WRONG:

Hay / grass smell:
├── Drying too fast (over-dried) → 14-drying.md
├── Cured too cold/dry → 15-curing.md
└── Chlorophyll not broken down (rushed dry/cure) → 14-drying.md + 15-curing.md

Ammonia / sweet rot:
├── Mold during cure (Aw too high) → 09-disease.md + 15-curing.md (target 0.55-0.62)
├── Anaerobic spots in jar → 15-curing.md (burping)
└── Bud rot (Botrytis) — STOP curing, inspect → 09-disease.md (Botrytis)

Cat pee / sharp ammonia:
├── Nitrogen-heavy late flower → 07-deficiencies.md + 12-flowering.md
└── Some genetics naturally smell this way → 01-genetics-strains.md

Sour / vinegar:
├── Fermentation in cure (over-wet) → 15-curing.md
└── Bacterial bloom in trim before dry → 13-harvest.md + 14-drying.md

Earthy / musty (off):
├── Mold in dry/cure → 09-disease.md
└── Stem rot during dry → 14-drying.md

LIVING PLANT smells like ammonia/death:
├── Pythium / root rot → 09-disease.md (root rot)
└── Anaerobic substrate → 04-medium-*.md
```

---

## E — PEST

```
USER REPORTS BUGS / WEBS / MOVEMENT — load 08-pests.md

Speckled / stippled leaves + tiny dots underside:
├── Spider mites (webbing in late stages) → 08-pests.md (spider mites)
└── Broad mite / russet mite (no web, severe distortion) → 08-pests.md (mites)

White flies fly when disturbed:
├── Whitefly → 08-pests.md (whitefly)

Tiny black/silver streaks + black dots (frass):
├── Thrips → 08-pests.md (thrips)

Sticky honeydew + ants on plant:
├── Aphids or scale → 08-pests.md (aphids/scale)

Soil-surface tiny black gnats:
├── Fungus gnats → 08-pests.md (fungus gnats)

Holes in leaves + green caterpillar frass:
├── Caterpillars (esp. budworms in flower) → 08-pests.md (caterpillars/budworms)

Slugs/snails outdoor:
├── Outdoor pest → 08-pests.md (slugs)

White cottony lumps in nodes:
├── Mealybugs → 08-pests.md (mealybugs)

Small jumping insects on substrate:
├── Springtails (usually harmless / beneficial) → 08-pests.md
└── Root aphids if pale and on roots → 08-pests.md (root aphids)

NO bugs visible BUT pest-like damage:
├── Broad/russet mites (microscopic, top growth) → loupe under 60x+ → 08-pests.md
├── Hop latent viroid mimics distortion → 09-disease.md (HLVd)
└── Heat/light damage misread → 02-environment.md + 03-lighting.md
```

---

## F — DISEASE

```
USER REPORTS SPOTS / FUZZ / MOLD — load 09-disease.md

White powdery dust on leaves:
├── Powdery mildew (PM) → 09-disease.md (PM)

Gray fuzzy mold on bud or stem:
├── Botrytis (bud rot) → 09-disease.md (Botrytis) — IMMEDIATE remove
└── Saprophytic mold on dead tissue → 09-disease.md

Round brown spots with yellow halo, lower leaves:
├── Septoria leaf spot → 09-disease.md (Septoria)

Yellow patches with downward leaf curl:
├── Downy mildew → 09-disease.md (downy mildew)

Wilting + brown streaks in stem when cut:
├── Fusarium wilt → 09-disease.md (Fusarium)
├── Verticillium wilt → 09-disease.md (Verticillium)

Roots brown/slimy, plant droops:
├── Pythium / root rot → 09-disease.md (Pythium)

Stunted plants from clones, duck-foot leaves, low yield:
├── HLVd (Hop Latent Viroid) → 09-disease.md (HLVd) — TEST RT-qPCR

Mosaic yellow patterns on leaves:
├── Tobacco Mosaic Virus or Cucumber Mosaic Virus → 09-disease.md (viruses)

Crown gall / tumor at soil line:
├── Agrobacterium → 09-disease.md
```

---

## G — BUD-SPECIFIC

```
BUD WON'T DENSIFY / FLUFFY / AIRY:
├── Low DLI → 03-lighting.md (need ≥40 mol/m²/day in flower)
├── High temp in flower (>82°F) → 02-environment.md (foxtailing risk)
├── Genetic (sativa-leaning) → 01-genetics-strains.md
└── Underfed in mid-flower → 06-nutrients-*.md

FOXTAILING (towers / spikes growing out of buds):
├── Heat stress (top canopy >85°F) → 02-environment.md
├── Light stress (too close / bleaching) → 03-lighting.md
└── Genetic (some sativa lines) → 01-genetics-strains.md

NANNERS / MALE FLOWERS LATE FLOWER:
├── Stress (heat, light leak, watering inconsistent) → 12-flowering.md (herm causes)
├── Genetic herm tendency → 01-genetics-strains.md + 18-breeding.md
├── Light leak in dark cycle → 03-lighting.md (sealed dark)
└── Too long flower past ripeness → 13-harvest.md

PURPLE BUDS:
├── Cold nights late flower (cosmetic) → 02-environment.md
├── Genetic (purple lines) → 01-genetics-strains.md
└── NOT a deficiency unless other symptoms → 07-deficiencies.md (P)

SEEDED BUDS (unintentional):
├── Self-pollination (herm nanner) → 12-flowering.md
├── Outdoor pollen drift → 18-breeding.md (pollen biology)
└── Reversal exposure (chemical drift) → 18-breeding.md

REVEG / RE-VEG (spike of single-leaf growth in flower):
├── Light leak / interrupted dark → 03-lighting.md
├── Photoperiod transition error → 12-flowering.md
└── Hermaphrodite stress response → 12-flowering.md

WHITE / BLEACHED BUDS:
├── Light too close (bleach) → 03-lighting.md (PPFD)
├── PM mistaken for trichomes → 09-disease.md (PM)
└── Genetic albino expression → 01-genetics-strains.md

CALYXES SWELLING but no real bud growth:
├── Late ripening normal → 13-harvest.md (calyx swell signal)
└── Stress-induced calyx swell → 12-flowering.md
```

---

## H — NUMBERS OFF

```
pH:

Input pH off:
├── Verify meter calibration → 05-water-quality.md
├── pH-up/down miscalibrated → 05-water-quality.md
└── Source water alkalinity drifting → 05-water-quality.md

Runoff pH drifting up over time (coco/hydro):
├── Salt buildup buffering → 05-water-quality.md (flush) + 04-medium-coco.md
└── Calcium accumulation → 05-water-quality.md

Runoff pH drifting down over time:
├── Aggressive feeding (acidic salts accumulating) → 06-nutrients-synthetic.md
├── Anaerobic substrate fermenting → 04-medium-*.md
└── Microbial bloom → 04-medium-living-soil.md

EC:

Runoff EC > input EC → salt buildup; lower feed EC or flush → 05-water-quality.md
Runoff EC < input EC → root zone depleted; could be underfeeding OR root issue/heat preventing water uptake → 04-medium-*.md + 09-disease.md
Runoff EC ≈ input EC → balanced (target) → 06-nutrients-*.md

PPM scale confusion:
├── 500 vs 700 scale (NaCl vs KCl) — verify which meter scale → 05-water-quality.md
└── EC × 700 = 700-scale ppm; EC × 500 = 500-scale ppm

Volume in vs volume out:
├── 10-20% runoff target normal feed → 04-medium-coco.md / 04-medium-soil.md
├── No runoff → underwatering, can't read runoff numbers → 04-medium-*.md
└── 50%+ runoff → flushing or overwatering → 05-water-quality.md

"Should I flush?":
├── Salt buildup (runoff EC > input by 0.5+) → YES, flush → 05-water-quality.md
├── pH drift severe → YES, flush + reset → 05-water-quality.md
├── Pre-harvest "to improve flavor" → NO, debunked, rely on cure → 13-harvest.md + 15-curing.md
├── Routine in coco/hydro → NO, daily fertigation handles this → 04-medium-coco.md
└── Living soil → NEVER flush → 04-medium-living-soil.md
```

---

## I — ENVIRONMENT OFF

```
TEMP:
├── Day too hot (>82°F flower) → 02-environment.md (cooling)
├── Night too cold (<62°F) → 02-environment.md (heater, anthocyanin risk)
├── Day-night swing too wide (>15°F) → 02-environment.md
├── Heat at canopy ≠ heat at sensor → relocate sensor or use IR check → 02-environment.md
└── Lights-off temp not falling → HVAC sizing → 02-environment.md + 20-commercial-ops.md

RH:
├── Too high in flower (>60%) → mold/bud rot risk → 02-environment.md + 09-disease.md
├── Too low in flower (<40%) → terp loss, plant stress → 02-environment.md
├── Too high in seedling (>75%) → damping off risk → 09-disease.md
├── Too low in clone (<70%) → won't root → 11-propagation.md
└── Lights-off RH spike → undersized dehumidifier → 02-environment.md + 20-commercial-ops.md

VPD:
├── High VPD (>1.4 kPa flower) → plant stressed, locked stomata → 02-environment.md
├── Low VPD (<0.7 kPa flower) → mold/bud rot risk → 02-environment.md + 09-disease.md
└── Calculate from temp + RH → 02-environment.md (VPD chart)

CO2:
├── Sealed room not enriching → check generator/tank → 02-environment.md
├── Unsealed room with CO2 = waste of money → 02-environment.md + 20-commercial-ops.md
└── CO2 too high (>5000 ppm) → human safety alarm → 20-commercial-ops.md

AIRFLOW:
├── Dead zones in tent/room → add fans → 02-environment.md
├── Fans too close, leaf burn from windburn → 02-environment.md
└── No fresh air exchange → CO2 depletion + heat buildup → 02-environment.md
```

---

## J — ROOT ISSUE

```
USER REPORTS WEIRD ROOTS — load 04-medium-*.md and 09-disease.md

White healthy roots → no problem → 11-propagation.md
Tan/cream roots → normal in some media (especially organic) → 04-medium-*.md
Brown / slimy roots + plant droop → Pythium → 09-disease.md (Pythium / root rot)
Roots circling pot bottom → root-bound, up-pot → 11-propagation.md
Roots growing OUT of fabric pot bottom → time to up-pot or set in tray → 11-propagation.md
Stunted root growth in coco → low EC in early veg, ramp up → 04-medium-coco.md
No root growth from clone after 3+ weeks → check humidity, hormone, temp → 11-propagation.md
Root aphids visible (pale insects on roots) → 08-pests.md (root aphids)
Smell of rot when pot inspected → anaerobic / Pythium → 09-disease.md + 04-medium-*.md
```

---

## K — SYSTEMIC / WHOLE-PLANT FAILING

```
PLANT IS DYING — emergency triage:

Sudden full wilt with no color change:
├── Pythium (root rot) → 09-disease.md (Pythium) — IMMEDIATE
├── pH crash → 05-water-quality.md
├── Major root damage (transplant shock, broken root) → 11-propagation.md
└── Severe overwatering with anaerobic conditions → 04-medium-*.md

Sudden dropping of all leaves:
├── Severe stress (toxic exposure, pH crash) → 02-environment.md
├── Cold shock → 02-environment.md
└── Late flower normal senescence (week 8+) → 13-harvest.md

Plant won't recover after watering:
├── Root rot established → 09-disease.md
├── Severe nute lockout → 05-water-quality.md (flush + reset)
└── Multiple compounding issues → run full intake → SKILL.md Rule 3

Yellow + drooping + stem soft at base:
├── Damping off (seedling) → 09-disease.md (Pythium)
└── Root rot adult plant → 09-disease.md (Pythium)

Plant looks fine but won't grow at all in 2+ weeks:
├── HLVd "dudding" → 09-disease.md (HLVd) — TEST
├── Severe pH lockout → 05-water-quality.md
├── Cold root zone → 02-environment.md (≥65°F media)
└── Overpotted / root-bound paradox → 11-propagation.md
```

---

## L — MULTI-PLANT PATTERN

The pattern across plants reveals the cause.

```
ALL plants same symptom → environmental, water, feed (system-level)
   → Check feed batch, pH, EC, environment, water source, light schedule

SOME plants same symptom (cluster) → genetics-cluster OR localized environment
   → Are they same strain? Same corner of room? Same clone batch?

ONE plant different from siblings → genetics, individual root issue, or HLVd
   → Test HLVd if unexplained slow + distortion → 09-disease.md

SAME-strain plants identical symptoms across rooms → strain susceptibility
   → 01-genetics-strains.md + check if it's a known herm/PM-prone line

CLONE-LINE pattern (only this clone shows it) → mom is the source
   → HLVd test → 09-disease.md
   → Refresh from cleaner mom → 11-propagation.md
   → Or replace from seed → 18-breeding.md

SEED-PACK pattern (entire pack of seeds shows it) → genetic line carries trait
   → 01-genetics-strains.md + 18-breeding.md
```

---

## L+ — AUTOFLOWER-SPECIFIC

```
Auto won't flower on time:
├── Light stress / transplant shock delaying flip → 11-propagation.md
├── Cold root zone slowing trigger → 02-environment.md
└── Genetic variance in pack (some autos slow) → 01-genetics-strains.md

Auto stunted permanently after stress:
├── Autos don't recover from veg-stage stress like photos → 11-propagation.md
└── Up-pot shock irreversible past day 14 → 04-medium-*.md

Auto finishing too small:
├── Pot too small from start (autos can't be transplanted) → 04-medium-*.md
├── Light intensity too low in critical first 3 weeks → 03-lighting.md
└── Genetic (modern autos still smaller than photos on average) → 01-genetics-strains.md
```

---

## MULTI-SYMPTOM PATTERNS ("Syndromes")

Some symptom combinations are diagnostic on sight. If user describes more than one symptom, check the combination here first.

| Combined symptoms | Most likely cause | Knowledge file |
|---|---|---|
| Yellow lower leaves + dark green claw upper | N feed mismatch (under in old, over in new) | `07-deficiencies.md` (N) |
| Interveinal yellow upper + Fe-style green veins + recent water source change | Fe lockout from pH drift | `05-water-quality.md` + `07-deficiencies.md` |
| Brown tip burn + EC creep at runoff | Salt buildup; flush needed | `05-water-quality.md` |
| Stunted + duck-foot leaves + low yield + clone-line | HLVd | `09-disease.md` (HLVd) — test |
| Wilting + slow + brown roots + sour smell | Pythium / root rot | `09-disease.md` (Pythium) |
| Dust on leaves + spreading from one plant | Powdery mildew | `09-disease.md` (PM) |
| Webbing in canopy + tiny moving dots + stippled leaves | Spider mites | `08-pests.md` |
| Twisted new growth + speckled leaves + no visible bugs | Broad or russet mites (microscope) | `08-pests.md` (mites) |
| Hay smell after dry + brittle stems | Over-dried | `14-drying.md` |
| Ammonia smell + moist buds in jar | Cure failure / Aw too high / mold | `15-curing.md` + `09-disease.md` |
| Bleached top buds + small lower buds | Light too close, raise | `03-lighting.md` |
| Foxtailing + heat at canopy + sativa pheno | Heat-driven foxtail in heat-prone strain | `02-environment.md` + `01-genetics-strains.md` |
| Nanners late flower + recent stress event (heat, water, light leak) | Stress-induced herm | `12-flowering.md` |
| Distortion + yellowing + multiple plants from clones | HLVd or systemic disease | `09-disease.md` |
| Slow root + cold tent + winter | Root zone temp too low | `02-environment.md` (root zone ≥65°F) |
| Calcium-style tip burn on new growth + RO water + coco | RO + coco without Cal-Mg | `07-deficiencies.md` (Ca) + `05-water-quality.md` |
| Magnesium-style interveinal + mid-late flower + heavy feeding | K-Mg antagonism from PK boost | `07-deficiencies.md` (Mg) + `06-nutrients-*.md` |
| Multiple "deficiencies" simultaneously | Single pH lockout cascading | `05-water-quality.md` |
| Lower fade in week 7+ flower (no other symptoms) | Normal ripening | `13-harvest.md` |

---

## STAGE-BASED TRIAGE

Different stages have different baseline expectations. What's a problem in veg may be normal in flower.

| Stage | Common normal observations | When to act |
|---|---|---|
| Seedling (week 0-2) | Slow first week, cotyledons yellow as true leaves develop | Stem damping, dark/wet base, no growth past day 10 |
| Veg (week 3-6) | Dark green, vigorous, all-leaf-same-color | Yellowing, stretching, distortion |
| Pre-flower (week 0-1 of flip) | Stretch starts, pre-flowers visible | Stunted stretch, no preflowers by day 10 of 12/12 |
| Stretch flower (week 2-3) | 50-100% height gain | Excessive stretch (sativa or low light), nanners |
| Bud development (week 4-6) | Flower fattening, terps up, lower leaves may yellow lightly | Bud rot, foxtail from heat, pest spike |
| Late flower (week 7-9) | Trichomes mature, lower leaves fade, ripening signals | Re-veg from light leak, stress nanners, mold |
| Pre-harvest (final week) | Fade, trichome cloud, smell peaks | Anything new — usually means harvest now |
| Drying (week 1 post-harvest) | Bud firms, snap test of stem develops | Hay smell (over-dry), mold (under-dry) |
| Curing (week 2-8 post-dry) | Smell deepens, RH stabilizes 58-62% | Ammonia (mold), grass smell (rushed dry) |

---

## CONFIDENCE GATING WALK-THROUGH

After narrowing the tree to a leaf node, before stating the diagnosis:

1. **Do you have intake data?** (stage, medium, feed, pH, EC, runoff, temp, RH, water source) — see `SKILL.md` Rule 3
   - All present → potentially HIGH confidence
   - Most missing → LOW confidence, request data first
2. **Do you have a clear photo?** (white light, focused, whole plant + close-up)
   - No / blurple LED → request retake (`workflows/diagnose-from-photo.md`)
3. **Have you applied "Always Check First"?** (pH, EC, moisture, recent change)
   - No → check before naming a cause
4. **Are you stating top 3 ranked possibilities?**
   - One answer → revise to ranked list per `workflows/diagnose-from-photo.md`
5. **Have you cited which knowledge file the diagnosis comes from?**
   - Yes → proceed
   - No → cite for the user to verify

---

## SOURCES

This file routes to deeper files; canonical sources for each topic live there. Routing logic itself synthesizes:

**Tier 1 — Peer-reviewed (foundations of routing logic):**
- Bugbee, B. — Utah State, foundational environment and lighting research
- Caplan, D. et al. — Guelph, fertilizer and substrate research
- Punja, Z. K. et al. (2019) — *Frontiers in Plant Science* — pathogen review in controlled cannabis cultivation
- Warren, J. G. et al. (2019) — *Plant Disease* — HLVd characterization
- Chandra, S. et al. — strain biology and physiology

**Tier 2 — Industry / lab:**
- Athena Pro, Canna, Jacks technical bulletins (per-symptom troubleshooting trees these draw on)
- Medicinal Genomics — HLVd diagnostic protocols
- Pulse Pro, Trolmaster — environment threshold guidance

**Tier 3 — Master practitioners:**
- Jorge Cervantes — *Cannabis Encyclopedia* diagnostic chapters
- Ed Rosenthal — *Marijuana Grower's Handbook* problem chapters
- DeBacco University — symptom-by-symptom diagnostic content
- Mr. Canucks Grow — practical troubleshooting demonstrations

**Tier 4 — Community consensus (cross-confirm before applying):**
- Grasscity, ICmag, /r/microgrowery diagnostic threads — useful for outlier patterns, cross-confirm with tier 1-3

---

## CROSS-REFERENCES (FULL ROUTING TARGETS)

- Routing destination for color/structure/growth → `00-fundamentals.md`, `07-deficiencies.md`
- pH/water issues → `05-water-quality.md`
- Medium-specific → `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md`
- Environment → `02-environment.md`
- Lighting → `03-lighting.md`
- Pests → `08-pests.md`
- Diseases → `09-disease.md`
- Stage-related → `11-propagation.md`, `12-flowering.md`, `13-harvest.md`
- Post-harvest → `14-drying.md`, `15-curing.md`, `16-trimming.md`
- Genetic factors → `01-genetics-strains.md`, `18-breeding.md`
- TC / clean stock context → `19-tissue-culture.md`
- Commercial-scale syndromes → `20-commercial-ops.md`
- Workflows for full diagnostic flow → `workflows/diagnose-from-photo.md`, `workflows/troubleshoot-grow.md`
