# 05 — Water Quality

Water is the foundation under every nutrient decision. EC math, pH targets, and Cal-Mg strategy all sit on top of what comes out of the source. Two grows on identical schedules but different source water will get different results — and most "mystery deficiencies" trace back here. Cross-reference with `04-medium-*.md` (each medium has different pH targets and alkalinity tolerance), `06-nutrients-synthetic.md` and `06-nutrients-organic.md` (feed recipes assume a baseline starting EC), and `07-deficiencies.md` (the pH lockout map is downstream of source-water alkalinity).

## How to Use This File

1. **Get a source water test FIRST** — before buying nutes, before choosing a medium pH target, before anything. You can't dial what you can't measure.
2. **Classify your source** — RO, tap, well, rain, distilled, or blend. Each has different default pitfalls.
3. **Identify the limiting factor** — usually alkalinity (high tap), or absence of Ca/Mg (RO), or sodium load (water-softener tap).
4. **Set Cal-Mg strategy** — driven by source + medium. RO + coco = always supplement. Hard tap + soil = often skip.
5. **Set pH adjustment strategy** — acid choice depends on alkalinity (high alkalinity needs more acid, picks the type), nutrient line, and stage.
6. **Verify by runoff/res monitoring** — input EC and pH are not the whole story. What's leaving the pot or sitting in the res tells you what the plant actually saw.

## Critical Concept — EC vs PPM and the Two Scales

EC (electrical conductivity) measures dissolved salts directly. PPM is EC translated through a multiplier — and there are two competing multipliers, which is the source of half the confusion in this hobby.

| Scale | Multiplier | Used by | Region |
|---|---|---|---|
| **500 (NaCl)** | EC (mS/cm) × 500 = ppm | Hanna, Milwaukee, HM Digital, most US TDS pens | Mostly US |
| **700 (KCl / 442)** | EC (mS/cm) × 700 = ppm | Bluelab, Truncheon | EU + AU + commercial hydro |
| **640** | EC × 640 = ppm | Some European meters | Rare |

**Same water reads three different numbers on three meters.** A nutrient solution at 1.5 mS/cm reads 750 ppm on a 500-scale meter and 1,050 ppm on a 700-scale meter. Neither is "wrong." But mixing them is.

**Practical rule:** EC is the only conversion-free measurement. If you talk to other growers in EC, you are unambiguous. If you talk in PPM, you must specify which scale or you're guaranteed to miscommunicate (Tier 2 — Bluelab tech docs).

**For this skill's recommendations:** EC values are canonical. PPM is only quoted when matching a specific brand schedule that uses it.

### Starting EC — what your raw water contributes

Every dissolved mineral in your tap raises EC before you've added a drop of nute.

| Source | Typical starting EC (mS/cm) | Typical starting PPM (500 scale) |
|---|---|---|
| RO (4-stage, working membrane) | 0.0–0.05 | 0–25 |
| Distilled | 0.0 | 0 |
| Rainwater (collected) | 0.02–0.10 | 10–50 |
| Soft tap (Pacific Northwest, Northeast US, Northern UK) | 0.1–0.3 | 50–150 |
| Medium tap (most US, EU, AU) | 0.3–0.6 | 150–300 |
| Hard tap (US Southwest, Spain, Italy, Malta, Israel) | 0.6–1.2 | 300–600 |
| Well (variable) | 0.2–2.0+ | 100–1000+ |

If your starting EC is 0.5 and your target feed is 1.6, you have only 1.1 EC of headroom for nutes — meaning you're running ~30% lighter than the bottle dose suggests. This is a common cause of underfeeding on tap water.

## Critical Concept — pH vs Alkalinity vs Hardness

These three terms get used interchangeably by beginners and even some product copy. They mean different things, and confusing them is the #1 cause of "my pH won't stay down."

| Term | What it measures | Unit | Why it matters |
|---|---|---|---|
| **pH** | Acidity at this moment | 0–14 (log scale) | Determines what nutrients roots can absorb |
| **Alkalinity** | Buffering capacity (carbonate / bicarbonate) | ppm CaCO3 or mEq/L | Determines how hard your pH FIGHTS BACK against adjustment |
| **Hardness** | Total Ca + Mg in water | ppm CaCO3 or grains/gallon | Determines if you need Cal-Mg supplementation |

