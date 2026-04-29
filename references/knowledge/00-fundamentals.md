# 00 — Cannabis Fundamentals

Plant biology baseline for the rest of the skill. Covers taxonomy, anatomy, life cycle, sex, photoperiod, cannabinoid and terpene biosynthesis, photosynthesis, and transpiration. Every other knowledge file assumes the concepts here. Cross-reference with `01-genetics-strains.md` (cultivar selection), `02-environment.md` (VPD, temp, RH targets), `03-lighting.md` (PPFD/DLI math), `12-flowering.md` (transition mechanics), `13-harvest.md` (cannabinoid/terpene maturity reading).

## How to Use This File

1. **Read sequentially the first time** — concepts build on each other (anatomy → life cycle → sex → photoperiod → biochemistry).
2. **For diagnostic work, jump to Life Cycle Stages first** — most "what's wrong" questions resolve once stage is correctly identified.
3. **For cultivar/product decisions, skip to Cannabinoid Biosynthesis and Terpene Biosynthesis** — these explain why heat handling and harvest timing matter.
4. **For room/light planning, skip to Photoperiod Biology and Photosynthesis & Transpiration** — these justify the targets in `02-environment.md` and `03-lighting.md`.

## Core Concepts

Four facts unlock most of the rest of the skill. Memorize these.

| Concept | What it means | Why it matters |
|---|---|---|
| **Cannabis is photoperiod-sensitive** (with a ruderalis-derived exception) | Most cultivars flower in response to long uninterrupted dark periods, not light hours | Drives the entire indoor lighting protocol (18/6 veg, 12/12 flower) |
| **Cannabis is dioecious by default** | Separate male and female plants in nature | Females produce the trichome-rich flowers we want; males pollinate and ruin sinsemilla yield |
| **Cannabis runs C3 photosynthesis** | Standard temperate-plant carbon fixation | Caps photosynthesis at moderate temps and CO₂; explains why CO₂ supplementation helps in sealed rooms |
| **Cannabinoids and terpenes are produced in glandular trichomes** | Resin glands on flower bracts (and sparingly on sugar leaves) are the chemical factories | Terpene heat sensitivity, harvest trichome reading, hash-making, drying RH all flow from this |

## Plant Taxonomy & Subspecies

Cannabis sits in family **Cannabaceae** alongside hops (*Humulus*) — a relationship that explains the shared monoterpene profile (myrcene, humulene) between cannabis and hoppy beer.

Whether *Cannabis* is one species or three is unresolved among taxonomists. Three frameworks dominate:

| Framework | Position | Notable for |
|---|---|---|
| **Small & Cronquist (1976)** | One species, *C. sativa* L., with subspecies *sativa* (fiber/seed) and *indica* (drug). | Closest to original protolog data; the conservative academic position. |
| **Hillig (2005)** | Polytypic — three species (*C. sativa*, *C. indica*, *C. ruderalis*) with seven subspecies/varieties, based on allozyme variation at 17 loci across 157 samples. | The polytypic / "three species" position grower vernacular borrows. |
| **Clarke & Merlin (2013)** | Chemotaxonomic — narrow-leaf drug (NLD), broad-leaf drug (BLD), narrow-leaf hemp (NLH). | Cleaner mapping to what growers actually see; sidesteps the species debate. |

**Vernacular reality:** "Indica" and "sativa" labels on dispensary shelves are marketing, not taxonomy. After 60+ years of hybridization, almost every modern cultivar is a hybrid. Effects predicted from "indica" or "sativa" labels correlate weakly with chemovar — terpene + cannabinoid profile predicts effects far better. See `01-genetics-strains.md`.

**Chemovar (chemotype) approach** is replacing morphology-based labels:
- **Type I** — THC-dominant
- **Type II** — Balanced THC:CBD (~1:1)
- **Type III** — CBD-dominant
- **Type IV** — CBG-dominant (rare, breeding interest)
- **Type V** — Negligible cannabinoids (industrial hemp, fiber)

