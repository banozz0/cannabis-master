# 11 — Propagation

Propagation is the genetic supply chain — every grow starts here. Get it wrong and you've wasted weeks before veg even begins; get it right and you've banked the genetic uniformity that drives commercial consistency. This file covers seed germination, cuttings/clones, mother plant management, an introduction to tissue culture (full protocol in `19-tissue-culture.md`), transplanting, and hardening off. Cross-reference with `01-genetics-strains.md` (which seeds/clones to start with — pheno-hunting strategy), `09-disease.md` (HLVd transmission via cuts and tools — propagation is the #1 entry point for the #1 commercial threat), `19-tissue-culture.md` (the advanced version — meristem cleaning, micropropagation, MS/DKW media), `10-training.md` (monstercropping — clones from flowering mothers), `02-environment.md` (cloning has unique RH/temp/light setpoints), `04-medium-coco.md` and `04-medium-living-soil.md` (transplant medium choices), `references/workflows/new-grow-setup.md` (where propagation fits in setup planning).

## How to Use This File

1. **Pick seed-or-clone first** — different protocols, different timelines, different risk profiles.
2. **Match propagation method to skill level + scale** — paper towel for 1–4 seeds; cubes for many; aero for commercial; tissue culture for clean stock.
3. **Set the propagation environment correctly** — cloning RH/temp setpoints differ from veg; substrate temp matters more than air temp.
4. **PCR-test mothers and incoming clones** — every 4–6 weeks for HLVd, before every clone harvest. This is non-negotiable in commercial.
5. **Sterile cutting tools** — every cut is a HLVd transmission point; soak tools in 10% bleach 10 minutes between plants.
6. **Harden off before any environmental transition** — dome → veg, indoor → outdoor, cube → coco; gradual transitions only.
7. **Transplant on root-bound signals**, not on a schedule — visible roots at container perimeter is the trigger.

## Critical Concept — Seed vs Clone Decision

The first fork in propagation. Different paths, different trade-offs.

| Aspect | Seed | Clone |
|---|---|---|
| Genetic certainty | Variable — pheno-hunt to find winners | Identical to mother (assuming no drift) |
| Vigor | Stronger taproot; faster early establishment | Weaker root system; faster total cycle (skip 2–4 weeks of seedling) |
| Time to harvest | +2–4 weeks vs clone of same strain | Faster (no seedling stage) |
| Disease risk | Low — most pathogens minor; HLVd via seed possible but rare | High — clones inherit mother's HLVd, mites, viruses |
| Cost | $5–20+ per seed | $5–20+ per clone (or free from your own moms) |
| Best for | Pheno-hunting, breeding, beginners learning, fresh genetics | Production runs, commercial consistency, known pheno |
| HLVd risk | Low | Very high — the #1 transmission route in licensed cannabis |

**Practical rule:** seed-only setups don't accumulate HLVd. Clone-only setups need rigorous testing infrastructure. Most commercial setups run mother rooms with quarterly-or-tighter PCR testing because clone-based production is faster and more uniform — but the testing burden is real.

## Critical Concept — The Cloning Environment Paradox

Cloning needs HIGH RH (70–90%) — cuttings have no roots, transpire from leaves only, dry out fast. But high RH everywhere else equals disease pressure (see `09-disease.md`). The solution is a dedicated propagation chamber separate from veg/flower rooms.

**Specific setpoints (Tier 2 — multiple commercial cloning system specifications):**

| Parameter | Setpoint | Notes |
|---|---|---|
| Air temp | 72–78°F (22–25°C) | 80°F upper bound for vigorous strains |
| **Substrate temp** | **76–80°F (24–27°C)** | More important than air temp; heat mat usually required |
| RH under dome | 80–90% days 1–3, then taper | Vents closed first 2 days, open day 3+ |
| PPFD | 100–200 µmol·m⁻²·s⁻¹ | Very low — high light stresses unrooted cuttings |
| Photoperiod | 18–24 hours | 24/0 shaves a day off rooting; 18/6 fine |
| Airflow | Gentle, present | Zero airflow → fungal issues; strong airflow → desiccation |
| Misting | Day 1 only, unless wilting | Over-misting → mold |

**Key practical points:**
- Day 1: dome closed, full RH
- Day 2–3: dome closed, monitor for excess condensation (wipe off if pooling)
- Day 3+: vent dome 5–10 minutes daily, increasing through day 7–10
- Day 10–14: dome off, hardening to ambient RH
- Substrate temp drives root initiation — without a heat mat, propagation in a 65°F basement fails consistently
- High air temp without high substrate temp = cuttings transpire faster than roots can develop = dead clones

## Critical Concept — Genetic Drift & Mother Plant Longevity

Clones taken from clones taken from clones over years can show genetic drift — vigor loss, pheno expression changes, increased disease susceptibility. The documented mechanism in cannabis is **HLVd accumulation** — silent infection that compounds across clone generations even when individual generations look normal (Tier 1 — Adkar-Purushothama / Sherbrooke; Punja research; PMC 2023 *Transmission, Spread, Longevity and Management of Hop Latent Viroid* peer-reviewed).

**Mother plant management timeline:**
- 0–6 months: standard care, light HLVd risk if sourced clean
- **6 months: PCR test the mother (HLVd specifically)**
- 6–12 months: continue testing every 4–6 weeks before clone harvest
- 12–18 months: consider rotation; vigor / pheno expression may drift even if HLVd-negative
- 18+ months: refresh from seed OR meristem-cleaned tissue culture stock

**Best-practice HLVd PCR testing schedule (Tier 1 + Tier 2 — Medicinal Genomics, TumiGenomics, Cannabis Business Times consensus):**
- **Every 4–6 weeks on every mother plant**
- **Before every clone harvest**
- **Every incoming clone** at 14-day quarantine before introduction to flower room
- Root tissue has highest HLVd levels and is most reliable for detection

This is more aggressive than older schedules suggested — the field moved fast 2023–2026 as the asymptomatic-spread mechanism became clear.

---

## SEED PROPAGATION — Per-Item Deep Profiles

### Seed Quality & Viability Assessment

**Visual quality cues:**
- **Good seeds:** dark mottled tan/brown, hard shell, "tiger stripes" pattern, glossy surface
- **Marginal seeds:** uniformly tan, less hard, lower stripes
- **Poor seeds:** pale green, white, or grey; soft when squeezed; no patterns
- **Crushed/cracked:** discard

**Viability over time:**
- Fresh (year 0–1): 95%+ germination
- Year 2–3: 80–90%
- Year 5: ~50%
- Year 10+: highly variable, often <30%
- Storage in cool dark dry conditions extends viability 5–10 years

**Storage best practice:**
- Airtight container in fridge (not freezer — ice damages embryos)
- Silica gel desiccant
- Keep dark, no UV exposure
- Original packaging until use

**Float test caveat:** seeds that sink in water are sometimes called "viable" — this is unreliable. Some healthy seeds float; some duds sink. Visual + germination test are better indicators.

### Paper Towel Method (the hobby standard)

**What it is:** Germinate seeds between two damp paper towels in a covered container, dark warm spot. The classic method for 1–10 seeds.

**How to execute:**
1. Two plates (one as lid) or a sealable plastic container
2. 2–3 layers paper towel on bottom, dampened with pH-corrected water (6.0 ideal)
3. Space seeds 1 inch apart on towel
4. Cover with another 2–3 layers damp paper towel
5. Cover and place in 70–78°F dark area (top of fridge, on a heat mat, in a closed cabinet)
6. Check every 12 hours; mist if drying
7. **Taproot at 5–10 mm = transplant time** (don't wait for green shoot — too late)

**Timeline:** 24–72 hours for taproot emergence; 90%+ success rate at consistent moisture and temp.

**Conditions:**
- Temp: 70–78°F (21–25°C) optimum; 70–85°F acceptable
- Moisture: damp not soaking — squeeze towel, no drips but feels wet
- Darkness: full dark
- RH inside container: 70–90%

**Common failures:**
- Paper towel dried out → re-wet, may save partial
- Too cold → germination stalls; warm up
- Old seeds → may not germinate at all
- Mold on towel → too wet; damp not soaking
- Taproot grew through towel → transplant immediately, may damage taproot

### Direct Sow

**What it is:** Plant seed directly into final / intermediate substrate. Less shock than paper-towel-transplant; relies on substrate moisture management.

**How to execute:**
1. Pre-moisten substrate (coco, soil, or starter cube) with pH 6.0 water
2. Make a 1/4 inch hole
3. Drop seed in (taproot up or down — doesn't matter; gravity sorts it)
4. Cover lightly, mist surface
5. Cover with humidity dome or plastic wrap
6. 70–78°F, low light or dark for 24–72 hours
7. Remove cover when seedling emerges

**Pros:** no transplant shock; fewer steps; less handling.
**Cons:** can't see what's happening; non-germinators waste pot space; harder to control moisture.

### Glass of Water (24h Soak)

**What it is:** Pre-germination soak to soften shell. Combine with paper towel for harder/older seeds.

**How to execute:**
1. Glass of room-temp pH 6.0 water (RO or dechlorinated)
2. Drop seeds in
3. Soak 12–24 hours (longer than 24h risks drowning)
4. Transfer to paper towel method or starter cube

**When to use:** old seeds (3+ years), particularly hard shells, low germination history. Skip for fresh seeds — unnecessary stress.

### Starter Cubes (Rapid Rooter, Root Riot, Jiffy, Rockwool)

**What it is:** Pre-charged plug germination. Commercial standard — consistent results, easy to scale, easy to transplant.

**How to execute (Rapid Rooter / Root Riot — peat-based):**
1. Pre-soak cubes in pH 6.0 water 30 minutes
2. Squeeze excess water out (damp not dripping)
3. Place seed in pre-formed hole, cover with pinch of substrate
4. Place cubes in dome tray, cover with humidity dome
5. 70–78°F, low light or dark
6. Cubes hold moisture 3–5 days; check daily and re-mist if drying

**For rockwool:**
- Pre-soak in **pH 4.0 water** for 30+ minutes — rockwool is naturally alkaline (pH ~7.5–8.0), pre-soaking with acidic water buffers it down to 5.5–6.1 at use
- Rinse with pH 5.8 water
- Insert seed, fold pre-existing slot closed
- Same dome / temp / light protocol

**Timeline:** taproot in 24–72 hours; first true leaves at 5–7 days; ready for transplant when roots visible at cube edges (10–14 days).

### Seed-to-Seedling Transition

**Day 1–3 post-emergence:**
- Cotyledons (round first leaves) emerge
- No feeding — seed has stored energy
- Light at low PPFD (100–200 µmol)
- 70–78°F, RH 65–70%

**Day 4–10:**
- First true serrated leaves
- Light pH-corrected water with very dilute feed (0.4 EC max)
- Reduce dome RH gradually if using

**Day 10–21:**
- Establishing seedling, multiple node sets
- Increase feed strength to 0.6–0.8 EC
- Transplant at 4th–5th true leaf set OR when roots visible at cube edges

---

## CLONING — Per-Item Deep Profiles

### Mother Plant Selection

**Selection criteria (in order):**
1. **HLVd PCR-tested negative** — non-negotiable for commercial; recommended for hobbyists with mother rooms
2. **Vigorous growth** — strong stem, good lateral branching, normal leaf morphology
3. **Disease-free** — no PM, no Botrytis history, no russet mites
4. **Sexed** (female) — confirmed by previous flower or by genetic test
5. **True-to-pheno** — matches expected phenotype expression
6. **Productive** — historical yield data if available

**Sourcing:**
- From your own grow: select best phenotype from a seed run, take cuttings before flip
- Commercial dispensary clones: HLVd risk; quarantine + test before introducing
- Tissue-culture-cleaned stock: highest cost, lowest disease risk
- Friend/peer: HLVd risk; quarantine + test mandatory

### Cutting Selection & Prep

**Which branch to cut:**
- 4–6 inch length
- Mid-canopy branches (not lowest, not topmost)
- 2–3 nodes total
- Healthy lush leaves (not yellowing or damaged)
- Some "woodiness" at base (fully tender stems root slower)

**Prep steps:**
1. **Sterile sharp blade** — sterilize between every plant cut (10% bleach 10 minutes OR fresh blade per plant — HLVd!)
2. **45° diagonal cut** — increases surface area for water/hormone uptake
3. **Strip lower leaves** — remove all leaves on the lower 1–2 inches that will be in substrate
4. **Trim large fan leaves** — cut largest fan leaves to ~50% size to reduce transpiration load
5. **Optional: scrape lower 5 mm of stem** OR slice up the middle of base (exposes more cambium for root initiation)
6. **Get into water immediately** — even 30 seconds of air can air-embolize the stem

### Rooting Hormones

**Clonex Rooting Gel** (the standard, Tier 2 — Hortilux/HDI):
- **3000 PPM IBA** (indole-3-butyric acid) — the gold-standard concentration
- Water-based gel formula
- Includes broad-spectrum antifungal (protects cut tissue during rooting)
- Method: dip cutting in gel 5–10 seconds, insert into rooting medium

**Olivia's Cloning Solution** — lower IBA, gentler, popular for sensitive strains.

**Hormodin / Rootone** (powder) — lower-cost, IBA in talc base. Older formula, still works.

**DIY options:**
- **Willow water** — soak willow twigs 24h; contains natural IBA (low concentration)
- **Honey** — folk method, mild antimicrobial; weak hormone effect

**Practical:** Clonex is the standard for a reason — 3000 PPM IBA + antifungal + ease of use. Don't reinvent unless cost-driven.

### Rockwool / Rapid Rooter Cubes (the standard hobby method)

**Setup:**
1. Pre-soak cubes (rockwool: pH 4.0; Rapid Rooter: pH 6.0) — 30 min minimum
2. Squeeze damp not dripping
3. Tray + dome ready
4. Heat mat under tray, set 76–80°F substrate temp

**Cloning step:**
1. Cut cutting per prep protocol above
2. Dip in Clonex gel
3. Insert into pre-cut slot/hole in cube, deep enough that lower 1–2 inches of stem are buried
4. Place in tray, cover with humidity dome
5. Vents closed days 1–2; open partially day 3+
6. Mist cuttings day 1 (under dome), no further misting unless wilting

**Timeline:**
- Day 1–3: callus formation (white tissue at cut)
- Day 5–10: first roots visible at cube edges
- Day 10–14: root mass developed; roots out of cube bottom
- Day 14–21: ready for transplant

**Success rate:** 80–95% with good technique.

### Aero Cloner (EzClone, TurboKlone, Cloner Pro)

**What it is:** Cuttings held in neoprene collars suspended over a reservoir; intermittent mist sprays the bare stem ends. No substrate; "aero" or "fogger" cloning.

**Setup:**
1. Reservoir with pH 5.8 water + Clonex Mist (or Hormex, or just plain pH'd water)
2. Water temp 75–80°F (heat the reservoir if needed)
3. Mist cycle: 1 minute on / 4–5 minutes off
4. Air pump for reservoir oxygenation
5. Low-PPFD light (100–200 µmol), 18/6 photoperiod
6. **No humidity dome** — aero cloners self-humidify via mist

**Cloning step:**
1. Cut, prep, optional Clonex dip
2. Insert into neoprene collar
3. Place in cloner top
4. Run mist cycle continuously

**Timeline:**
- Day 3–5: callus + first root nubs
- Day 5–9: root mass developed
- Day 7–14: thick fuzzy root system, ready for transplant
- Pull at root mass ≥1 inch

**Success rate:** 90–99% with proper technique (Tier 2 — TurboKlone, EzClone manufacturer specs and user-reported data).

**Pros:**
- Fast rooting (often 7 days vs 10–14 in cubes)
- High success rate
- Easy to inspect roots without disturbing
- Scales well (24–96 sites in commercial models)

**Cons:**
- Equipment cost ($150–500)
- Reservoir maintenance (cleaning, water changes)
- Pump failure = dead cuttings
- Power outage risk
- Slightly more "rooting shock" at transplant (bare-root → substrate)

### Water Cloning

**What it is:** Cup of water + cutting; change water every 2–3 days; transfer to substrate when roots visible.

**How to execute:**
1. Glass jar (opaque preferred — light promotes algae)
2. pH 5.8 water + 1 drop H₂O₂ (slows microbial growth)
3. Cut cutting per prep
4. Insert into water 1–2 inches deep
5. Change water every 2–3 days
6. Once roots are 1+ inch, transfer to substrate (rockwool, coco, soil)

**Timeline:** 14–21 days typical (slow vs other methods).

**Pros:** zero equipment cost; you can watch roots develop.
**Cons:** slow; risk of algae/bacterial growth; transfer-shock from water-roots to substrate-roots.

**Best fit:** beginners with no equipment; rescue cloning when other methods unavailable.

### Soil/Coco Direct Cloning

**What it is:** Stick the cutting straight into damp coco or soil under a dome. Old-school, low success rate but workable.

**How to execute:**
1. Damp pre-buffered coco or seedling-strength soil mix
2. Cut, prep, Clonex dip
3. Insert into pre-made hole in substrate
4. Place under dome
5. Heat mat, dome, low light — same as cubes
6. Don't disturb — checking roots damages them

**Timeline:** 14–21 days; harder to verify roots without disturbing.

**Success rate:** 60–80% (lower than cubes or aero).

**Best fit:** living soil setups where uniformity isn't critical; outdoor / greenhouse simple setups.

### Hardening Off (Cube → Veg Substrate)

**Day 14 (roots visible):**
- Begin opening dome 5–10 minutes per day
- Increase light slightly (200–300 µmol)
- Reduce RH gradually (90% → 75%)

**Day 17–18:**
- Dome off completely
- Transplant cube into 4-inch pot or solo cup with veg-strength substrate
- Bury cube to top edge

**Day 18–21:**
- Plants transitioning to standard veg
- Light feed (0.6–0.8 EC)
- RH 60–70%, temp 75–82°F
- Light increasing toward standard veg PPFD (300–500 µmol)

---

## MOTHER PLANT MANAGEMENT

### Setup

- Dedicated mother room or chamber, separate from veg/flower
- 18+ hour photoperiod (sometimes 24/0 — no flowering trigger)
- Lower light intensity than production (300–500 µmol — moms don't need to yield, just stay healthy)
- Standard veg environment (RH 55–65%, temp 75–80°F)
- Larger containers (5–10 gallon for established moms)
- Topping for clone harvest — keep the plant short enough to access cuttings

### Feeding

- Lighter than production veg feed (~0.8–1.2 EC)
- Balanced N-P-K, no aggressive bloom amendments
- Cal-Mg supplementation per medium
- pH 5.8–6.2 (coco/hydro) or 6.3–6.8 (soil)
- Consistent — moms don't like big changes

### Training for Clone Production

- Top mother plants regularly to keep manageable size
- Encourage many side branches (more clone-harvest sites)
- LST to prevent vertical sprawl
- Defoliate periodically to maintain airflow

### HLVd Testing

**Schedule (Tier 1 + Tier 2 consensus):**
- Initial test on acquisition or first clone
- Every 4–6 weeks ongoing
- Before every clone harvest
- After any suspected exposure event (visitor, new equipment, sister plant positive)

**Sample type:** root tissue has highest HLVd levels and is most reliable for detection (Tier 1 — multiple PMC publications). Leaf tissue acceptable for routine screening, root for confirmation.

**Cost:** $30–80 per sample at major labs (TumiGenomics, Medicinal Genomics, MyFloraDNA, Phylos, Front Range Bio).

### Retirement Triggers

Retire (replace from seed or meristem-cleaned stock) when:
- HLVd PCR positive
- Visible pheno drift from established baseline
- Repeated disease issues despite environmental management
- Vigor drop without clear cause
- Mother age > 18–24 months without exceptional reason to keep

---

## TISSUE CULTURE INTRO (cross-ref to `19-tissue-culture.md`)

**What it is:** In vitro propagation in sterile agar/gel media containing nutrients, hormones, and sugars. Plants grow from tiny meristem tissue under controlled lab conditions.

**Why use it:**
- **HLVd cleaning** — meristem-tip culture (<0.5 mm tip) can produce clean stock from infected mothers (Tier 1 — Adkar-Purushothama, multiple peer-reviewed protocols)
- **Mass propagation** — one mother can yield thousands of identical plantlets
- **Long-term genetic library** — slow-growth maintenance preserves genetics in lab indefinitely
- **Commercial scale** — Aurora, Canopy, large producers all run TC libraries

**Basic process (full protocol in `19-tissue-culture.md`):**
1. **Explant excision** — tiny meristem tip (≤0.5 mm for cleaning, 2–5 mm for routine multiplication) cut from healthy mother
2. **Surface sterilization** — bleach + ethanol washes to kill surface microbes
3. **Establishment** — explant placed on **MS media (Murashige & Skoog basal salts) or DKW media (Driver & Kuniyuki Walnut)** with plant growth regulators (TDZ, IBA, GA₃) (Tier 1 — Lata, University of Mississippi National Center for Natural Product Research; multiple protocols 2010–2025)
4. **Multiplication** — explant divides; subculture every 4–8 weeks
5. **Rooting phase** — transfer to rooting media (lower hormones)
6. **Ex vitro acclimation** — gradual transition out of agar to soil/coco; high humidity initially

**Recent research note:** while MS media has been the standard for cannabis tissue culture, recent research suggests **DKW media may be preferable** due to higher Ca, S, Cu and different vitamin profile better suited to cannabis specifically (Tier 1 — multiple 2024–2025 publications).

**See `19-tissue-culture.md` for full protocol, media recipes, sterilization technique, and common failure modes.**

---

## TRANSPLANTING

### Container Progression

Standard photoperiod indoor grow:
- **Solo cup (16 oz)** — initial seedling, weeks 0–2
- **4-inch pot or 1-gal** — first transplant, weeks 2–4
- **3–5 gal** — veg → pre-flip
- **5–10 gal** — final flower container

**Skip steps if rapid grow planned** — solo cup → 5-gal direct works for fast grows; container progression is for grower control of root development and resource efficiency.

**Up-pot rule of thumb:** new container 3–5× volume of previous. Bigger jumps risk overwatering (excess substrate stays wet).

### Root-Bound Signals

Don't transplant on a schedule — transplant on these signals:
- **Visible white roots at perimeter** of root ball (lift and inspect)
- **Roots out of drainage holes**
- **Substrate dries within 24 hours** of watering (high root density consuming fast)
- **Slowed growth** despite adequate feed and light
- **Yellowing or wilting** of mature leaves (root system maxed out)

**Plant signals:** transplant when seedling has 4th–5th true-leaf set; that timing usually aligns with first root-bound signals.

### Transplant Technique

1. **Pre-water 24h before** — moist root ball holds together; dry root ball crumbles
2. **Pre-fill new container** with substrate up to where the root ball will sit
3. **Gently invert original container** — squeeze sides to release; never pull from stem
4. **Inspect roots** — healthy white; yellow/brown indicates issues
5. **Set root ball in new container**, ensuring original soil line matches new soil line
6. **Backfill** with fresh substrate around sides
7. **Water in** with mycorrhizae + light feed (0.6–0.8 EC)
8. **24–48 hour low-light recovery** before normal light schedule
9. **Wait for new growth signals** (3–5 days) before training or stress

### Transplant Shock Minimization

- **Mild shock** (slight droop hours): resolves 1–2 days
- **Moderate shock** (drooping + yellowing): 3–7 days recovery
- **Severe shock** (stalled growth, mass yellowing): 2+ weeks; may not fully recover

**Reduce shock by:**
- Matching medium type (coco → coco, soil → soil — don't switch substrates at transplant)
- Pre-watering 24h before
- Mycorrhizae inoculation at transplant
- Kelp / fish hydrolysate / B vitamins (Superthrive, Rhizotonic) at first watering
- Stable environment for 5 days post-transplant (no training, no aggressive feeding)
- Same pH and EC as previous routine

---

## HARDENING OFF (Indoor → Outdoor)

When moving indoor-grown plants outdoors, indoor-soft tissue can't tolerate direct sun, UV, or wind without acclimation.

**7–10 day hardening protocol:**
- Day 1–2: 1–2 hours direct outdoor sun, ideally morning (low-intensity sun)
- Day 3–4: 2–4 hours, expand into midday
- Day 5–6: 4–6 hours, near full day
- Day 7–10: full sun all day, return indoors only at night
- Day 11+: full outdoor

**Light hardening notes:**
- Cloudy days don't count — need direct sun
- UV is the major shock factor (indoor LEDs typically lack significant UV)
- Plants may show "sun stress" first 2–3 days (slight stippling, leaf curl) — normal

**Temp hardening:**
- Indoor 75–82°F constant → outdoor diurnal swings (50–95°F range possible)
- Gradual exposure over the same 7–10 days helps
- If overnight lows <55°F, bring plants in until consistently warm

**Wind/movement hardening:**
- Run an oscillating fan indoors for 1–2 weeks pre-move (strengthens stems)
- Outdoor breeze stimulates further stem-strengthening within a few days
- Stake any tall plants until they've adapted

**IPM hardening:**
- Outdoor exposure introduces pests/disease
- Pre-treat with neem soil drench or beneficial microbes before move
- Inspect daily during transition for new pest/disease signs
- See `08-pests.md` and `09-disease.md`

---

## PHENO HUNTING (Brief Overview)

(Cross-ref `01-genetics-strains.md` for genetic theory; this is the propagation-stage practice.)

**Process:**
1. Pop a regular or feminized seed pack of the cultivar (5–20+ seeds)
2. Grow each through full cycle in identical conditions (same medium, same feed, same environment)
3. Tag each plant uniquely; track through flower
4. Evaluate at harvest + cure on:
   - Quantitative: yield (g), cannabinoid % (lab test if available), terpene profile, time to harvest
   - Qualitative: smell, taste, structure, vigor, pest/disease resistance, mold resistance
5. Pick the 1–3 best phenotypes
6. Take clones from the best phenotypes pre-flip OR re-veg post-harvest (monstercrop — see `10-training.md`)
7. Establish those clones as mothers for production
8. Discard others

**Timeline:** one full grow cycle (12–16 weeks photoperiod) per pheno-hunt round.

**Practical:** beginners often pick winners on yield alone. Experienced hunters weight quality (terpene/cannabinoid expression, smoke quality) higher because terpenes have broader market value than raw weight.

---

## Common Failures & Troubleshooting

| Issue | Likely cause | Fix |
|---|---|---|
| Seeds not popping at all | Old seeds OR temp too low OR towel dried | Check seed age; warm up; verify moisture |
| Seeds germinate then die | Watering too hard at sprout OR substrate too cold | Gentle mist only; heat mat |
| Clones wilt under dome | RH too low OR substrate too cold OR fan blowing on dome | Verify RH 80–90%; substrate temp 76–80°F; redirect airflow |
| Clones rooted but stalling | Cube transplant timing OR light too bright OR hardening rushed | Slow down hardening; reduce light to 200 µmol initially |
| Cube dried out | Missed water OR dome lifted too long | Re-mist; replace dome; check daily |
| Mold on clones | Dome too wet + zero airflow | Vent dome briefly daily; gentle airflow |
| Aero cloner failed (no roots) | Water too cold OR pump failure OR water contamination | Check pump; warm water 75–80°F; clean reservoir + restart |
| Mother plant pheno drift | Genetic drift OR HLVd OR feed/environment shift | PCR test first; check feed schedule; consider replacing mother |
| Transplant shock severe | Medium mismatch OR root damage OR stress at wrong time | Match medium; gentle technique; recovery in stable conditions |
| Hardening-off plants fried | Too much sun too fast OR no UV adaptation | Restart at 1h direct sun; gradual ramp |

---

## Quick Reference — Propagation Method Decision Tree

```
START → Goal?
├── New genetics / pheno hunt → Seed
├── Production from known pheno → Clone (your moms or commercial)
├── Bulk production with proven winner → Tissue culture (see 19-tissue-culture.md)
└── Rescue genetics from HLVd → Tissue culture meristem (see 09-disease.md + 19)

SEED method?
├── Beginner / 1–4 seeds → Paper towel
├── Many seeds at once / commercial → Starter cubes (Rapid Rooter or rockwool)
├── Hard old seeds → 24h water soak then paper towel
└── Outdoor direct → Direct sow after frost

CLONE rooting method?
├── Beginner / few clones → Rockwool or Rapid Rooter cubes + dome
├── Many clones / commercial → Aero cloner (EzClone, TurboKlone)
├── No equipment / budget → Water cloning
└── Established living soil → Direct in coco or soil

MOTHER MANAGEMENT?
├── Set up dedicated room → 18/6, lighter feed, 4–6 week PCR cadence
├── Already have moms → start PCR testing immediately
└── Refresh stock → Tissue culture meristem cleaning if genetics worth saving

TRANSPLANT?
├── Roots at perimeter → transplant
├── 4th–5th true leaf set → first transplant
├── Slowed growth + drying fast → up-pot
└── Stem long, leaves yellow → may already be root-bound + stressed
```

---

## Verification Questions Before Starting

1. Seed or clone path?
2. Source HLVd-tested? (mandatory for clones in commercial)
3. Cloning environment ready (dome, substrate temp 76–80°F, RH 80–90%, low PPFD)?
4. Mother plant healthy, vigorous, sexed, PCR-tested in last 4–6 weeks?
5. Rooting hormone available (Clonex 3000 PPM IBA standard)?
6. Substrate prepared (cubes pre-soaked at right pH)?
7. Recovery space available (post-rooting hardening zone with veg-strength environment)?
8. Final destination prepared (veg light, container, feed plan)?
9. Sterile cutting tools? (HLVd transmission via every cut)
10. Backup plan if propagation fails (extra seeds, extra clones, time buffer)?

If 4+ unknown → don't start yet. Get the data and the plan.

---

## Sources

- **Tier 1** — Caplan, D. & Zheng, Y. (University of Guelph) — propagation and rooting research; cannabis-specific cultivation studies
- **Tier 1** — Lata, H. (University of Mississippi, National Center for Natural Product Research) — cannabis micropropagation foundational research; MS media + plant growth regulators protocols
- **Tier 1** — Adkar-Purushothama, C.R. et al. (Université de Sherbrooke) — HLVd transmission via clones, viroid persistence research
- **Tier 1** — Punja, Z. (Simon Fraser University) — cannabis pathology in propagation context, mother plant disease management
- **Tier 1** — *Transmission, Spread, Longevity and Management of Hop Latent Viroid* — PMC peer-reviewed comprehensive HLVd review
- **Tier 1** — Holmes et al. — cannabis seed viability and storage research
- **Tier 1** — Pacifico et al., Codesido et al. — cannabis tissue culture optimization (DKW vs MS media findings)
- **Tier 2** — Hortilux / Hydrodynamics International — Clonex Rooting Gel technical specifications (3000 PPM IBA)
- **Tier 2** — Rapid Rooter / General Hydroponics — pre-charged starter cube protocols
- **Tier 2** — Root Riot — peat-based cube specs
- **Tier 2** — EzClone, TurboKlone, Cloner Pro — aeroponic cloning system specs and root timelines
- **Tier 2** — TumiGenomics, Medicinal Genomics, MyFloraDNA, Phylos Bioscience, Front Range Biosciences — HLVd PCR testing services and frequency recommendations
- **Tier 2** — Cannabis Business Times — *Hop Latent Viroid: A Guide to Sampling, Testing and Lab Selection*
- **Tier 3** — Jorge Cervantes (propagation chapter, *Cannabis Encyclopedia*)
- **Tier 3** — Ed Rosenthal (*Marijuana Grower's Handbook*)
- **Tier 3** — DJ Short — pheno-hunting methodology and breeding philosophy
- **Tier 3** — Soma Seeds — mother plant management
- **Tier 3** — DeBacco University propagation lectures
- **Tier 3** — Mr. Canucks Grow cloning walkthroughs
- **Tier 3** — Subcool — mother plant selection and pheno-hunting

---

## Cross-References

- Strain choice and pheno-hunting context → `01-genetics-strains.md`
- HLVd as the #1 propagation-stage threat — testing, transmission, mitigation → `09-disease.md`
- Advanced version with full tissue culture protocols → `19-tissue-culture.md`
- Monstercropping (clones from flowering mothers) → `10-training.md`
- Cloning-specific environmental setpoints → `02-environment.md`
- Transplant medium choices and pre-charging → `04-medium-coco.md`, `04-medium-living-soil.md`
- pH adjustment for rockwool pre-soak → `05-water-quality.md`
- Light feeding for seedlings + mothers → `06-nutrients-synthetic.md`, `06-nutrients-organic.md`
- Where propagation fits in setup workflow → `references/workflows/new-grow-setup.md`
- Onboarding when user has no plants yet → `references/workflows/onboarding.md`
- Master diagnostic tree branching to "is this a propagation issue?" → `21-troubleshooting-tree.md`