**The trap:** "Hard water" loosely refers to BOTH high hardness AND high alkalinity, because they often correlate (limestone aquifers add both Ca and bicarbonate). But softened water (ion-exchange) removes hardness while leaving alkalinity unchanged AND adding sodium — the worst possible combination for cannabis.

**Conversion:** 1 mEq/L alkalinity = 50 ppm CaCO3. Cannabis Business Times and academic sources often report alkalinity in mEq/L; municipal water reports use ppm CaCO3. You'll see both — convert by ×50 or ÷50 (Tier 2 — Cannabis Business Times "Alkalinity Control for Container-Grown Cannabis").

## Critical Concept — Alkalinity Thresholds

Alkalinity is the silent #1 problem in tap-water grows. High alkalinity neutralizes the acid you add to lower pH, then quietly raises substrate pH over weeks until micros lock out.

| Alkalinity (ppm CaCO3) | Status | What to do |
|---|---|---|
| <40 | Ideal — almost no buffering, pH adjusts easily | Use as-is, monitor |
| 40–100 | Acceptable — moderate buffering | Acid-inject normally, expect small pH drift up over time |
| 100–150 | Marginal — substrate pH will creep up | Use acid pH-down aggressively, watch runoff pH weekly, consider RO blend |
| 150–250 | Problematic — pH won't hold, micros lock out | RO blend (50/50) or full RO + Cal-Mg |
| >250 | Severe — switch to RO | Tap unusable for cannabis without dilution |