## Anatomy

### Roots
- **Taproot** in seed-grown plants; **fibrous adventitious mat** in clones (clones have no taproot — affects pot sizing and stake support).
- **Root tips** (white, growing) absorb water; **root hairs** (microscopic projections) absorb nutrients.
- **Mycorrhizal associations** — cannabis forms weak vesicular-arbuscular associations. Inoculants help in low-microbe substrates (coco, sterile soil) but contribute less than in many crops.

### Stem & Branches
- **Main stem (stalk)** — vertical leader. In topped/mainlined plants, multiple "main" stems develop after apical removal.
- **Branches** — emerge from nodes. Lower branches lignify (turn woody) over time; upper branches stay flexible — relevant for LST and HST timing.
- **Hollow stems** are normal in vigorous plants. Hollow + brown stem interior = boron deficiency (see `07-deficiencies.md`).

### Nodes & Internodes
- **Node** — point on the stem where leaves and branches emerge.
- **Internode** — space between nodes.
- **Tight internodal spacing** = often indica-leaning genetics, low light, or correctly-dialed environment.
- **Stretched internodes** = sativa genetics, low light, heat stress, or excessive nitrogen.
- **Phyllotaxy** — cannabis nodes are *opposite* (paired) in seedling/early veg, then transition to *alternate* (single) phyllotaxy as the plant matures and starts flowering. Alternate phyllotaxy is the first reliable sign the plant is preparing to flower.

### Leaves
- **Fan leaves** — large, palmate (5–11 leaflets), the photosynthetic engine. Don't strip without reason — see `10-training.md`.
- **Sugar leaves** — small, single-bladed, embedded in flowers. Carry trichomes, less than the bract itself.
- **Cotyledons** — the first two round leaves from a sprouted seed. Photosynthesize for the first 1–2 weeks, then senesce naturally.

### Flowers (Female)
- **Bract** — the small leaf-like structure that wraps around the developing seed (or, when unpollinated, the resin gland cluster). Produces the highest density of trichomes on the plant — bracts are what "buds" are made of, not leaves.
- **Calyx** — botanically incorrect when applied to cannabis flowers (a true calyx is a sepal whorl); the bract-and-perigonal-bract structure is what's actually being referenced. Term persists by convention.
- **Pistil** — composed of two **stigmas** (the white-then-orange-then-brown hairs) and the ovary. Stigmas are pollen-receptive at first, then darken and recede as the flower matures.
- **Pollen sacs** — male flower structures. Look like clusters of small green/yellow balls. Open at maturity to release pollen.

### Trichomes (the resin glands)
Three morphological types, only one is the cannabinoid factory:

| Type | Size | Where | Cannabinoid production |
|---|---|---|---|
| **Bulbous** | 10–30 µm | Whole plant including leaves | Negligible |
| **Capitate-sessile** | 25–100 µm | Leaves, bract surfaces | Low to moderate |
| **Capitate-stalked** | 150–500 µm | Bracts, sugar leaves of female flowers | **The main producer — read these for harvest** |

Capitate-stalked trichomes have a stalk and a bulbous head. Inside the head: a disc of secretory cells produces cannabinoids and terpenes, secreted into the cuticle bubble. **Color shift of the head (clear → milky → amber)** is the canonical harvest readiness signal — see `13-harvest.md`.

## Life Cycle Stages

Times are typical photoperiod indoor; outdoor and autoflowers vary. Multiply by 1.0–1.3× for cooler temps or low light.

### Seed
- Dormant viable for 1–5 years if stored cool, dark, dry (4°C in airtight + desiccant is gold standard).
- Viability drops fast above 20°C or in light.
- Healthy seed: dark brown / black with marbling, hard shell, sinks in water within 2 hours.
- Pale, green, white, or floating seed = often immature, low viability.

