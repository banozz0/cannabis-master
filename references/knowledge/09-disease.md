# 09 — Disease

Diseases are the third leg of the plant-health triangle (with `07-deficiencies.md` and `08-pests.md`). They overlap heavily with pests — caterpillar entry seeds *Botrytis* infections; mite-stressed plants are more susceptible to root rot; thrips vector viruses. And they overlap with the environment file — RH and airflow are the master disease-prevention levers, more powerful than any spray. Cross-reference with `08-pests.md` (pest damage opens entry for pathogens — bud rot frequently follows caterpillar feeding), `02-environment.md` (the disease triangle's environmental corner is where most prevention happens), `04-medium-soil.md` / `04-medium-coco.md` / `04-medium-hydro.md` / `04-medium-living-soil.md` (each medium has different root-zone disease risk), `01-genetics-strains.md` (HLVd specifically — clonal genetics carry it forward indefinitely), `references/workflows/diagnose-from-photo.md` (require macro photos for fungal ID; PCR test recommendation for viroids).

## How to Use This File

1. **Rule out abiotic FIRST** — heat, light bleach, cold stress, water stress. Most "disease" calls are environmental.
2. **Identify pathogen class** before treating — fungi, oomycetes, bacteria, viruses, viroids each need different responses.
3. **Confirm with appropriate diagnostic** — visual + magnification for fungi, lab test for some bacteria, PCR for viroids and viruses. Don't guess on viroids — they have no symptoms early.
4. **Don't shotgun fungicides at viral problems** — wrong category; only sanitation + culling work for viruses/viroids.
5. **Treat the root cause** — environmental conditions usually. A spray that "fixes" PM in a 70% RH room is just suppressing while the conditions reload.
6. **Stop foliar sprays at week 2–3 of flower** — same rule as pests; flower-stage chemistry persists into product.

## Critical Concept — The Disease Triangle

For plant disease to develop, three conditions must align simultaneously:

```
        Susceptible HOST
              /\
             /  \
            /    \
           / DISEASE \
          /          \
         /____________\
   Virulent          Conducive
   PATHOGEN          ENVIRONMENT
```

- **Host**: cannabis genotype, stage, stress state
- **Pathogen**: present, in active phase, virulent
- **Environment**: RH, temp, leaf wetness, airflow, root-zone conditions

**Break ANY corner → disease doesn't develop.**

In cannabis, the most achievable corner to break is environment — RH below 50% in late flower stops Botrytis cold; PM struggles below 60% RH; Pythium needs warm wet root zones. Genotype changes (host corner) take a season to swap. Eliminating pathogen presence (pathogen corner) is hard once established. Environment is where 80% of preventive work pays off.

## Critical Concept — Pathogen Classification

Parallel to mobile/immobile in `07` and above-soil/in-soil in `08`. Pathogen class dictates treatment paradigm.

| Class | Examples | Treatment paradigm |
|---|---|---|
| **Fungi (true — Ascomycota, Basidiomycota)** | Botrytis, Powdery Mildew, Fusarium, Septoria, Aspergillus | Biofungicides, contact fungicides, environmental control |
| **Oomycetes (water molds — Stramenopiles, NOT fungi)** | Pythium, Phytophthora, downy mildew | Different chemistry — most fungicides miss them; root-zone hygiene + DO + Bacillus biocontrol |
| **Bacteria** | Pseudomonas, Xanthomonas, Erwinia | Copper-based, sanitation, environmental — rare in cannabis |
| **Viruses** | TMV, LCV, BCTV, TSWV, CanCV | NO TREATMENT — prevention + vector control + culling |
| **Viroids** | HLVd | NO TREATMENT — testing, culling, tissue-culture meristem cleanup, **resistant to standard sterilizers** |

**Why oomycetes deserve their own row:** they look like fungi (microscopic mycelium) but are taxonomically closer to brown algae. Standard fungicides (sulfur, copper, neem) often miss them. Mefenoxam/Subdue is the chemistry-based answer (flower-incompatible). For cannabis, the practical answer is *Bacillus amyloliquefaciens* prophylactic + DO + environment.

## Critical Concept — Stage Vulnerability Map

| Stage | Highest-risk diseases | Why |
|---|---|---|
| Germination / seedling | Damping off (Pythium, Rhizoctonia) | Wet seedling stem rots overnight |
| Veg | Powdery mildew, Pythium root rot, Fusarium wilt | High RH; warm wet root zones |
| Stretch / early flower | Powdery mildew (peak window) | Canopy closing, RH rising in dense stretch |
| Mid-flower (week 3–5) | PM persists, early Botrytis signs | Bud-set, density increasing |
| Late flower (week 6+) | **Botrytis bud rot** (#1 late-flower threat), bud calyx PM | Dense buds + cooler nights + transpiration moisture |
| Drying | Aspergillus, Penicillium, residual Botrytis | Wrong RH/temp during dry can spawn molds |
| Mother plants / clones | HLVd, Fusarium chronicles | Long-term carrier reservoir; sanitation drift over years |

## Critical Concept — Environmental Setpoints for Disease Prevention

Cross-ref `02-environment.md` for full physiology context. These are the disease-specific targets.

| Stage | RH target | Temp target | Hard rule |
|---|---|---|---|
| Seedling | 65–70% | 75–80°F | Drainage + airflow; dome ventilation daily |
| Veg | 55–65% | 75–82°F | PM prevention starts <60% |
| Stretch | 50–60% | 75–80°F | Drop RH 5% from veg week-by-week |
| Mid-flower | 45–55% | 72–78°F | Botrytis prevention engaged |
| Late flower | 40–50% | 68–75°F | Aggressive RH drop; below 50% mandatory in week 6+ |
| Last 2 weeks | 40–45% | 65–72°F | Keep night temps from condensing on buds |

**Hard environmental rules for disease prevention:**
- **Leaf wetness >6 hours = fungal disease window.** Foliar spray at lights-on, never lights-off, never above 60% RH.
- **Air movement at canopy = disease prevention.** Visible leaf flutter at every layer; Punja showed direct fan-on-buds reduces RH and total mold counts (Tier 1 — Punja Botrytis epidemiology research).
- **No condensation surfaces.** Cool walls + warm air = water beads = pathogen entry. Insulate or heat the cool surface.
- **Defoliate strategically.** Remove fan leaves blocking airflow into bud zones at week 3 of flower; remove bottom-third of plant for the "lollipop" airflow pattern.

---

## FUNGAL DISEASES — Per-Item Deep Profiles

### Botrytis cinerea (Gray Mold / Bud Rot) — the #1 flower-destroyer

**Pathogen:** *Botrytis cinerea*, Ascomycota; ubiquitous, polyphagous (infects 200+ plant species). Spores are airborne, present in virtually every grow environment — the question is whether conditions activate them.

**Identification:**
- Early: water-soaked / wet-looking spot on calyx or inner bud — visible only by breaking dense buds open
- Mid: brown to gray fuzzy mycelium grows from interior, leaf petiole at bud base browns
- Advanced: dense gray-brown velvet of spores (the "gray mold" namesake), buds collapse and crumble
- Diagnostic shortcut: gently tug at suspect bud — if a section pulls free easily and inside is brown/fuzzy = Botrytis

**Conditions favored (Tier 1 — Punja, *Canadian Journal of Botany* 2023; *Canadian Journal of Plant Pathology* 2025):**
- Spore germination optimum: 11–16°C (52–61°F), RH >97% (effectively at leaf surface during night transpiration condensation)
- Visible mycelium / sporulation: 11–16°C, RH >80%
- Active flower destruction: 17–24°C, RH >70%
- Practical translation: any time leaf or bud surface is wet for 6+ hours, a Botrytis event is possible

**Lifecycle:**
- Spores land, germinate when wet film present on tissue, penetrate through wounds or natural openings
- Caterpillar feeding wounds are the #1 entry point in outdoor / greenhouse (Tier 1 — Punja, Cranshaw confirms)
- Once inside, mycelium spreads rapidly through dense bud tissue
- Mature mycelium produces millions of new spores → atmospheric spore load increases → adjacent buds infect

**Confusion risk:**
- Pin rot / bud calyx senescence (natural late-flower fade) — calyx browns but no mycelium; not contagious
- Aspergillus / Penicillium (different molds; different colors — Aspergillus more khaki-yellow, Penicillium blue-green)
- Caterpillar damage alone (frass without mycelium = caterpillar; both = caterpillar + Botrytis follow-on)

**Treatment ladder:**
- **Cultural** (the only reliable defense once flowering):
  - RH 40–50% mid- to late-flower (Tier 1 — Punja recommended)
  - Direct fan-on-buds (Punja showed reduces RH, temp, and total mold counts)
  - Remove infected buds with sterile tools, double-bag and dispose offsite — don't compost on premises
  - Strategic defoliation week 3 of flower for canopy penetration
  - Genetics: some genotypes far more susceptible than others — drop the worst-hit cultivars
- **Biological / Biofungicide**:
  - *Bacillus subtilis* QST713 (Cease, Serenade) — preventive foliar in early flower
  - *Bacillus amyloliquefaciens* (Stargus) — also Botrytis suppression
  - *Gliocladium catenulatum* (Prestop) — Botrytis-targeted antagonist
  - *Reynoutria sachalinensis* extract (Regalia / Procidic) — induced systemic resistance, OMRI-listed, cannabis-cleared in multiple states
- **Botanical / Mineral**: potassium bicarbonate (Milstop) — surface contact only, late-flower-cautious
- **No-go**: Eagle 20EW (myclobutanil) is banned in legal cannabis — converts to hydrogen cyanide on combustion (Tier 1 — multiple state lab confirmations)

**Stage-safe options:**
- Veg: full ladder
- Early flower: biocontrols + environmental
- Mid-flower: environmental + spot-removal of any infected tissue
- Late flower / last 2 weeks: hand-removal only, accept losses, harvest early if widespread

### Powdery Mildew (Golovinomyces ambrosiae and others)

**Pathogen taxonomy update:** the cannabis-infecting PM was historically called *Sphaerotheca macularis* or *Podosphaera macularis* by hop researchers, then *Golovinomyces cichoracearum* sensu lato or *G. spadiceus*. Modern molecular taxonomy confirms the dominant species is **Golovinomyces ambrosiae** (Tier 1 — APS *Plant Disease* first reports: Oregon 2020, Quebec 2022; Mieslerová et al. 2024 *Journal of Phytopathology* confirmed co-occurrence of two species in field). Hop powdery mildew (*Podosphaera macularis*) has also been confirmed naturally infecting cannabis in field conditions (Tier 1 — Punja 2021).

**Identification:**
- White flour-like dusty patches on leaf surface, expanding outward in circular colonies
- Initially few small spots; rapidly spreads if RH stays high
- Often starts in dense canopy where airflow is poor
- Late stage: yellowing, leaf drop; bud calyx infection in flower

**Conditions favored:**
- RH 60–85% (yes — PM doesn't need ultra-high RH like Botrytis)
- Moderate temps 65–80°F
- Low airflow + dense canopy + cool nights with daytime warmth (the PM "alternation")
- Greenhouse cultivation in spring/fall is peak risk

**Confusion risk:**
- Trichome accumulation in late flower (PM spreads colony-like; trichomes are uniform on bud, slightly oily)
- Silica spots on leaves (silica: dry, isolated, doesn't spread; PM: spreading colonies)
- Powdery sugar / dust contamination (wipes off; PM regrows after wiping)

**Treatment ladder:**
- **Cultural**: RH <60%, defoliate dense canopy, direct airflow at every layer, sanitize tools, quarantine clones (clone-borne is common entry route)
- **Biological**: *Bacillus subtilis* QST713 (Cease) preventive weekly in veg/early flower
- **Biofungicide**: **Regalia (Reynoutria sachalinensis extract)** — gold-standard cannabis biofungicide for PM; OMRI-listed; ISR mechanism (Tier 2 — Marrone Bio / Pro Farm trials show "superior PM control" cannabis/hemp)
- **Mineral**: 
  - Potassium bicarbonate (Milstop) — contact, surface kill, veg + early flower
  - Sulfur dust or sulfur burner — veg only; never within 14 days of oils
  - Citric acid foliar at 1–2% — mild contact treatment
- **Botanical**: cinnamon oil, rosemary oil — soft preventives, low effect alone
- **Last resort / not for legal cannabis**: Eagle 20 (myclobutanil) — banned, see Botrytis section

**Stage-safe options:**
- Veg: full ladder including sulfur
- Early flower: biofungicides only; no sulfur if oils used recently
- Mid-flower+: Regalia, *Bacillus subtilis*, environmental only
- Late flower: hand-removal of affected leaves, environmental, accept losses

### Fusarium spp. (Root Rot + Wilt)

**Pathogens:**
- *Fusarium oxysporum f. sp. cannabis* — vascular wilt, NO root rot (Tier 1 — Punja 2020 *Canadian Journal of Plant Pathology*)
- *F. oxysporum* (non-special form) — root browning + crown infection
- *F. solani* — root rot complex
- *F. proliferatum* — also reported on cannabis

**Identification (wilt form):**
- Lower leaves yellow, wilt — often **unilateral** (one side of plant affected) — diagnostic "half-leaf" pattern
- Wilting persists despite watering (xylem blockage)
- Cut stem reveals **reddish-brown vascular streaks** — diagnostic confirmation
- Plant decline progressive over 1–4 weeks

**Identification (root rot form):**
- Root browning, cortex sloughs off if pulled
- Crown rot at soil line — stem brown and soft at base
- Reduced vigor, intermittent wilt, slow nutrient response

**Conditions favored:**
- Persistent in soil (years) — once present, hard to eliminate
- Warm root zones (>75°F) accelerate
- Wet substrate, poor drainage
- Plant stress (over/under fertilization, drought) increases susceptibility

**Confusion risk:**
- Wilt vs underwatering (underwater recovers in hours; wilt persists)
- Pythium root rot (Pythium: brown slimy roots, often acute; Fusarium: progressive wilt + vascular streaks)
- N deficiency lower-leaf yellowing (N def: bilateral, gradual; Fusarium: unilateral, wilting)

**Treatment ladder:**
- **Cultural**: 
  - Remove + dispose entire plant including root ball (do NOT shake — releases spores)
  - 4-year rotation away from cannabis if outdoor (Tier 1 — USU Extension, OSU)
  - Disinfest containers and tools with 10% bleach
  - Pathogen-free seed in pathogen-free media for new starts
- **Biological**:
  - *Trichoderma harzianum* — root-zone antagonist, preventive at transplant
  - *Streptomyces lydicus* (Actinovate) — soil drench preventive
  - *Bacillus amyloliquefaciens* (Hydroguard, Stargus) — Tier 1 — Punja 2023 trials show 30–56% disease severity reduction in cannabis Fusarium/Pythium
  - *Gliocladium virens* — competitive exclusion in soil
- **Botanical / Mineral**: cinnamon oil soil drench, mustard meal as biofumigant (cover crop)
- **Synthetic / flower-incompatible**: propiconazole, thiophanate-methyl — banned/discouraged for legal cannabis residue testing

**Stage-safe options:**
- Best done preventively at transplant (Trichoderma, Hydroguard inoculation)
- Once visible: cull and dispose, no in-flower treatment is reliable

### Septoria cannabis (Yellow Leaf Spot)

**Identification:**
- Round to angular brown/tan spots with yellow halo on leaves
- Lower leaves first, works upward
- Spots may have dark concentric rings (pycnidia — fungal fruiting bodies)
- Mostly outdoor/greenhouse

**Conditions favored:** warm wet conditions, splashing water from rain or overhead irrigation, dense canopy.

**Treatment:**
- Cultural: drip irrigation only (no overhead water), remove infected lower leaves, mulch to prevent splash
- Biological: *Bacillus subtilis*, Regalia
- Mineral: copper-based (cannabis-cautious)

### Damping Off (Pythium + Rhizoctonia at Seedling)

**Pathogens:** *Pythium ultimum*, *P. aphanidermatum*, *Rhizoctonia solani* — all common nursery pathogens.

**Identification:**
- Pre-emergence: seeds rot in soil, never sprout
- Post-emergence: stem at soil line darkens, pinches, seedling falls over and dies — overnight
- Survivors stunted, sluggish

**Conditions favored:** wet seedling tray, low airflow, warm humid dome, contaminated media.

**Treatment:**
- Cultural: drainage, ventilate dome 2× daily, sterile media, quality seeds
- Biological: pre-soak seeds in *Trichoderma* solution; Hydroguard in propagation water at half strength
- Don't replant in contaminated media — full reset

### Bud-Stage Side Issues — Aspergillus, Penicillium, Pin Rot (Quick reference)

| Issue | ID | Treatment shortcut |
|---|---|---|
| **Aspergillus** | Khaki-yellow fuzzy mold; serious health concern (mycotoxins) | Cull, dispose; cannabis testing programs flag this |
| **Penicillium** | Blue-green fuzzy mold during dry/cure | Improve drying environment; cull affected; lower RH during cure |
| **Pin rot** | Single calyx browns then dies — often genetic / heat | Often confused with early Botrytis; remove and monitor |
| **Sclerotinia (white mold)** | Fluffy white mycelium on stems, sclerotia (black hard bodies) | Rare in cannabis; cultural + Bacillus |

---

## OOMYCETE DISEASES

### Pythium Root Rot (Pythium aphanidermatum, P. myriotylum, P. ultimum)

The dominant cannabis water-mold pathogen. (Tier 1 — Punja 2018, 2021 *Canadian Journal of Plant Pathology*; first reports from Florida 2025, Arizona 2021 in *Plant Disease*.)

**Identification:**
- Roots brown, slimy, easily slough off when handled
- Lower stem may darken at substrate level
- Plants wilt despite wet substrate (roots can't absorb)
- Leaves yellow then drop
- Smell: sour, swampy (anaerobic)
- Acute death possible in 24–48 hours under warm conditions

**Conditions favored:**
- Warm root zones (>72°F) — *P. aphanidermatum* loves warmth
- Low dissolved oxygen (DO) in hydro
- Stagnant nutrient solution, dirty res
- Wet substrate without dry-back cycles in soil/coco
- Any organic debris in res or substrate

**Confusion risk:**
- Overwatering (root color: overwater = yellow-brown; Pythium = brown slimy)
- Fusarium root rot (Fusarium: progressive; Pythium: often acute)
- Nutrient burn root damage (chemical burn = white root tips browning; Pythium = whole root system slimy)

**Treatment ladder:**
- **Cultural / environmental**:
  - Drop res temp to 65–68°F (Pythium slows below 70°F)
  - Aerate aggressively — DO target >6 ppm
  - Clean res, replace solution, sanitize lines
  - In soil: dry back fully between waterings
- **Biological** (the gold standard):
  - **Hydroguard / Stargus (*Bacillus amyloliquefaciens* D747)** — preventive at every res change; cornerstone of clean DWC. (Tier 1 — Punja 2023 trials confirm 30–56% disease severity reduction in cannabis)
  - *Trichoderma harzianum* — root colonizer, competitive exclusion
  - *Streptomyces lydicus* (Actinovate) — soil/coco drench
  - *Glomus / Mycorrhizae* — root-tip protection
- **Biofungicide**: Regalia ISR
- **Synthetic / flower-incompatible**: Mefenoxam (Subdue, Ridomil) — oomycete-specific, banned in legal cannabis for residue
- **Last resort**: H₂O₂ at 1–3% in res for 24 hours emergency knockdown — kills biology, reset only

**Critical note:** for any DWC / RDWC system, *Bacillus amyloliquefaciens* prophylactic at every res change is the single most cost-effective disease prevention. It's not optional in commercial DWC.

### Downy Mildew

Rare in cannabis but emerging — different fungus from PM despite similar name. Yellow patches on leaf top, fuzzy gray-purple sporulation on leaf underside (PM is white on top). Treat similarly to PM but pay special attention to oomycete-targeted options.

### Phytophthora

Outdoor / greenhouse stem and root rot. Less common in indoor cannabis. Treatment overlaps with Pythium — *Bacillus*, Trichoderma, environmental.

---

## BACTERIAL DISEASES

### Pseudomonas / Xanthomonas Leaf Spots

**Identification:**
- Water-soaked spots with yellow halo
- Spots may darken to brown/black; angular limited by leaf veins (vs round Septoria spots)
- Bacterial ooze visible under microscope on cut edge
- Less common in indoor cannabis than fungal/oomycete

**Treatment:**
- Cultural: sanitation, no overhead water, prune affected
- Mineral: copper-based (cannabis-cautious — use sparingly, residue concerns)
- Biological: *Bacillus subtilis* shows some efficacy

### Crown Gall (Agrobacterium tumefaciens)

Rare cannabis report. Tumor-like galls on stems near soil. Cull plant; don't replant in same soil for 2 years.

---

## VIRAL & VIROID DISEASES — Critical Commercial Section

### Hop Latent Viroid (HLVd) — "Dudding Disease"

**The single most important disease topic for commercial cannabis 2018–2026.** What follows is intentionally exhaustive.

**Pathogen:**
- A 256-nucleotide circular RNA — no protein coat (Tier 1 — Adkar-Purushothama et al., Université de Sherbrooke; multiple PMC publications 2023–2024)
- Originally identified in hops, now most commercially significant pathogen in cannabis
- Many commercial mother-stock libraries carry it asymptomatically

**Symptoms (when expressed — many infections stay latent):**
- Stunting and reduced internode length
- "Duck-foot" leaf deformity (leaflets fused or deformed)
- Brittle, hollow stems
- Reduced trichome production, dull/dusty bud appearance
- **20–30% reduction in cannabinoid production** (Tier 1 — multiple peer-reviewed surveys)
- **20–30% reduction in yield**
- Plants often look "tired" or "underperforming" without obvious cause
- Symptoms often only appear under stress (transplant, training, light flip)

**Asymptomatic carriers are the problem.** A mother plant can be HLVd-positive and look fine for years, producing thousands of infected clones, until finally one clone batch underperforms and the test reveals contamination throughout the library.

**Transmission routes (Tier 1):**
- **Clonal (primary)** — every cutting from an infected mother is infected
- **Mechanical (cutting tools, hands)** — viroids stable on surfaces; cross-contamination during pruning, cloning, training
- **Root-to-root in shared hydroponics** — confirmed in DWC / fertigation systems
- **Pollen and seed** — anthers and pollen from infected males are infected; up to 100% of seedlings from infected female × infected male are HLVd-positive
- **NOT vector-borne** (no insect transmission confirmed)

**Detection (Tier 1 — Medicinal Genomics / TumiGenomics / Front Range Bio / Phylos / MyFlora DNA / Norgen Biotek):**
- **qPCR (TaqMan RT-PCR)** is the gold standard — sensitive to 5 picograms total RNA
- Test cost: $30–80 per sample at major labs
- Sample type: leaf tissue, ~2–4 cm² per plant
- Turnaround: 24–72 hours
- Major commercial labs: Medicinal Genomics, TumiGenomics, MyFloraDNA, Phylos, Front Range Biosciences
- Visual diagnosis is unreliable — test, don't guess

**Treatment — there isn't one. But there are protocols:**
1. **Cull infected plants and substrate.** Not "treat" — remove.
2. **Sanitize tools between plants** with 10% bleach OR Virkon S OR ZeroTol OR hypochlorous acid — **but note: NONE of these destroy HLVd in plant tissue** (Tier 1 — Medicinal Genomics research: HLVd resistant to bleach, Virkon, ZeroTol, hypochlorous acid, UV-C, and heat to 70°C). Sanitizers only prevent surface transmission — they do not save infected plants.
3. **Tissue-culture meristem cleaning** — the only known cure for genetics worth saving:
   - Take meristem tip <0.5 mm
   - Combined with cold treatment (2–4°C in dark for 8–21 months) more effective than meristem alone (Tier 1 — published 2024 protocols)
   - Total process: 12–16 months from infected mom to confirmed-clean clone
   - Re-test multiple times — HLVd not uniformly distributed in tissue culture; replication may delay then re-emerge
   - Not all genetics survive — the more stress, the more loss
4. **Replace mother stock with confirmed-clean meristem-cleaned stock** when feasible. For most operations this is cheaper than tissue culture in-house.

**Prevention protocol for clean facility:**
- Test every mother quarterly (or every clone batch if rotating)
- Test every incoming clone at 14-day quarantine before introducing to flower room
- Test seedlings if starting from seed of unknown parentage
- One-way workflow: clean room → propagation → veg → flower (no reverse handling)
- Tools per plant or sterilize between plants — soak in 10% bleach 10 minutes minimum
- New gloves between plants when cloning / training mom plants
- Quarantine + PCR test any clone gift, seed pack, or new genetics before introducing to facility

**Why HLVd is "the COVID of cannabis":**
- Asymptomatic spread
- Widespread before recognition
- No effective treatment
- Detection requires lab test
- Best response is testing + isolation + replacement of infected stock

(Sources throughout — Tier 1: Adkar-Purushothama et al.; Bektaş, A. et al. 2019 *Frontiers in Microbiology*; Punja viroid surveys; Phylos Bioscience discovery announcement 2019. Tier 2: Medicinal Genomics technical documentation; TumiGenomics protocol whitepapers.)

### Other Viral / Viroid Diseases

| Disease | Pathogen | Vector / spread | Symptoms | Treatment |
|---|---|---|---|---|
| **Lettuce Chlorosis Virus (LCV)** | LCV crinivirus | Whiteflies (*Bemisia tabaci*) | Interveinal chlorosis on lower leaves | None — vector control + cull |
| **Beet Curly Top Virus (BCTV)** | BCTV geminivirus | Beet leafhopper | Stunting, leaf curling, rosette growth | None — outdoor screening, cull |
| **Tobacco Mosaic Virus (TMV)** | TMV tobamovirus | Mechanical, smoking residue on hands | Mosaic mottling, leaf deformity (rare confirmed in cannabis) | None — sanitation, no smoking around plants |
| **Cannabis Cryptic Virus (CanCV)** | CanCV partitivirus | Vertical transmission only (no spread) | Largely asymptomatic | None — generally considered benign |
| **Tomato Spotted Wilt Virus (TSWV)** | TSWV tospovirus | Western Flower Thrips | Necrotic ringspots, stunting | None — thrips control, see `08-pests.md` |
| **Cucumber Mosaic Virus (CMV)** | CMV cucumovirus | Aphids (60+ species) | Mosaic mottling, stunting | None — aphid control, cull |

**Master rule for all viral/viroid:** test → cull → sanitize tools and surfaces → replace stock with tested-clean material. There is no spray. Test the mom, cull the bad ones, work clean.

---

## ABIOTIC LOOK-ALIKES (Rule These Out FIRST)

| Looks like disease | Actually | How to tell |
|---|---|---|
| White leaf bleaching | Light burn at top canopy | Symmetric across canopy top, only top leaves; raise fixture |
| Yellow blotchy patches | Heat stress | Top of canopy hottest; check leaf-surface temp |
| Purpling stems / leaves | Cold root zone or genetics | Check temp; some strains naturally purple |
| Brown leaf edges | Wind/airflow burn | Leaves directly in fan path; redirect air |
| Tip burn | Salt buildup or light burn | See `07-deficiencies.md` |
| Chlorosis (general yellowing) | N deficiency or pH lockout | See `07-deficiencies.md` |
| Curled leaves | Heat / VPD off / genetics | See `02-environment.md` |
| Drooping with no color change | Watering issue | See `04-medium-*.md` |

If any of these explanations fit, fix the abiotic cause first. Don't spray fungicide at heat damage.

---

## IPM Treatment Toolkit — Disease-Specific

### Cultural / Environmental (the master tier)

| Tool | Application |
|---|---|
| **RH management** | The #1 lever — see Environmental Setpoints table above |
| **Airflow at canopy** | Visible leaf flutter every layer; fan-on-buds direct in late flower (Punja recommended) |
| **Defoliation** | Week 3 of flower for canopy penetration; bottom-third "lollipop" |
| **Sanitation between cycles** | 10% bleach OR ZeroTol 2.0 OR Virkon S — full surfaces, fan blades, ducting |
| **Quarantine + PCR testing** | Mandatory for HLVd; 14-day minimum quarantine for new genetics |
| **UV-C light sterilization** | Between cycles only, not on plants; varies in dose by pathogen |
| **One-way workflow** | Clean → propagation → veg → flower; no reverse handling |
| **Tool sterilization between plants** | 10% bleach soak 10 minutes for HLVd-conscious work |
| **Genetics culling** | Drop susceptible cultivars; Botrytis-prone genetics not worth keeping |

### Biological / Biofungicides (the cornerstone of cannabis disease IPM)

| Product | Active ingredient | Target | Notes |
|---|---|---|---|
| **Hydroguard / Stargus** | *Bacillus amyloliquefaciens* D747 | Pythium, Fusarium, root rot | Preventive at every res change; mandatory for clean DWC |
| **Cease / Serenade** | *Bacillus subtilis* QST713 | Botrytis, PM, foliar pathogens | Weekly preventive in veg / early flower |
| **RootShield / Tenet** | *Trichoderma harzianum / virens* | Pythium, Fusarium, Rhizoctonia | At transplant; long-term root colonizer |
| **Actinovate** | *Streptomyces lydicus* | Pythium, Fusarium, Rhizoctonia | Soil drench preventive |
| **Prestop** | *Gliocladium catenulatum* | Botrytis, Pythium | Foliar + soil application |
| **Regalia / Procidic** | *Reynoutria sachalinensis* extract | Powdery mildew (gold standard), Botrytis | ISR mechanism; OMRI-listed; cannabis-cleared multiple states |
| **Mycorrhizae** | *Glomus, Rhizophagus* spp. | Root protection (general) | Inoculate at transplant; not a cure but a defense |

### Botanical / Mineral

| Product | Target | Stage | Notes |
|---|---|---|---|
| **Sulfur (dust, spray, burner)** | PM | Veg only; never within 14 days of oil | Burner overnight in empty room between cycles |
| **Potassium bicarbonate (Milstop)** | PM contact | Veg + early flower | Surface kill; no residual |
| **Copper-based (Cu hydroxide, Cu sulfate)** | Bacterial spots, downy mildew | Veg only; cannabis-cautious for residue | Use sparingly — residue concerns |
| **Cinnamon oil** | Soil-borne pathogens, mild PM | Any stage | Soft, soil drench |
| **Citric acid (1–2%)** | PM mild contact | Veg | Foliar surface treatment |
| **Hydrogen peroxide (3%)** | Emergency root zone reset | Reset only — kills biology | Use only when biological approach has failed |

### Synthetic Chemistry — Flower-Incompatible / Banned in Legal Cannabis

| Product | Banned/restricted because |
|---|---|
| **Eagle 20EW (myclobutanil)** | Converts to hydrogen cyanide on combustion — banned for combustible cannabis (Tier 1 — multiple state lab confirmations) |
| **Mefenoxam (Subdue, Ridomil)** | Oomycete-specific; cannabis residue test failures |
| **Propiconazole** | Cannabis residue test failures |
| **Thiophanate-methyl** | Same |
| **Avid / Forbid (acaricides)** | Listed under pests; fungicidal effect minimal anyway |

**For commercial cannabis:** test program limits typically 0.05 ppm. One spray of any of the above in late veg fails flower test 8–10 weeks later. The right play is biologicals + environmental + Regalia.

---

## Sterilization Protocols Between Cycles

### Standard sterilization (kills most pathogens)

| Sanitizer | Active ingredient | Contact time | Notes |
|---|---|---|---|
| **10% bleach** | 0.5–1% sodium hypochlorite | 10 minutes minimum | Cheapest; corrodes metal; not EPA-registered for greenhouse |
| **ZeroTol 2.0** | Hydrogen dioxide + peroxyacetic acid | Per label | EPA-registered; cannabis-cleared; surfaces + reservoirs |
| **OxiDate 2.0** | Same chemistry as ZeroTol | Per label | Same use case |
| **SaniDate 5.0** | Hydrogen peroxide | Per label | Organic-certified |
| **Virkon S** | Potassium peroxymonosulfate | 10 minutes | EU-standard; broad spectrum |
| **Green-Shield II / Physan 20** | Quaternary ammonium | Per label | Surface only, less for biology |
| **Hypochlorous acid (HOCl)** | Stabilized | Per label | Newer plant-safe option; gentle |

### CRITICAL HLVd-specific note (Tier 1 — Medicinal Genomics research)

**HLVd is NOT destroyed by bleach, Virkon, ZeroTol, hypochlorous acid, UV-C, or heat to 70°C.** Standard sterilizers prevent surface transmission only — they do not save infected plants.

For HLVd specifically:
- Sanitizers prevent **between-plant** transmission of viroid present on tools/surfaces
- Sanitizers do NOT remove viroid from infected plant tissue
- The only known cure is meristem tissue culture (cold + meristem <0.5 mm)
- One-way workflow + PCR testing + isolation are the practical protocol
- Replace infected mother stock with tested-clean stock — don't try to "clean" infected moms

### Between-cycle full reset protocol

1. Remove all plants and substrate from room
2. Vacuum dust, debris, leaves
3. Surface scrub all surfaces with 10% bleach OR ZeroTol — 10-minute contact
4. Clean fan blades (often missed) — pathogen reservoir
5. Clean HVAC filters and ducting if accessible
6. Replace fabric pots OR hot-wash with bleach
7. Clean hydroponic res, lines, drippers — chlorine flush 30 minutes
8. **Sulfur burner overnight (6–8 hours) with no plants in room** — kills mite eggs + PM spores
9. Run UV-C lamps in empty room 12+ hours
10. Air out, neutralize (open ventilation 24 hours)
11. Wipe walls with hypochlorous acid for residual surface
12. **Restock with tested-clean genetics only**

---

## Quick Reference — Diagnostic Tree

```
START → Rule out abiotic FIRST
  ├── Top canopy white/yellow → light burn (raise fixture)
  ├── Heat damage at top → drop temp / PPFD
  ├── Cold-related purpling → check root zone temp
  ├── Wind/airflow burn → leaf in direct fan path
  └── Pure droop, no color → watering issue, not disease

If NOT abiotic → identify pathogen class.

LEAVES?
├── White flour-like patches spreading → Powdery Mildew (Golovinomyces)
├── Brown spots with yellow halo, lower leaves → Septoria
├── Mosaic mottling, distorted growth → Virus (PCR test)
├── Duck-foot deformity, stunting, multiple plants → HLVd (PCR test mandatory)
├── Water-soaked angular spots → Bacterial leaf spot (Pseudomonas/Xanthomonas)
└── Yellowing one side only → Fusarium wilt (cut stem to confirm vascular streaks)

BUDS?
├── Gray-brown fuzzy mold inside dense bud → Botrytis bud rot
├── Khaki-yellow fuzzy mold → Aspergillus (cull and dispose)
├── Blue-green mold during cure → Penicillium (improve drying)
├── Single calyx browns → pin rot (often genetic) or early Botrytis
└── Bud + caterpillar frass → caterpillar damage + Botrytis follow-on (see 08-pests)

ROOTS?
├── Brown slimy roots, wilting plant → Pythium root rot
├── Brown roots + reddish-brown vascular streaks in stem → Fusarium
├── White cottony cluster on roots → root aphids (see 08-pests, not disease)
├── Galls/swellings → root knot nematodes or crown gall
└── Brown roots, sour smell → Pythium or anaerobic conditions

WHOLE PLANT WILT (SUDDEN)?
├── Substrate wet → Pythium (acute)
├── Lower leaves yellow, vascular streaks → Fusarium
└── Brown crown + soft stem at soil → Damping off (Pythium/Rhizoctonia)

REDUCED VIGOR / "DUDDING" / NO OBVIOUS CAUSE?
├── Multiple plants, stunted, brittle stems → HLVd (PCR test)
├── Single plant only → check genetics + environment
└── All plants underperforming → environmental or schedule issue, not disease
```

---

## Common Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| Powdery Mildew | Trichome accumulation in late flower | PM spreads as colonies; trichomes are uniform/oily |
| PM | Silica spots from foliar silica | Silica: dry, isolated; PM: spreading colonies |
| Botrytis bud rot | Caterpillar damage alone | Caterpillar = frass externally; Botrytis = brown fuzzy mycelium internally; often co-occur |
| Fusarium wilt | Underwatering | Underwater recovers in hours; wilt persists; cut stem for vascular streaks |
| Pythium root rot | Overwatering symptoms | Lift pot; Pythium = brown slimy + sour smell; overwater = no smell, roots intact |
| HLVd | Calcium deficiency / broad mite | HLVd = multi-plant, duck-foot leaves, no mites visible (microscope); PCR test confirms |
| HLVd | Genetic phenotype | If multiple plants from same mother all underperform → suspect HLVd; if only one → genetics |
| Bacterial leaf spot | Septoria | Bacterial = angular limited by veins; Septoria = round with concentric rings |
| Heat bleach | Light burn / PM | Heat = uniform top; light = symmetric top; PM = patchy and spreading |
| Botrytis | Aspergillus | Botrytis = gray-brown; Aspergillus = khaki-yellow + serious health concern |
| "Dud plant" | Genetics OR HLVd | Test before assuming genetics — HLVd is now the more likely cause in commercial |

---

## Verification Questions Before Treating

1. RH and temp at canopy NOW and over last 7 days
2. Stage and week-in-stage
3. Pathogen confirmed visually / by lab test / not yet
4. Recent foliar spray (timing matters for biofungicide compatibility)
5. Pest pressure currently? (Pest damage opens disease entry)
6. Source of clones / seeds (HLVd contamination chain)
7. PCR testing done on mothers in last 90 days
8. Any plants showing symptoms vs whole canopy
9. Sanitation protocol between cycles documented
10. Genetic susceptibility known? (some strains PM-prone, some HLVd-resistant)

If 4+ unknown → don't treat yet. Get the data. Wrong-pathogen-class sprays make resistance worse and may damage the plant.

---

## Sources

- **Tier 1** — Punja, Z. (Simon Fraser University) — definitive cannabis pathology research; Botrytis epidemiology (*Canadian Journal of Botany* 2023, *Canadian Journal of Plant Pathology* 2025); Pythium and Fusarium epidemiology (CJPP 2018, 2020, 2021); biological control trials (CJPP 2023)
- **Tier 1** — Adkar-Purushothama, C.R. et al. (Université de Sherbrooke) — HLVd molecular biology, viroid detection, transmission research
- **Tier 1** — Bektaş, A. et al. (2019) — *Frontiers in Microbiology* — HLVd in cannabis foundational survey
- **Tier 1** — APS *Plant Disease* journal — first reports of *Golovinomyces ambrosiae* on cannabis (Oregon 2020, Quebec 2022, multiple US states); first reports of *Pythium aphanidermatum* on cannabis (Arizona 2021, Florida 2025)
- **Tier 1** — Mieslerová et al. (2024) *Journal of Phytopathology* — co-occurrence of two PM species on cannabis confirmed
- **Tier 1** — Rodriguez-Morrison cannabis flower-stage research with disease-pressure relevance
- **Tier 1** — *Canadian Journal of Plant Pathology* — bud rot pathogen complex, Pythium species diversity in cannabis
- **Tier 1** — Cranshaw, W. (Colorado State Extension) — caterpillar–Botrytis interaction
- **Tier 1** — USU Extension, OSU Extension, NC State Extension — Fusarium wilt, Botrytis, PM management for hemp
- **Tier 1** — Pacific Northwest Pest Management Handbook — disease-by-disease cannabis/hemp protocols
- **Tier 2** — Medicinal Genomics — HLVd PCR detection technology, sterilizer-resistance research
- **Tier 2** — TumiGenomics, MyFloraDNA, Phylos Bioscience, Front Range Biosciences, Norgen Biotek — HLVd PCR testing services and methodology
- **Tier 2** — Marrone Bio (Pro Farm Group) — Regalia / Stargus / Cease cannabis trial data
- **Tier 2** — BioWorks — Cease, RootShield product technical
- **Tier 2** — Certis Biologicals — Actinovate, Prestop technical
- **Tier 2** — Hydroguard / Veg+Bloom — *Bacillus amyloliquefaciens* D747 technical
- **Tier 3** — Cervantes, J. *The Cannabis Encyclopedia* — disease chapter
- **Tier 3** — Rosenthal, E. *Marijuana Garden Saver* — disease field manual
- **Tier 3** — DeBacco University disease lectures
- **Tier 3** — Mr. Canucks Grow IPM walkthroughs

---

## Cross-References

- Pest damage opens entry for pathogens (caterpillar + Botrytis, mite stress + root rot) → `08-pests.md`
- Abiotic look-alikes — heat, light, cold, water stress before treating as disease → `07-deficiencies.md`
- RH/airflow setpoints — the master disease prevention lever → `02-environment.md`
- Root-zone disease risk per medium → `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md`
- HLVd clonal contamination chain (genetics file context) → `01-genetics-strains.md`
- Drying and curing molds (Aspergillus, Penicillium during dry/cure) → `14-drying.md`, `15-curing.md`
- Macro photos and PCR testing recommendations → `references/workflows/diagnose-from-photo.md`
- Full intake protocol for disease-suspect cases → `references/workflows/troubleshoot-grow.md`
- Master diagnostic tree branching to deficiency / pest / disease → `21-troubleshooting-tree.md`