**Container-size adjustment** (Tier 2 — Cannabis Business Times):
- Small plants (4" pots, propagation): tolerate ≤1.3 mEq/L (65 ppm CaCO3)
- Mid containers (1–3 gal): tolerate ≤2.0 mEq/L (100 ppm CaCO3)
- Large containers (5+ gal, established): tolerate ≤2.6 mEq/L (130 ppm CaCO3)

Smaller containers have less substrate volume to absorb the alkalinity drift, so they crash to high pH faster.

**How alkalinity tests:** drop tests (API freshwater alkalinity kit), strips (LaMotte / Hach), or send to a lab. Municipal water reports list it (sometimes as "total alkalinity" or "as CaCO3"). Free at most US municipalities — request the annual Consumer Confidence Report.

---

## SOURCE WATER PROFILES

### Reverse Osmosis (RO)

**Profile:**
- EC: 0.0–0.05 mS/cm (0–25 ppm)
- pH: 5.5–7.0 (unstable, no buffer)
- Alkalinity: 0–10 ppm CaCO3
- Hardness: ~0
- Ca, Mg, Fe: zero
- Removes: 90–98% of dissolved solids, all chlorine/chloramine, most pesticides, heavy metals

**Pros:**
- Predictable baseline — every grow starts the same
- No alkalinity fighting your pH-down
- No sodium, no chloramine, no surprise contaminants
- Required for sensitive setups (Athena Pro Stack, fully-defined commercial recipes)

**Cons:**
- Wastes water — typical 4-stage RO rejects 3–4 gallons per gallon produced (newer tankless permeate-pump systems get 1:1)
- Zero Ca/Mg means **mandatory** Cal-Mg supplementation at every feed
- pH crashes easily — no buffer means a tiny acid spill swings 2 full points
- Equipment cost ($150–500 for a quality 4–5 stage system) + filter replacement ($30–80/year)

**Pre-treatment needed:**
- Sediment pre-filter (replace every 6–12 months)
- Carbon pre-filter (replace every 6–12 months) — protects RO membrane from chlorine
- RO membrane (replace every 2–3 years, or when output EC drifts above 50 ppm)

**Cal-Mg strategy:**
- Mandatory. Target 60–80 ppm Ca and 20–30 ppm Mg in finished feed water (Tier 3 — community consensus, cross-confirmed by Athena and Canna technical bulletins)
- Maintain 4.5:1 to 6:1 Ca:Mg ratio (Tier 2 — Athena Pro)
- Typical product: 1–2 ml/L of any major Cal-Mg adds ~50–100 ppm Ca and ~15–30 ppm Mg
- DIY: calcium nitrate + Epsom salts in 4:1 ratio by weight if using synthetic; gypsum + Epsom for organic

**pH adjustment difficulty:** Easy. Tiny acid doses produce big pH movement. Easy to overshoot — add acid drop by drop.

**Common pitfalls:**
- Skipping Cal-Mg "to save money" → guaranteed deficiency in week 2–3 of veg
- Not flushing the membrane after install → high initial EC (run 5+ gallons before using)
- Cold-weather RO output drops 30–50% (membrane efficiency is temp-dependent)
- Letting the membrane sit dry between long breaks → premature failure

### Tap (Municipal)

**Profile (varies wildly by region):**
- EC: 0.1–1.2 mS/cm (50–600 ppm)
- pH: 6.5–8.5 (often alkaline due to corrosion control)
- Alkalinity: 30–300 ppm CaCO3
- Hardness: 30–400 ppm CaCO3
- Ca: 20–150 ppm typical
- Mg: 5–50 ppm typical
- Sodium: 5–80 ppm (varies — softened water is much higher)
- Chlorine OR chloramine: 0.5–4 ppm
- Possible: fluoride (0.5–1.2 ppm), trace metals, pesticides depending on watershed

**Pros:**
- Free or near-free
- Already has some Ca/Mg (often enough for soil grows)
- Convenient — no equipment

**Cons:**
- Unpredictable — composition shifts seasonally
- Alkalinity often the limiting factor
- Chloramine doesn't off-gas
- Sodium load can creep over time in coco/hydro re-fills
- Municipal sources sometimes switch chlorine ↔ chloramine without notice

**Pre-treatment needed:**
- Get the Consumer Confidence Report (US) or equivalent annual water-quality report
- For chlorine: aerate 24 hours OR run a basic carbon filter
- For chloramine: catalytic carbon filter, ascorbic acid (40 mg per gallon), or sodium ascorbate
- For high alkalinity: acid-inject (phosphoric or nitric) to neutralize OR blend with RO

**Cal-Mg strategy:**
- Test first. Hard tap (>120 ppm CaCO3 hardness) often has 60+ ppm Ca and 20+ ppm Mg already — Cal-Mg may be unnecessary in soil
- In coco/hydro, even hard tap usually benefits from a small Cal-Mg dose (0.5 ml/L) due to coco's Ca-binding nature
- Soft tap (<60 ppm CaCO3 hardness) treat like RO — full Cal-Mg

**pH adjustment difficulty:** Hard. High alkalinity fights every drop of acid. Plan on more pH-down than RO and expect substrate pH to drift up over weeks.

**Common pitfalls:**
- Trusting "drinking water safe" as "plant safe" — they're different standards
- Adding Cal-Mg to already-hard tap → calcium toxicity / lockout of K and Mg
- Using ion-exchange softened water → guaranteed sodium toxicity over 6–8 weeks
- Ignoring chloramine because "it's just chlorine" → sterilizes living soil, slows beneficials
- Not retesting seasonally — spring runoff, summer drought, fall reservoir turnover all change tap chemistry

### Well Water

**Profile (highly variable):**
- EC: 0.2–2.0+ mS/cm (often the highest of any source)
- pH: 6.0–8.5
- Alkalinity: 50–500+ ppm CaCO3
- Hardness: very variable — could be very hard (limestone aquifer) or soft (granite)
- Iron (Fe): often elevated (red staining = >0.3 ppm) — clogs drip lines, oxidizes
- Manganese (Mn): often elevated alongside Fe
- Sulfur (H2S): rotten-egg smell — toxic to roots
- Sodium: variable, can be high in coastal or arid wells
- Microbiological: untreated well water can carry pathogens

**Pros:**
- Free (after well install)
- Often mineral-rich — can support some grow setups directly

**Cons:**
- Most variable source — full lab test mandatory before any grow
- Iron and manganese problems are common and corrode equipment
- Chemistry changes with seasonal water table

**Pre-treatment needed:**
- **Lab test annually minimum.** Standard agricultural water panel from a state extension lab or commercial lab ($30–80) — look for Ca, Mg, Na, Cl, S, Fe, Mn, alkalinity, hardness, pH, EC, total nitrogen
- Iron/Mn high → oxidation filter (greensand) or aeration tank + sediment filter
- H2S → aeration + activated carbon
- Hardness/alkalinity high → RO or blend
- Bacterial contamination → UV sterilizer

**Cal-Mg strategy:** Test-driven. Most well water has plenty of Ca, often too much. Mg may or may not be sufficient.

**pH adjustment difficulty:** Variable. High-alkalinity wells fight pH-down hard. Low-alkalinity granite-aquifer wells behave like soft tap.

**Common pitfalls:**
- Skipping the lab test → flying blind
- Adding Cal-Mg without testing → toxicity
- Not maintaining filtration → iron oxidation in feed lines
- Using well water on living soil with high alkalinity → biology can't compensate fast enough

### Rainwater

**Profile:**
- EC: 0.02–0.10 mS/cm (10–50 ppm) — depends on air pollution
- pH: 5.0–6.5 (slightly acidic, atmospheric CO2)
- Alkalinity: 0–20 ppm CaCO3
- Hardness: ~0
- Trace minerals: minor amounts of N (from lightning + air), S, dust-borne minerals
- Possible contaminants: roof material leaching (asphalt shingles → PAH; metal roofs → zinc/copper), bird/insect debris, atmospheric pollutants near industry

**Pros:**
- Free, naturally soft, low alkalinity
- Slightly acidic pH is friendly to most setups
- Closer to "what plants evolved with" than any other source
- Excellent for living soil

**Cons:**
- Storage required, capacity limits scale
- Quality depends on collection surface and atmosphere
- Algae/biological growth in stored rain
- Legal restrictions in some US states (Colorado, Utah have/had limits)

**Pre-treatment needed:**
- First-flush diverter (discard first 5–10 gal of any storm to flush roof debris)
- Sediment filter
- Optional UV or chlorination for stored water
- Avoid asphalt-shingle or treated-wood collection surfaces

**Cal-Mg strategy:** Treat as RO — full Cal-Mg supplementation needed.

**pH adjustment difficulty:** Easy, behaves like RO with slightly more buffering.

**Common pitfalls:**
- Algae blooms in opaque tanks left in light → use opaque/dark storage
- Trusting roof runoff after pesticide spraying or wildfire → contamination risk
- Long storage without circulation → anaerobic bacteria, off-smells

### Distilled

**Profile:**
- EC: 0.0
- pH: 5.5–7.0 (unstable)
- All other minerals: 0

**Identical to RO operationally** but produced by boiling and condensing rather than membrane filtration. More energy-intensive, lower throughput, but achieves the same result.

**Use case:** small grows where bottled distilled is convenient, or RO unavailable. Not practical above 1–2 plants due to cost ($1–2/gallon at retail).

**Cal-Mg, pH, and pitfalls:** identical to RO.

### Blended (RO + Tap)

**Profile (50/50 example with medium tap):**
- EC: 0.15–0.30 mS/cm
- Alkalinity: ~50% of tap value (40–80 ppm CaCO3)
- Ca/Mg: ~50% of tap value (often enough for soil, supplement for hydro)

**When to blend:**
- Tap alkalinity is 100–200 ppm CaCO3 — too high for direct use, not bad enough to justify pure RO every feed
- Want some baseline minerals but not the full tap load
- RO equipment can't keep up with grow demand — extend output

**How to set ratio:**
- Test tap alkalinity, calculate dilution to hit target <100 ppm CaCO3 in blend
- Verify blended EC, alkalinity, and pH before mixing nutes
- Common ratios: 50/50, 70/30 (RO/tap), 30/70 (RO/tap)

**Cal-Mg strategy:** Calculate from blended Ca/Mg. Often sits in the "supplement lightly" zone (0.5–1 ml/L Cal-Mg).

---

## CHLORINE & CHLORAMINE

Both are added to municipal water as disinfectants. They behave very differently in your reservoir and your soil.

| Property | Chlorine (Cl2) | Chloramine (NH2Cl) |
|---|---|---|
| Form | Free chlorine gas dissolved | Bonded chlorine + ammonia |
| Typical municipal level | 0.5–2 ppm | 1–4 ppm |
| Off-gases overnight? | Yes — 24h aeration removes most | No — stable for weeks |
| Removed by basic carbon filter? | Yes | Partially, slowly |
| Removed by catalytic carbon? | Yes, fast | Yes, fast |
| Removed by RO membrane? | Yes | Yes |
| Removed by ascorbic acid (Vitamin C)? | Yes | Yes |
| Affects soil microbes? | Yes, but recovers | Yes, persistent |
| Affects DWC reservoirs? | Yes (kills beneficials) | Yes (kills beneficials, harder to remove) |

**How to know which your city uses:** call the utility or check the Consumer Confidence Report. Many US utilities switched from chlorine to chloramine in the 2000s for longer-lasting disinfection — "I let my water sit out overnight" is no longer reliable in many cities.

**Removal methods:**
- **Catalytic carbon filter** — best for ongoing supply, expensive ($100–300 inline unit), works for both. Standard activated carbon is much slower on chloramine (Tier 2 — manufacturer specs from Pentair, Aquasana).
- **Ascorbic acid (Vitamin C)** — 40 mg per gallon (about 10 mg/L) neutralizes both chlorine and chloramine. Sodium ascorbate is preferred over plain ascorbic acid because it doesn't drop pH (Tier 1 — SFPUC standard dechlorination protocol).
- **Aeration only** — works for chlorine in 12–24 hours. Does not work reliably for chloramine.
- **RO** — removes both, but the membrane wears faster on chlorinated water; carbon pre-filter mandatory.

**For living soil specifically:** chlorine/chloramine kills bacterial and fungal allies. Always remove before watering living soil. Even a single chlorinated watering measurably knocks down microbial activity for 3–7 days.

---

## pH ADJUSTMENT — Choosing an Acid

| Acid | Strength | Adds | Stage | Notes |
|---|---|---|---|---|
| **Phosphoric (H3PO4)** | Moderate | P | Bloom-friendly | Most common pH-down. Holds pH stable longer than nitric. Generic GH/GH-style pH-down is dilute phosphoric (Tier 2 — General Hydroponics MSDS) |
| **Nitric (HNO3)** | Strong | N | Veg-friendly | Common in commercial. Lets you reduce N feed accordingly. Aggressive — wear gloves and eye protection (Tier 2 — Athena Pro tech bulletin) |
| **Sulfuric (H2SO4)** | Very strong | S | Either | Cheapest at scale. Dangerous to handle. Some operations use battery acid grade — verify food-safe |
| **Citric** | Weak | Carbon (compostable) | Living soil / organic | Doesn't last — pH rebounds in days. Good for organic where you don't want mineral additions. Won't hold a hydro res |

**Practical recommendations:**
- Hobby grow, soil or coco: phosphoric pH-down (any major brand: GH, Advanced Nutrients, Bluelab) — works year-round
- Veg-only res: nitric — supplements N
- Bloom res: phosphoric — supplements P
- Living soil: don't pH-adjust water at all (biology handles it). If you must, use citric
- Commercial scale: sulfuric or nitric (cost) with proper PPE
- Research / fully-defined recipes: nitric in veg, phosphoric in flower (this is what Athena Pro and Canna assume in their schedules)

**pH-up:**
- **Potassium hydroxide (KOH)** — standard pH-up. Adds K. Works fast, holds well.
- **Potassium silicate** — doubles as silica supplement. Raises pH significantly per ml. Add to water FIRST (before any other input) to avoid precipitation.
- **Calcium carbonate / dolomite lime** — for soil amendment, not for water. Buffers pH long-term.

**Order of operations when mixing nutes:**
1. Plain water in res
2. Silica (if using) — raises pH
3. Cal-Mg
4. Base nutrients (A then B if 2-part, or all parts in order)
5. Additives
6. Adjust pH last

Reversing the order often causes precipitation (calcium phosphate clouds), nutrient lockout, or wasted product.

---

## CAL-MG STRATEGY BY SOURCE

| Source | Cal-Mg need | Typical dose |
|---|---|---|
| RO / distilled / rain | Always | 1–2 ml/L (full mfg dose) |
| Soft tap (<60 ppm CaCO3 hardness) | Usually | 0.5–1 ml/L |
| Medium tap (60–120 ppm) | Sometimes | 0–0.5 ml/L, test-driven |
| Hard tap (>120 ppm) | Rarely | 0 ml/L in soil; 0.25 ml/L in coco/hydro |
| Well | Test first | Variable |

**Target finished-feed levels (Tier 2 — Athena Pro, Canna technical):**
- Ca: 60–150 ppm
- Mg: 25–50 ppm
- Ratio: 4.5:1 to 6:1 (Ca:Mg)

**Why coco needs more than soil:** coco fiber has a high cation exchange capacity (CEC) that binds Ca preferentially, removing it from solution. The plant sees less Ca than the bottle math suggests until the coco is "buffered" (pre-charged). New coco needs extra Cal-Mg for the first 1–2 weeks — see `04-medium-coco.md` for the buffering protocol.

**Why hydro/DWC needs Cal-Mg even with RO:** there's no medium to buffer, so the only Ca/Mg the plant gets is what's in the res. Skipping is a guaranteed deficiency in 7–14 days.

**Product comparison (Tier 2 — manufacturer documentation):**
- Botanicare CaMg+ — 2-1-1, includes nitrogen, one of the older formulas, common
- Athena Cal-Mag — 5-0-0, clean formulation, expensive
- Canna CalMag Agent — 1-0-0, magnesium-leaning ratio
- General Hydroponics CALiMAGic — 1-0-0, well-established
- DIY: Calcium nitrate + Epsom salts at 4:1 weight ratio. Cheapest at scale, not organic.

---

## SOURCE WATER TESTING PROTOCOL

What to measure, in priority order:

**Tier A — measure every grow (essential):**
- EC / starting PPM (cheap pen, $30)
- pH (pen, $50–100, calibrated weekly)
- Alkalinity (drop test or strip, $10–20)
- Chlorine/chloramine (cheap pool test strip, $10)

**Tier B — measure annually or on suspicion (lab test):**
- Ca, Mg (drives Cal-Mg strategy)
- Sodium (drives whether to switch sources)
- Chloride (paired with Na)
- Sulfate
- Iron, manganese (especially for well water)
- Total nitrogen (well water especially)
- Hardness (paired with alkalinity)

**Where to test:**
- US: state agricultural extension lab (cheapest, $30–80) — search "[state] agricultural water test"
- Commercial: Spectrum Analytic, Logan Labs, A&L Laboratories — irrigation suitability panel
- Free starting point: pull your municipality's annual Consumer Confidence Report online

**When to retest:**
- New grow space / new water source: full panel before any grow
- Same source, ongoing: full panel annually
- Seasonal change suspected (taste/smell different, EC drift): retest the simple parameters
- After any equipment change (new RO membrane, new well pump, new filtration): retest

---

## METER CARE — Calibration and Lifespan

**pH meter:**
- Calibrate weekly minimum, more often if used heavily (Tier 2 — Bluelab, Hanna)
- Two-point calibration: pH 4.01 and pH 7.01 buffer solutions (do not mix pen across buffers without rinsing in distilled)
- Store in KCl storage solution — never plain water (pulls ions out of the bulb, ruins the electrode)
- Replace electrode every 1–2 years for hobby use; commercial replaces every 6 months
- Signs of dying electrode: drift, slow response (>30 sec to settle), inconsistent readings between buffers
- Cheap pens ($15–30) drift constantly and lie. A Bluelab/Apera mid-tier pen ($90–150) is the floor for serious use

**EC meter:**
- Calibrate monthly (more stable than pH)
- Use 1413 µS/cm calibration solution
- Temperature compensation matters — readings vary 2% per °C
- Same brands (Bluelab, Apera, Hanna) for reliable hobby use
- Combo pens (pH + EC + temp) save money but have shorter electrode life

**Both meters:**
- Rinse in distilled between samples
- Don't store dry (kills electrodes)
- Replace calibration solutions when seal opened >12 months ago
- If a calibration "won't take" — first suspect the buffer/standard, then the meter

---

## Quick Reference — Decision Tree

```
START → Got a source water test?
  No → Stop. Test EC, pH, alkalinity, chlorine/chloramine before proceeding.
  Yes → Continue.

EC of source water?
  <0.05 → RO/distilled/rain → Cal-Mg mandatory, easy pH adjust
  0.1–0.3 → Soft tap or rain → Cal-Mg likely needed in coco/hydro
  0.3–0.6 → Medium tap → Test alkalinity to decide
  0.6+ → Hard tap or well → Lab test mandatory

Alkalinity of source water?
  <40 ppm CaCO3 → Use as-is
  40–100 → Use, monitor runoff pH weekly
  100–150 → Acid-inject + monitor, or 30/70 RO blend
  150–250 → 50/50 RO blend or full RO
  >250 → Switch to RO entirely

Chlorine vs chloramine?
  Aeration removes chlorine in 24h → fine for non-organic
  Chloramine present → catalytic carbon, ascorbic acid, or RO mandatory if living soil

Sodium >50 ppm?
  Yes → Don't use for cannabis — find alternate source or RO
  No → Continue

Hardness?
  <60 ppm CaCO3 → Cal-Mg needed at full dose
  60–120 → Cal-Mg at half dose, test-adjust
  >120 → Cal-Mg often unneeded in soil, lighter dose in coco/hydro

Stage?
  Veg → Nitric pH-down (adds N) acceptable
  Bloom → Phosphoric pH-down (adds P) preferred
  Living soil → No pH adjustment, biology handles it
```

---

## Common Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| pH-down "not working" | High alkalinity buffering it back | Test alkalinity. >100 ppm CaCO3 means pH-down fights uphill |
| Calcium deficiency on tap water | Sodium-induced Ca lockout (softener water) | Test sodium. >50 ppm suspicious, >100 ppm guaranteed |
| Iron deficiency | Substrate pH crept up due to high source alkalinity | Test runoff pH; if >6.5 in coco/hydro, that's why |
| Mystery EC creep in res | Sodium accumulation from tap top-offs | Test res Na; switch top-off water to RO |
| RO water "killing my plants" | No Cal-Mg added | RO without Cal-Mg = guaranteed deficiency, not water purity issue |
| Tap water "fine for years" suddenly causing problems | Municipality switched chlorine to chloramine | Call utility; aerated water no longer dechlorinates |
| 800 ppm reading on different meter | Different scale (500 vs 700) | Confirm scale; same EC ≠ same PPM number |
| Burnt tips on consistent feed | Source EC contribution + nute EC = total too high | Subtract source EC from target before nute math |
| pH crashing in hydro res | RO base + acidic nutes + no buffer | Add silica (raises pH) or alkalinity buffer; check daily |
| Living soil pH "wrong" | Reading raw water or nute solution, not soil | Living soil pH is set by biology in substrate, not water |

---

## Verification Questions Before Acting

Before recommending source-water changes:

1. What's the source EC and pH straight from the tap/RO/well?
2. What's the alkalinity in ppm CaCO3? (Or "not tested" — and that's the answer to find first.)
3. What's the medium? (Different pH targets per medium drive different acid choices.)
4. What's the runoff pH and EC? (Source matters less than what's leaving the pot.)
5. Has the water source changed recently? (Move, season change, utility switch.)
6. What Cal-Mg product is currently in use, at what dose?
7. Is chloramine confirmed present or just suspected?
8. Has a lab test been done in the last 12 months?