### Germination (1–10 days)
- **Imbibition** (water uptake) → seed coat cracks → **radicle** (embryonic root) emerges first → cotyledons unfold above substrate.
- Optimal: 22–26°C, dark, moist (not soaked).
- Methods: paper-towel, direct-to-substrate, jiffy/rapid rooter cube. All work; direct-to-substrate avoids transplant shock to the radicle.
- **Common mistake:** burying too deep. Plant the seed 0.5–1.5 cm deep; deeper than 2 cm and the cotyledons may exhaust energy reaching the surface.

### Seedling (1–3 weeks)
- **First true leaves** appear above the cotyledons — single-bladed, then 3-blade, then 5-blade as nodes develop.
- Root system is shallow and fragile. Risk: overwatering (#1 seedling killer). Roots need oxygen; saturated medium suffocates them.
- Light: low to moderate. PPFD 200–400 µmol/m²/s. High light at this stage causes leaf curling and stress, not faster growth.
- Nutrients: little to none for the first 1–2 weeks if substrate is amended; otherwise 25% strength veg feed.

### Vegetative (2–12 weeks for photoperiod)
- Plant focuses on leaf, stem, and root mass — no flower development.
- Internodes form 3-blade → 5-blade → 7-blade → 9-blade leaves over time.
- **Topping window:** when plant has 5–6 nodes, with stable root development. See `10-training.md`.
- **Sex shows in pre-flowers** at week 4–6 of veg (photoperiod). Look at the node where leaf meets stem: a tiny **calyx with a single hair** = female; a **ball-on-a-stalk** = male. Hold a flashlight to the underside.
- **Vegetative duration is grower's choice** — longer veg = bigger plant + bigger yield, but more space and time. Common range 4–8 weeks indoor.

### Pre-Flower / Stretch (weeks 1–3 of 12/12 for photoperiod)
- After light flip, plant doesn't switch instantly. **Critical photoperiod commitment takes 4–5 days of exposure** before flowering hormones cascade (see Photoperiod Biology below).
- **Stretch:** plant elongates 1.5×–3× its veg height in this window. Sativa-leaning genetics stretch more.
- **Pre-flowers** mature into pistil clusters at every node. Confirms sex if missed in veg.
- **Don't top, FIM, or super-crop after week 2 of flower** — recovery time eats into yield. See `10-training.md`.

### Flowering — Bud Formation (weeks 3–6 of 12/12)
- Stretch slows; bud sites at every node thicken. Pistils proliferate, white and erect.
- Highest nutrient demand of the cycle for **P and K** in this window. N drops.
- Trichome production ramps. Smell intensifies — if no carbon filter yet, install now.

### Ripening / Maturation (weeks 6–9+ of 12/12)
- Pistils begin browning and recede into bracts.
- Bracts swell ("calyx swelling") as the plant prepares for seed (which never arrives in sinsemilla).
- Trichomes shift from clear → milky → amber. **Trichome head color is the canonical harvest signal** — see `13-harvest.md`.
- Some lower-leaf yellowing is normal "fade" — not nitrogen deficiency. Don't feed more N this late.

### Senescence
- Leaves yellow and drop. Plant pulls remaining nutrients into flowers and seeds.
- Indoor cultivators harvest before full senescence (chase trichome window). Outdoor / breeding contexts may let plants senesce fully.

## Sex & Reproduction

Cannabis is **dioecious by default** — separate male and female plants. Sinsemilla cultivation depends on segregating females and removing males before pollen release.

### Male
- **Pollen sacs** (look like ball clusters, green to yellow at maturity) form at internodes.
- Open and release pollen 2–4 days after first sacs appear.
- A single male can pollinate a tent of females in hours via airflow.
- Smaller, sparser flower structures than females.

### Female
- **Pistils** (white, two-pronged hair pairs) emerge at internodes.
- Once pollinated, pistils brown immediately and the bract swells with a developing seed.
- Without pollination, the plant continues throwing more pistils → bract clusters → trichome-rich flowers (sinsemilla).

### Pre-Flower Identification (Pre-Flip)
- Photoperiod plants typically show pre-flowers at the nodes of the upper third of the plant by week 4–6 of veg.
- **Female pre-flower:** a tiny teardrop-shaped calyx with one or two thin white hairs (stigmas) emerging.
- **Male pre-flower:** a ball or round nodule on a short stalk, no hairs.
- Inspect with a phone camera macro or jeweler's loupe at the node.
- Autoflowers show sex within 3–4 weeks from sprout because they're already flowering.

### Hermaphrodite, Monoecious, and Intersex
Three different things, often conflated:

| Term | Meaning | Practical risk |
|---|---|---|
| **Monoecious** | Genetically programmed to produce both pollen sacs and pistils on the same plant | Hemp varieties often monoecious by design; NOT common in drug-type cultivars |
| **Hermaphrodite** | Female plant develops pollen sacs in addition to pistils, usually under stress; "true herm" produces both whole-flower types on the same plant | Pollinates itself and neighbors → seeded buds, lost run |
| **Intersex / "nanners"** | Female plant develops a few pollen-bearing anthers ("banana"-shaped) intermixed with pistils, late in flower | Less devastating than full herm; can sometimes be removed if caught early |

### What Triggers Herming
1. **Light stress** — light leaks during dark period, photoperiod inconsistency.
2. **Heat stress** — sustained canopy temps above 30°C late flower.
3. **Genetics** — some lineages are herm-prone (cull these in pheno selection).
4. **Severe nutrient stress** or pH crash.
5. **Re-vegging mid-flower** — dropping back to veg light schedule after triggering flower confuses hormones.
6. **Harvest delay past trichome senescence** — overripe plants throw nanners.

If herming detected → identify the cause first, isolate the plant if seeds aren't wanted, and consider whether the genetics are worth keeping.

## Photoperiod Biology

Cannabis is a **short-day plant** (more accurately, a **long-night plant**) — it flowers when the uninterrupted dark period exceeds a critical threshold.

### Phytochrome System
Plants sense red and far-red light through **phytochromes** (PhyA, PhyB primarily). Phytochromes exist in two interconvertible forms:

- **Pr** — inactive form, absorbs red light at ~660 nm.
- **Pfr** — active form, absorbs far-red light at ~730 nm.

Red light pushes the population to Pfr. Far-red pushes it back to Pr. In darkness, Pfr slowly reverts to Pr over several hours.

When the dark period is long enough for Pfr to drop below a threshold, flowering hormones cascade. (Tier 1 — see Bugbee, Magagnini, Rodriguez-Morrison.)

### Critical Night Length
- **Most commercial cultivars require ~10–10.5 hours of uninterrupted darkness** to initiate and sustain flowering. (Tier 1 — Bugbee research at Utah State.)
- **Some equatorial landraces require 12+ hours of darkness** — the reason 12/12 became the indoor standard, since it works for nearly every cultivar.
- **4–5 days of exposure** to a sufficient short-day photoperiod commits the plant to flowering — the cascade isn't reversible after that without significant disruption.

### The Light Leak Myth (Bugbee)
Common forum advice says "any pinhole of light during dark phase will herm your plant." Bugbee's lab found cannabis cultivars **could not perceive light below ~10 nmol/m²/s** during the dark period — equivalent to a very dim moon. (Tier 1 — *Photons from NIR LEDs can delay flowering in short-day soybean and Cannabis*, 2021.)

Practical translation:
- A **bright moon, a phone screen briefly used, or a power-LED across the room** is below the threshold and will not herm.
- A **room light flicked on for minutes, a sliver of streetlight under a door, or a status LED inches from canopy** can exceed it and will delay/reverse flowering or herm.
- **Far-red (>700 nm) photons** can re-induce flowering after a red pulse — relevant for sunset-emulating spectra and some greenhouse interventions.

The threshold depends on cultivar sensitivity. Conservative growers black out fully anyway because the cost of leaks (a herming run) exceeds the cost of light-blocking material.

### Reverting and Re-Vegging
A plant pushed back to long-day light (18/6) mid-flower can revert to vegetative growth. The plant goes through a chaotic "re-veg" phase with twisted single-blade leaves before normalizing. Re-vegged plants are often saved for clone preservation, but yields and quality from a re-vegged plant are reduced — usually not worth doing intentionally.

## Autoflower Biology

Autoflowering cannabis derives its trait from **Cannabis ruderalis** — a small, weedy population from Eastern Europe / Central Asia adapted to short summer windows. Ruderalis-derived plants flower based on **age**, not photoperiod.

### How It Works
- A recessive autoflowering gene (or set of genes — incompletely characterized) shifts the flowering trigger from photoperiod-dependent to age-dependent.
- Modern feminized autos finish from seed in **8–12 weeks**, regardless of light schedule.
- Light schedule still matters for **growth speed and yield** — most growers run autos on **18/6 or 20/4 throughout the cycle** for maximum DLI.

### Trade-offs vs Photoperiod
| Auto pro | Auto con |
|---|---|
| Faster total cycle (8–12 wk vs 12–20 wk for photo) | Smaller plant size, lower per-plant yield |
| No light-schedule changes needed | Can't take effective clones (clones inherit the parent's age — flower immediately) |
| Stealth / outdoor multi-harvest | Less training tolerance — recovery time eats into limited veg |
| Easier for beginners | Genetics catalog smaller (though growing fast) |

