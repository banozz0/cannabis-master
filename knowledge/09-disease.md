# 09 — Disease

Diseases are the third leg of the plant-health triangle (with `07-deficiencies.md` and `08-pests.md`). They overlap heavily with pests — caterpillar entry seeds *Botrytis* infections; mite-stressed plants are more susceptible to root rot; thrips vector viruses. And they overlap with the environment file — RH and airflow are the master disease-prevention levers, more powerful than any spray. Cross-reference with `08-pests.md` (pest damage opens entry for pathogens — bud rot frequently follows caterpillar feeding), `02-environment.md` (the disease triangle's environmental corner is where most prevention happens), `04-medium-soil.md` / `04-medium-coco.md` / `04-medium-hydro.md` / `04-medium-living-soil.md` (each medium has different root-zone disease risk), `01-genetics-strains.md` (HLVd specifically — clonal genetics carry it forward indefinitely), `workflows/diagnose-from-photo.md` (require macro photos for fungal ID; PCR test recommendation for viroids).

## How to Use This File

1. **Rule out abiotic FIRST** — heat, light bleach, cold stress, water stress. Most "disease" calls are environmental.
2. **Identify pathogen class** before treating — fungi, oomycetes, bacteria, viruses, viroids each need different responses.
3. **Confirm with appropriate diagnostic** — visual + magnification for fungi, lab test for some bacteria, PCR for viroids and viruses. Don't guess on viroids — they have no symptoms early.
4. **Don't shotgun fungicides at viral problems** — wrong category; only sanitation + culling work for viruses/viroids.
5. **Treat the root cause** — environmental conditions usually. A spray that "fixes" PM in a 70% RH room is just suppressing while the conditions reload.
6. **Avoid foliar sprays once flowers are forming** unless the product label explicitly allows it and the crop-loss risk is higher than residue/mold risk. Prefer environment, sanitation, removal, and biological prevention.

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

**Weakening any corner reduces disease pressure.** Do not promise elimination; disease risk is probabilistic.

In cannabis, the most achievable corner to manage is environment — lower late-flower RH reduces Botrytis risk, PM is favored by humid/stagnant canopies, and Pythium is favored by warm, wet, low-oxygen root zones. Genotype changes take a season to swap. Eliminating pathogen presence is hard once established. Environment is where most preventive work pays off.

## Critical Concept — Pathogen Classification

Parallel to mobile/immobile in `07` and above-soil/in-soil in `08`. Pathogen class dictates treatment paradigm.

| Class | Examples | Treatment paradigm |
|---|---|---|
| **Fungi (true — Ascomycota, Basidiomycota)** | Botrytis, Powdery Mildew, Fusarium, Septoria, Aspergillus | Biofungicides, contact fungicides, environmental control |
| **Oomycetes (water molds — Stramenopiles, NOT fungi)** | Pythium, Phytophthora, downy mildew | Different chemistry — most fungicides miss them; root-zone hygiene + DO + Bacillus biocontrol |
| **Bacteria** | Pseudomonas, Xanthomonas, Erwinia | Copper-based, sanitation, environmental — rare in cannabis |
| **Viruses** | LCV, BCTV, TSWV, CMV, occasional tobamovirus reports | NO spray cure — prevention, vector control, testing when available, and culling confirmed infected plants |
| **Viroids** | HLVd | NO spray cure — test, isolate, cull infected plants, prevent tool transmission, and use specialist meristem/tissue-culture cleanup only for valuable genetics |

**Why oomycetes deserve their own row:** they look like fungi but are biologically different, so many common foliar fungicides miss them. For public home-grow guidance, prioritize root-zone hygiene, oxygen, temperature control, clean water, and preventive biologicals instead of restricted chemistry.

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
| Late flower | 40–50% when cultivar/environment allows | 68–75°F | Reduce RH while avoiding plant stress and condensation |
| Last 2 weeks | 40–50% | 65–72°F | Keep night temps from condensing on buds |

**Hard environmental rules for disease prevention:**
- **Leaf wetness for hours creates a disease window.** Avoid foliar spraying near lights-off; only spray when the canopy can dry quickly and the product label supports use.
- **Air movement at canopy = disease prevention.** Aim for gentle movement through the canopy without blasting buds or causing wind burn.
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
- **Cultural** (the lowest-risk defense once flowering):
  - RH 40–50% mid- to late-flower (Tier 1 — Punja recommended)
  - Gentle airflow through bud zones without direct wind burn
  - Remove infected buds with clean tools, bag/seal, and discard; do not compost or consume moldy material
  - Strategic defoliation week 3 of flower for canopy penetration
  - Genetics: some genotypes far more susceptible than others — drop the worst-hit cultivars
- **Biological / Biofungicide**:
  - *Bacillus subtilis* QST713 (Cease, Serenade) — preventive foliar in early flower
  - *Bacillus amyloliquefaciens* (Stargus) — also Botrytis suppression
  - *Gliocladium catenulatum* (Prestop) — Botrytis-targeted antagonist
  - *Reynoutria sachalinensis* extract products — induced systemic resistance; use only when label-compatible
- **Botanical / Mineral**: potassium bicarbonate products — surface contact only, veg/early-stage preferred, label-compatible only
- **No-go**: myclobutanil and similar systemic fungicides are not appropriate for consumable cannabis; do not recommend them

**Stage-safe options:**
- Veg: full ladder
- Early flower: biocontrols + environmental
- Mid-flower: environmental + spot-removal of any infected tissue
- Late flower / last 2 weeks: hand-removal/removal of affected material, accept losses, harvest only clean material if safe

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
- **Biofungicide**: *Reynoutria sachalinensis* extract products can help as preventive/early intervention when label-compatible; do not treat them as a rescue cure for dense infected flower
- **Mineral**: 
  - Potassium bicarbonate (Milstop) — contact, surface kill, veg + early flower
  - Sulfur products — veg/empty-room only, label-compatible, never within 14 days of oils, and not beginner-default
  - Citric-acid products — use labeled products/rates only; homemade concentration errors can burn plants
- **Botanical**: essential-oil products may suppress light PM in veg but can burn plants and leave residues; label-compatible only
- **Avoid**: systemic fungicides such as myclobutanil; not appropriate for consumable cannabis

**Stage-safe options:**
- Veg: full ladder including sulfur
- Early flower: biofungicides only; no sulfur if oils used recently
- Mid-flower+: environment, removal of affected leaves, and label-compatible biologicals only if they will not contact buds
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
  - Clean nonporous containers and tools with a label-compatible disinfectant; discard porous items that cannot be cleaned
  - Pathogen-free seed in pathogen-free media for new starts
- **Biological**:
  - *Trichoderma harzianum* — root-zone antagonist, preventive at transplant
  - *Streptomyces lydicus* (Actinovate) — soil drench preventive
  - *Bacillus amyloliquefaciens* (Hydroguard, Stargus) — Tier 1 — Punja 2023 trials show 30–56% disease severity reduction in cannabis Fusarium/Pythium
  - *Gliocladium virens* — competitive exclusion in soil
- **Botanical / Mineral**: use cautiously; avoid home biofumigation or oil drenches around roots unless following a horticultural label/protocol
- **Avoid**: systemic fungicides such as propiconazole or thiophanate-methyl for consumable cannabis

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
- Biological: use labeled *Trichoderma* or *Bacillus* products in propagation water/media when compatible
- Don't replant in contaminated media — full reset

### Bud-Stage Side Issues — Aspergillus, Penicillium, Pin Rot (Quick reference)

| Issue | ID | Treatment shortcut |
|---|---|---|
| **Aspergillus** | Khaki-yellow fuzzy mold; potential mycotoxin/allergen risk | Cull and discard; do not consume or attempt to salvage moldy material |
| **Penicillium** | Blue-green fuzzy mold during dry/cure | Discard affected material; improve drying/curing environment |
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
  - ***Bacillus amyloliquefaciens* products** — preventive biologicals for clean systems; follow label/rate and do not treat as a cure for collapsed roots
  - *Trichoderma harzianum* — root colonizer, competitive exclusion
  - *Streptomyces lydicus* (Actinovate) — soil/coco drench
  - *Glomus / Mycorrhizae* — root-tip protection
- **Biofungicide**: Regalia ISR
- **Avoid**: mefenoxam/Subdue/Ridomil-style chemistry for consumable cannabis unless a qualified local professional confirms legality and label compatibility
- **Emergency reset only**: oxidizers/peroxide products can kill biology and injure roots; use label-compatible products, reset the reservoir, and rebuild beneficials only after the root cause is fixed

**Critical note:** DWC/RDWC needs a root-disease prevention plan: cool solution, high dissolved oxygen, clean reservoir/lines, no organic debris, and compatible biologicals or sterile-res management. Do not rely on one additive to compensate for poor conditions.

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
- Mineral: copper products only if label-compatible, veg-only, and used sparingly; residue and phytotoxicity are concerns
- Biological: *Bacillus subtilis* shows some efficacy

### Crown Gall (Agrobacterium tumefaciens)

Rare cannabis report. Tumor-like galls on stems near soil. Cull plant; don't replant in same soil for 2 years.

---

## VIRAL & VIROID DISEASES — Clean-Stock Safety Section

### Hop Latent Viroid (HLVd) — "Dudding Disease"

HLVd is one of the most important clean-stock risks for clone-based cannabis. Keep guidance practical: test, quarantine, avoid tool transmission, and do not claim visual certainty.

**Pathogen:**
- A 256-nucleotide circular RNA — no protein coat (Tier 1 — Adkar-Purushothama et al., Université de Sherbrooke; multiple PMC publications 2023–2024)
- Originally identified in hops; now a significant pathogen in clone-based cannabis cultivation
- Mother plants and incoming clones can carry it asymptomatically

**Symptoms (when expressed — many infections stay latent):**
- Stunting and reduced internode length
- "Duck-foot" leaf deformity (leaflets fused or deformed)
- Brittle, hollow stems
- Reduced trichome production, dull/dusty bud appearance
- Reported reductions in cannabinoid/terpene expression in symptomatic infected plants; exact loss varies by cultivar, infection status, and environment
- Yield and vigor can be reduced, sometimes substantially
- Plants often look "tired" or "underperforming" without obvious cause
- Symptoms often only appear under stress (transplant, training, light flip)

**Asymptomatic carriers are the problem.** A mother plant can test positive while looking acceptable and can pass HLVd to cuttings before symptoms are obvious.

**Transmission routes (Tier 1):**
- **Clonal (primary)** — every cutting from an infected mother is infected
- **Mechanical (cutting tools, hands)** — viroids stable on surfaces; cross-contamination during pruning, cloning, training
- **Root-to-root in shared hydroponics** — confirmed in DWC / fertigation systems
- **Pollen/seed risk** — transmission has been reported; risk depends on infected parent tissue and should be treated conservatively until tested-clean
- **NOT vector-borne** (no insect transmission confirmed)

**Detection:**
- **qPCR (TaqMan RT-PCR)** is the gold standard — sensitive to 5 picograms total RNA
- Test cost and turnaround vary by lab and region
- Sample type: leaf tissue, ~2–4 cm² per plant
- Turnaround varies by lab
- Use a reputable plant diagnostic lab or validated assay
- Visual diagnosis is unreliable — test, don't guess

**Treatment — there isn't one. But there are protocols:**
1. **Cull infected plants and substrate.** Not "treat" — remove.
2. **Prevent tool transmission.** Use fresh disposable blades per plant when practical, or a validated disinfectant protocol for tools/surfaces. Sanitizers only address surface contamination; they do not cure infected plant tissue.
3. **Specialist meristem/tissue-culture cleanup** can sometimes recover valuable genetics, but it is not a home rescue recipe:
   - Requires trained sterile technique and very small meristem/explant work
   - Some published protocols combine meristem culture with cold treatment; success varies
   - Timeline can be months to over a year and requires repeated testing
   - Re-test multiple times; a single negative result is not enough for high-value stock
   - Not all genetics survive or clean successfully
4. **Replace infected mother stock with tested-clean stock** when feasible. For most home growers, replacement is safer than trying to clean infected genetics.

**Prevention protocol for clean facility:**
- For mother plants, test periodically if clones are repeatedly taken or unexplained dudding appears
- Quarantine incoming clones 14–21 days and test high-risk genetics before introducing to the main grow
- Seeds are generally lower-risk than clones, but test if the source is high-risk or symptoms appear
- One-way workflow: clean room → propagation → veg → flower (no reverse handling)
- Prefer fresh blades per plant when taking cuttings; otherwise use a validated disinfectant protocol and contact time
- New gloves between plants when cloning / training mom plants
- Quarantine clone gifts or new genetics before introducing them to the main grow

**Why HLVd deserves caution:**
- Can spread before symptoms are obvious
- Visual diagnosis is unreliable
- No spray cure exists
- Detection requires testing
- Best response is quarantine, testing, isolation, and replacement of infected stock

(Sources throughout — Tier 1: Adkar-Purushothama et al.; Bektaş, A. et al. 2019 *Frontiers in Microbiology*; Punja viroid surveys; Phylos Bioscience discovery announcement 2019. Tier 2: Medicinal Genomics technical documentation; TumiGenomics protocol whitepapers.)

### Other Viral / Viroid Diseases

| Disease | Pathogen | Vector / spread | Symptoms | Treatment |
|---|---|---|---|---|
| **Lettuce Chlorosis Virus (LCV)** | LCV crinivirus | Whiteflies (*Bemisia tabaci*) | Interveinal chlorosis on lower leaves | None — vector control + cull |
| **Beet Curly Top Virus (BCTV)** | BCTV geminivirus | Beet leafhopper | Stunting, leaf curling, rosette growth | None — outdoor screening, cull |
| **Tobamovirus-like reports** | TMV/related tobamoviruses, rarely confirmed in cannabis | Mechanical contamination | Mosaic mottling, leaf deformity | None — sanitation, avoid tobacco handling before plant work |
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
| Drooping with no color change | Watering issue | See `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, or `04-medium-living-soil.md` |

If any of these explanations fit, fix the abiotic cause first. Don't spray fungicide at heat damage.

---

## IPM Treatment Toolkit — Disease-Specific

### Cultural / Environmental (the master tier)

| Tool | Application |
|---|---|
| **RH management** | The #1 lever — see Environmental Setpoints table above |
| **Airflow at canopy** | Gentle movement through every layer; avoid stagnant pockets and direct wind burn |
| **Defoliation** | Week 3 of flower for canopy penetration; bottom-third "lollipop" |
| **Sanitation between cycles** | Clean debris first, then use a label-compatible disinfectant on nonporous surfaces with required contact time |
| **Quarantine + testing** | Strongly recommended for clone-based grows; especially important for mother plants and unexplained dudding |
| **UV-C** | Specialist empty-room/surface tool only; eye/skin hazard and not a substitute for cleaning |
| **One-way workflow** | Clean → propagation → veg → flower; no reverse handling |
| **Tool hygiene between plants** | Fresh blades or validated disinfectant/contact time; wipe organic sap off first |
| **Genetics culling** | Drop susceptible cultivars; Botrytis-prone genetics not worth keeping |

### Biological / Biofungicides (the cornerstone of cannabis disease IPM)

| Product | Active ingredient | Target | Notes |
|---|---|---|---|
| ***Bacillus amyloliquefaciens* products** | Beneficial bacteria | Pythium/Fusarium suppression | Preventive support; label/rate-dependent, not a cure for failed root conditions |
| **Cease / Serenade** | *Bacillus subtilis* QST713 | Botrytis, PM, foliar pathogens | Weekly preventive in veg / early flower |
| **RootShield / Tenet** | *Trichoderma harzianum / virens* | Pythium, Fusarium, Rhizoctonia | At transplant; long-term root colonizer |
| **Actinovate** | *Streptomyces lydicus* | Pythium, Fusarium, Rhizoctonia | Soil drench preventive |
| **Prestop** | *Gliocladium catenulatum* | Botrytis, Pythium | Foliar + soil application |
| ***Reynoutria sachalinensis* extract products** | Plant extract/ISR | PM/Botrytis suppression | Preventive/early support; label-compatible only |
| **Mycorrhizae** | *Glomus, Rhizophagus* spp. | Root protection (general) | Inoculate at transplant; not a cure but a defense |

### Botanical / Mineral

| Product | Target | Stage | Notes |
|---|---|---|---|
| **Sulfur products** | PM | Veg/empty-room only; never near oils | Follow label/PPE; burners are not beginner-default |
| **Potassium bicarbonate (Milstop)** | PM contact | Veg + early flower | Surface kill; no residual |
| **Copper products** | Bacterial spots, some oomycete leaf diseases | Veg only if label-compatible | Phytotoxicity/residue risk; use sparingly |
| **Essential-oil products** | Mild foliar/root-zone suppression | Veg only if label-compatible | Burn/residue risk; not a cure |
| **Citric-acid products** | PM mild contact | Veg | Use labeled products/rates; avoid homemade acid burns |
| **Oxidizer/peroxide products** | Emergency sanitation/reset | Reset only | Can injure roots and kill biology; label-compatible only |

### Restricted / residual chemistry — do not recommend

Do not recommend systemic, restricted, unlabeled, or residual fungicides for consumable cannabis. If environmental correction, sanitation, removal, and label-compatible biologicals fail, the safer public guidance is to cull affected material, restart clean, or consult a qualified local extension/professional resource. Pesticide labels are legal safety documents and local rules vary.

---

## Sterilization Protocols Between Cycles

### Standard sanitation/disinfection (reduces many pathogens)

| Sanitizer | Active ingredient | Contact time | Notes |
|---|---|---|---|
| **Diluted household bleach** | Sodium hypochlorite | Per label / extension protocol | Corrodes metal; never mix with acids/ammonia; clean organic debris first |
| **ZeroTol 2.0** | Hydrogen dioxide + peroxyacetic acid | Per label | EPA-registered; cannabis-cleared; surfaces + reservoirs |
| **OxiDate 2.0** | Same chemistry as ZeroTol | Per label | Same use case |
| **SaniDate 5.0** | Hydrogen peroxide | Per label | Organic-certified |
| **Virkon S** | Potassium peroxymonosulfate | Per label | Broad-spectrum surface disinfectant |
| **Green-Shield II / Physan 20** | Quaternary ammonium | Per label | Surface only, less for biology |
| **Hypochlorous acid (HOCl)** | Stabilized | Per label | Gentle surface option; verify use case |

### HLVd-specific sanitation note

No surface sanitizer fixes an infected plant. Published guidance varies by product, concentration, contact time, and whether sap/organic debris was removed first, so do not promise that a casual wipe prevents HLVd spread.

For HLVd specifically:
- Sanitizers prevent **between-plant** transmission of viroid present on tools/surfaces
- Sanitizers do NOT remove viroid from infected plant tissue
- Specialist meristem/tissue-culture cleanup may recover some valuable genetics, but replacement is safer for most home growers
- One-way workflow + PCR testing + isolation are the practical protocol
- Replace infected mother stock with tested-clean stock — don't try to "clean" infected moms

### Between-cycle full reset protocol

1. Remove all plants and substrate from room
2. Vacuum dust, debris, leaves
3. Scrub nonporous surfaces, then disinfect with a label-compatible product and contact time
4. Clean fan blades (often missed) — pathogen reservoir
5. Clean HVAC filters and ducting if accessible
6. Replace fabric pots or other porous items that cannot be reliably cleaned
7. Clean hydroponic reservoir, lines, and drippers using a label-compatible sanitation protocol; flush thoroughly before plants return
8. Optional specialist empty-room treatments only if label-compatible and safe; do not run sulfur/UV-C around people, pets, or plants
9. If using UV-C, treat it as a serious eye/skin hazard and follow device instructions; it does not replace physical cleaning
10. Ventilate fully before reintroducing plants
11. Optional final surface wipe with a label-compatible disinfectant
12. Restock with clean, quarantined genetics

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
├── Khaki-yellow fuzzy mold → possible Aspergillus/other mold (discard affected material; do not consume)
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
| Botrytis | Aspergillus/other molds | Botrytis = gray-brown; Aspergillus often khaki-yellow; discard moldy material rather than salvaging |
| "Dud plant" | Genetics, environment, pests, or HLVd | Test before assuming; HLVd is a possibility in clone-based lines |

---

## Verification Questions Before Treating

1. RH and temp at canopy NOW and over last 7 days
2. Stage and week-in-stage
3. Pathogen confirmed visually / by lab test / not yet
4. Recent foliar spray (timing matters for biofungicide compatibility)
5. Pest pressure currently? (Pest damage opens disease entry)
6. Source of clones / seeds (HLVd contamination chain)
7. Any HLVd/virus testing done on mother plants or incoming clones?
8. Any plants showing symptoms vs whole canopy
9. Sanitation protocol between cycles documented
10. Genetic susceptibility known? (some cultivars are more PM/Botrytis-prone; do not assume disease resistance without evidence)

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
- Macro photos and PCR testing recommendations → `workflows/diagnose-from-photo.md`
- Full intake protocol for disease-suspect cases → `workflows/troubleshoot-grow.md`
- Master diagnostic tree branching to deficiency / pest / disease → `21-troubleshooting-tree.md`