If 4+ of these are unknown → don't recommend a source-water change. Get the data.

---

## Sources

- **Tier 1** — Bugbee, B. (Utah State Crop Physiology Lab) — water quality, pH and nutrient availability research, plant nutrient uptake mechanisms ([digitalcommons.usu.edu](https://digitalcommons.usu.edu/cgi/viewcontent.cgi?article=1001&context=cpl_nutrients))
- **Tier 1** — Caplan, D. & Zheng, Y. (University of Guelph) — substrate water relations and cannabis fertilizer studies
- **Tier 1** — SFPUC dechlorination protocol — ascorbic acid as standard chloramine neutralizer
- **Tier 2** — Cannabis Business Times "Alkalinity Control for Container-Grown Cannabis" — container-size alkalinity tolerance thresholds
- **Tier 2** — Rx Green Technologies water quality monitoring guides
- **Tier 2** — Bluelab technical documentation — EC/PPM scale conversion, calibration protocols
- **Tier 2** — Hanna Instruments calibration documentation
- **Tier 2** — Athena Pro, Canna Research, General Hydroponics technical bulletins — Cal-Mg targets, acid choice
- **Tier 3** — Cervantes, J. *The Cannabis Encyclopedia* — water chapter
- **Tier 3** — Rosenthal, E. *Marijuana Grower's Handbook* — water source selection
- **Tier 3** — DeBacco University (Penn State) horticulture lectures on irrigation water quality
- **Tier 3** — KiS Organics water testing guide — living soil water chemistry

---

## Cross-References

- Medium-specific pH targets and water tolerance → `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md`
- Feed schedules built on top of source-water EC math → `06-nutrients-synthetic.md`, `06-nutrients-organic.md`
- pH lockout map for nutrient deficiencies → `07-deficiencies.md`
- Custom feed schedule generation → `references/workflows/build-feed-schedule.md`
- Setup planning incl. RO equipment selection → `references/workflows/new-grow-setup.md`
- Diagnostic flowchart that branches to "check water first" → `21-troubleshooting-tree.md`