**Don't top autos aggressively** — recovery time eats into the fixed flowering window. Light LST works; HST and topping are usually a net loss.

## Cannabinoid Biosynthesis

Cannabinoids are synthesized in **glandular trichomes** (capitate-stalked primarily) on female flowers. The core pathway (Tier 1 — *Phytocannabinoids: Origins and Biosynthesis*, Trends in Plant Science 2020):

```
Hexanoyl-CoA + 3× Malonyl-CoA
        │  TKS (tetraketide synthase)
        ▼
3,5,7-trioxododecaneoyl-CoA
        │  OAC (olivetolic acid cyclase)
        ▼
Olivetolic acid (OLA)
        │  Aromatic prenyltransferase + GPP
        ▼
CANNABIGEROLIC ACID (CBGA)  ← central branch point
        │
   ┌────┼────┐
   │    │    │
 THCAS CBDAS CBCAS  (FAD-dependent oxidocyclases)
   │    │    │
   ▼    ▼    ▼
THCA  CBDA  CBCA
   │    │    │
   │    │    │   (Decarboxylation: heat / time / light)
   ▼    ▼    ▼
THC   CBD   CBC
```

### Key Mechanisms

**THCAS, CBDAS, CBCAS** are FAD-dependent flavin-cofactor enzymes from the berberine bridge enzyme family. They oxidatively cyclize CBGA into the three major cannabinoid-acid lineages, each releasing hydrogen peroxide as a byproduct.

**Which cannabinoid lineage dominates** is genetically controlled — chemovar Type I (THC-dominant) plants have functional THCAS and non-functional CBDAS; Type III (CBD-dominant) is the reverse; Type II has both functional. (Tier 1 — *Profiling Cannabinoid Contents and Expression Levels*, 2022.)

**CBGA stays as CBG-line** if the plant has knocked-out THCAS, CBDAS, AND CBCAS — Type IV chemovars. Rare and breeder-interest.

### Decarboxylation (Acidic → Neutral)
Cannabinoids are produced as **acidic forms** (THCA, CBDA, CBCA) — these have a carboxylic acid (-COOH) group. They convert to the **neutral, "active" forms** (THC, CBD, CBC) by losing CO₂.

Triggers for decarboxylation:
- **Heat** — fast at 110°C+ (joints, vapes, baking).
- **Time** — slow drift during cure (few % per month at room temp).
- **UV light** — minor degradation pathway.

This is why **raw / fresh / juiced cannabis is non-intoxicating** — almost all the THC is locked as THCA. Smoke, vape, or bake = decarboxylation = activation.

### Minor Cannabinoids
- **CBN (cannabinol)** — degradation product of THC under prolonged heat / oxygen / UV. Mildly psychoactive, often associated with sedation. High-CBN flower = old or poorly-stored.
- **THCV / CBDV** — analogs with a propyl side chain (instead of pentyl). Come from a parallel **divarinic acid** pathway; show up in some African and Southeast Asian landraces.
- **CBG (cannabigerol)** — neutral form of CBGA. Significant in Type IV chemovars and as a minor in normal cultivars.

## Terpene Biosynthesis

Terpenes are the volatile aromatic compounds responsible for cannabis smell and a significant portion of the effect profile (entourage hypothesis). Cannabis produces **mono- and sesquiterpenes** primarily, via two distinct cellular pathways. (Tier 1 — Booth et al., *Terpene synthases from Cannabis sativa*, 2017; Booth & Bohlmann, *Terpene Synthases and Terpene Variation in Cannabis sativa*, 2020.)

### Two Pathways, Two Compartments
| Pathway | Cellular location | Precursor | Products |
|---|---|---|---|
| **MEP** (methylerythritol phosphate) | Plastid | Pyruvate + glyceraldehyde-3-phosphate → IPP / DMAPP → GPP | **Monoterpenes** (C10): myrcene, limonene, pinene, linalool, terpinolene, ocimene |
| **MVA** (mevalonate) | Cytosol | Acetyl-CoA → IPP → FPP | **Sesquiterpenes** (C15): β-caryophyllene, α-humulene, farnesene, nerolidol |

**TPS enzymes** (terpene synthases) — Booth et al. characterized 9 cannabis TPS in subfamilies TPS-a (sesquiterpene-producing) and TPS-b (monoterpene-producing). Different cultivars express different TPS gene sets, producing different terpene fingerprints. Chemovar terpene profile is therefore largely genetic, with environment as a modulator.

### Major Terpenes in Cannabis

| Terpene | Class | Aroma | Notable for |
|---|---|---|---|
| **Myrcene** | Mono | Earthy, musky, ripe fruit | Most abundant in many cultivars; shared with hops, mango |
| **Limonene** | Mono | Citrus, lemon | Common in "Lemon" / "Sour" cultivars |
| **α-Pinene** | Mono | Pine, fresh forest | Shared with conifers, rosemary |
| **β-Caryophyllene** | Sesqui | Pepper, spice, woody | Only known dietary cannabinoid-receptor binder (CB2) |
| **α-Humulene** | Sesqui | Earthy, hops-like | Co-expresses with caryophyllene |
| **Linalool** | Mono | Floral, lavender | Shared with lavender |
| **Terpinolene** | Mono | Fruity, herbal, complex | Dominant in some Jack Herer / Trainwreck lines |
| **Ocimene** | Mono | Sweet, herbal, woody | Common in some sativa-leaning cultivars |
| **β-Farnesene** | Sesqui | Sweet woody | Defense compound shared across many plants |

### Why Terpenes Are Easy to Lose
- **Monoterpenes (C10) are highly volatile** — boiling points 150–180°C; they evaporate at room temperature steadily, faster with heat or airflow.
- Drying at >21°C, curing in low-RH (<55%), and prolonged storage in light + heat all bleed terpenes.
- Sesquiterpenes (C15) are heavier and more stable — surviving terps in old flower lean caryophyllene-heavy.

This biology drives the dry / cure / storage protocols in `14-drying.md` and `15-curing.md`.

## Photosynthesis & Transpiration

### C3 Pathway (Brief)
Cannabis uses **C3 photosynthesis** — the standard temperate-plant carbon-fixation route. CO₂ enters the leaf via stomata and is fixed by RuBisCO into a 3-carbon intermediate (3-PGA), then converted to glucose via the Calvin cycle.

C3 limitations relevant to cultivation:
- **Photorespiration losses** at high temperatures (RuBisCO binds O₂ instead of CO₂ when leaf temp climbs).
- **CO₂-saturating** — adding CO₂ above ambient (~420 ppm) increases photosynthesis up to ~1500 ppm, with diminishing returns past 1200 ppm. Justification for sealed-room CO₂ supplementation. (Tier 1 — Chandra et al., Bugbee CO₂ research.)
- Optimal leaf-temperature window: **24–28°C with elevated CO₂; 22–25°C at ambient CO₂.** Above this, photorespiration eats yield.

### Stomatal Regulation
- **Stomata** are pores on leaf surfaces (mostly underside) that open and close to balance CO₂ uptake against water loss.
- **VPD (vapor pressure deficit)** drives stomatal behavior. Too low VPD (high RH) → stomata stay open but transpiration is throttled → poor nutrient delivery and PM risk. Too high VPD (low RH or hot/dry) → stomata close to conserve water → photosynthesis stalls.
- **Stomata are mostly closed in the dark** — minimal transpiration during lights-off. This is why night humidity targets allow higher RH than day targets.

See `02-environment.md` for VPD targets per stage.

### Transpiration → Nutrient Delivery
Transpiration is the water-vapor loss from stomata that pulls the **transpiration stream** up from the roots. This is the only mechanism that delivers **immobile nutrients (Ca, B, S)** to the upper plant. If transpiration crashes (high RH, no airflow, very low VPD), the plant develops Ca and B deficiencies even with adequate root-zone supply.

Practical implication: a Ca deficiency in late flower with a perfect feed schedule and pH is almost always an **airflow / RH problem**, not a feed problem. See `07-deficiencies.md`.

## Confusion / Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| "Indica" effect | Chemovar effect (terpene/cannabinoid mix) | Shelf labels are marketing; lab COA tells the truth |
| Ripe (lots of orange pistils) | Not ripe — pistils brown well before peak trichome maturity | Always read trichomes with a loupe or scope |
| Hermaphrodite from light leak | Genetics-driven herm | Stress-herms appear after a known event; genetic herms appear without provocation, often early |
| Intersex "nanners" near harvest | Late-flower senescence response | If single anthers and within 1 week of planned chop, harvest now and move on |
| Re-veg in flower | Severe phototropic disruption | Twisted single-blade leaves on top growth + return to vegetative phyllotaxy |
| Single-blade leaves on a clone | Re-veg from a flowering mother, not a defect | First true generation of leaves on a mid-flower clone is often single-bladed |
| Light-leak herm | Heat-stress herm | Light leak triggers timing-tied; heat triggers correlate with peak afternoon temps |
| THC = THCA in raw flower | Almost all the cannabinoid is THCA until heat decarboxylates it | Lab COA will report both; raw consumption ≠ heated consumption |
| "All trichomes are amber, harvest now" | Some chemovars push to amber faster — it's about the stalked trichomes, not the bracts | Sample multiple bract surfaces, not just one bud face |
| "Sativas need longer flower" | Sometimes true, but more about cultivar-specific genetics than sativa/indica labels | Breeder flowering time is the only reliable predictor |
| "Stretch is over" at week 3 | Some cultivars stretch into week 4–5, especially equatorials | Watch internodal expansion stop, not the calendar |

## Quick Reference

### Life-Cycle Timeline (Indoor Photoperiod, Typical)

| Stage | Duration | Light schedule | Key event |
|---|---|---|---|
| Germination | 1–10 days | Dark / dim | Radicle emerges |
| Seedling | 1–3 weeks | 18/6, low PPFD | First true leaves |
| Vegetative | 2–12 weeks | 18/6, ramp PPFD | Topping/training, sex shows in pre-flowers |
| Stretch | Weeks 1–3 of flower | 12/12 | 1.5–3× height gain |
| Bud formation | Weeks 3–6 of flower | 12/12 | Peak P/K demand |
| Ripening | Weeks 6–9+ of flower | 12/12 | Trichome amber-up |
| Harvest | 1 day | — | Chop |
| Dry | 7–14 days | Dark | Snap-test stem |
| Cure | 4+ weeks | Dark, sealed | Burp jars |

### Cannabinoid Pathway Flow

```
Hexanoyl-CoA + Malonyl-CoA → OLA → CBGA → [THCAS|CBDAS|CBCAS] → THCA|CBDA|CBCA
                                                                       │
                                                              decarboxylation
                                                                       ▼
                                                                THC|CBD|CBC
```

### Terpene Pathway Compartments

```
PLASTID (MEP)            CYTOSOL (MVA)
  │                        │
  GPP                      FPP
  │                        │
  TPS-b                    TPS-a
  │                        │
Monoterpenes             Sesquiterpenes
(myrcene, limonene,      (caryophyllene,
 pinene, linalool,        humulene,
 terpinolene, ocimene)    farnesene)
```

## Sources

**Tier 1 — Peer-reviewed:**
- Andre, C. M., Hausman, J. F., & Guerriero, G. — *Cannabis sativa: The Plant of the Thousand and One Molecules.* Frontiers in Plant Science, 2016.
- Booth, J. K., Page, J. E., & Bohlmann, J. — *Terpene synthases from Cannabis sativa.* PLOS ONE, 2017.
- Booth, J. K., & Bohlmann, J. — *Terpene Synthases and Terpene Variation in Cannabis sativa.* Plant Physiology, 2020.
- Bugbee, B. (Utah State University) — Cannabis lighting, photoperiod, and CO₂ research; multiple papers and the *USU Cannabis Pre-Print Series*.
- Chandra, S., Lata, H., ElSohly, M. — Cannabis biology, photosynthesis, CO₂ response (multiple papers).
- Gülck, T., & Møller, B. L. — *Phytocannabinoids: Origins and Biosynthesis.* Trends in Plant Science, 2020.
- Hillig, K. W. — *Genetic evidence for speciation in Cannabis (Cannabaceae).* Genetic Resources and Crop Evolution, 2005.
- McPartland, J. M. — *Cannabis Systematics at the Levels of Family, Genus, and Species.* Cannabis and Cannabinoid Research, 2018.
- Rodriguez-Morrison, V., Llewellyn, D., & Zheng, Y. — *Cannabis Yield, Potency, and Leaf Photosynthesis Respond Differently to Increasing Light Levels.* Frontiers in Plant Science, 2021.
- Small, E., & Cronquist, A. — *A practical and natural taxonomy for Cannabis.* Taxon, 1976.

**Tier 3 — Master growers / educators:**
- Cervantes, J. — *Cannabis Encyclopedia.*
- Clarke, R. C., & Merlin, M. D. — *Cannabis: Evolution and Ethnobotany.* University of California Press, 2013.
- DeBacco University (YouTube) — Penn State horticulture lectures on cannabis.
- Rosenthal, E. — *Marijuana Grower's Handbook.*

## Cross-References

- Cultivar selection / strain biology → `01-genetics-strains.md`
- VPD, temperature, and humidity targets per stage → `02-environment.md`
- PPFD, DLI, and DLE → `03-lighting.md`
- Pre-flower training (topping, LST, mainline) → `10-training.md`
- Photoperiod transition mechanics and stretch management → `12-flowering.md`
- Trichome reading at harvest → `13-harvest.md`
- Drying terpene-preservation environment → `14-drying.md`
- Mobile vs immobile nutrient symptoms → `07-deficiencies.md`
- Seedling overwatering and root-zone management → `04-medium-soil.md`, `04-medium-coco.md`
