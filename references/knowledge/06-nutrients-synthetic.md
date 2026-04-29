# 06 — Nutrients (Synthetic / Mineral)

Synthetic nutrients are mineral salts in immediately-available form. They bypass the soil-microbe digestion path that organics require, which makes them faster, more predictable, and the standard for coco, hydro, and synthetic-fed soil. The tradeoff: zero margin for error. The plant gets exactly what's in the bottle, salt buildup is real, and pH must be set every mix. Cross-reference with `05-water-quality.md` (every feed sits on starting EC), `04-medium-soil.md` / `04-medium-coco.md` / `04-medium-hydro.md` (each medium dictates feed strength multiplier), `06-nutrients-organic.md` (don't mix mental models — organic and synthetic philosophies are different), `07-deficiencies.md` (toxicity is the symmetric risk on this side).

## How to Use This File

1. **Pick a line by medium and budget first** — line dictates schedule shape, not the other way around.
2. **Set EC target by stage** — using the master table, adjusted for medium and PPFD.
3. **Build the mix in correct order** — silica → Cal-Mg → calcium-bearing part → phosphate-bearing part → micros → additives → adjust pH last.
4. **Verify with runoff (soil/coco) or res reading (hydro)** — input EC alone tells you only what you put in, not what the plant saw.
5. **Adjust on data, not feeling** — runoff EC drift up means lower input; drift down means raise input.
6. **Don't switch lines mid-grow** unless solving a specific issue — interaction effects ruin the diagnostic signal.

## Critical Concept — The 17 Elements

Cannabis (like all higher plants) requires 17 essential elements. Synthetic lines vary in which they include and at what ratios — the difference between a "complete" line and a "base + supplement" approach is exactly this.

| Group | Element | Role | Symptom file ref |
|---|---|---|---|
| **Macros** | N (nitrogen) | Vegetative growth, chlorophyll | `07-deficiencies.md` |
| | P (phosphorus) | Root, energy transfer, flowering | |
| | K (potassium) | Water regulation, terpenes, density | |
| **Secondary** | Ca (calcium) | Cell walls, root tips | |
| | Mg (magnesium) | Chlorophyll core | |
| | S (sulfur) | Amino acids, terpene precursors | |
| **Micros** | Fe (iron) | Chlorophyll synthesis | |
| | Mn (manganese) | Photosynthesis enzymes | |
| | Zn (zinc) | Auxin synthesis, internode | |
| | B (boron) | Cell wall, reproductive tissue | |
| | Cu (copper) | Lignin, oxidative balance | |
| | Mo (molybdenum) | Nitrogen metabolism | |
| | Cl (chloride) | Photosystem II — usually from water | |
| | Ni (nickel) | Urease enzyme — trace need | |
| **Beneficial** | Si (silicon) | Cell wall strength, pest/heat resistance | |
| **Air/water** | C, H, O | From CO2 and water | |

**Why this matters for line choice:**
- Athena Pro, House & Garden, Canna include all 14 mineral elements as part of base.
- Jack's 321 includes all 14 (Part A is fully micro-fortified including B, Cu, Mo, Zn, Mn, Fe, Mo).
- GH Flora Series Micro contains the micros — that's why Micro is mandatory regardless of stage.
- MegaCrop / Greenleaf single-part also fully micro-fortified.
- Cheaper/incomplete lines may skip Si (almost always sold separately) and assume tap-water Cl.

## Critical Concept — EC Targets by Stage

The master EC table. Numbers are the *finished feed* including base + Cal-Mg + additives, on the EC scale (mS/cm), at standard PPFD (600–900 µmol·m⁻²·s⁻¹). Higher PPFD or CO2 supplementation pushes EC up; lower PPFD pulls it down.

| Stage | EC range | Notes |
|---|---|---|
| Seedling / clone | 0.4–0.8 | Light feeds only; over-fertilization stalls root growth |
| Early veg (week 1–2 after transplant) | 0.8–1.2 | Ramp gradually |
| Mid veg (week 3–4) | 1.2–1.6 | Plant is in steepest N demand |
| Late veg / pre-flip | 1.6–1.8 | Stop pushing if late-flip stretch is a concern |
| Stretch / week 1–2 flower | 1.6–2.0 | Don't crash EC at flip |
| Week 3–5 flower | 2.0–2.6 | Peak demand; bud-set + bulk |
| Week 6–7 flower | 1.8–2.2 | Begin tapering |
| Late flower / ripening (week 8+) | 1.6–2.0 | Tapering, NOT flushing |
| Optional flush (if doing) | 0–0.6 plain pH'd water | See flush debate below |

**Per-medium adjustment multiplier** (apply to the table above):

| Medium | EC multiplier | Reasoning |
|---|---|---|
| Synthetic-fed soil (FFOF, FFHF, etc.) | 0.6–0.8× | Soil already has nutrient charge; less needed |
| Pre-amended living soil | 0× synthetic | Use organic top-dress instead — see `06-nutrients-organic.md` |
| Coco-perlite | 0.9–1.1× | Coco binds Ca and is hydroponic — full strength expected |
| Rockwool / hydro / NFT | 0.8–1.0× | Standard hydroponic, follow mfg |
| DWC / RDWC | 0.6–0.8× | Roots have constant access — less is plenty |
| Aero / fogponics | 0.5–0.7× | Most efficient uptake of any system |

(Tier 2 — Athena Pro, Canna technical bulletins; Tier 1 — Bugbee EC×PPFD interaction research at Utah State CPL.)

**Diagnostic shortcut:** runoff EC (soil/coco) or res EC (hydro) should be within 0.3 of input EC. Higher = salt accumulation, flush or lower input. Lower = plant is consuming faster than supply, raise input.

## Critical Concept — Multi-Part Systems and Why They Exist

Synthetic lines come in 1, 2, or 3 parts (occasionally more). The reason isn't marketing — it's salt chemistry.

**The precipitation problem:** Calcium ions (Ca²⁺) and phosphate ions (PO₄³⁻) react in concentrated solution to form calcium phosphate, which precipitates out as a milky white solid. Same for calcium sulfate (gypsum). Once precipitated, these elements aren't bioavailable — they're rocks. So nutrient lines either:
- Bottle Ca separately from P/S (multi-part), OR
- Use chelation chemistry that prevents precipitation in dilute solution (some 1-parts), OR
- Restrict the formula to omit one of the offending elements (most "bloom" parts skip Ca)

| Format | Examples | How it works |
|---|---|---|
| **2-part (A+B)** | Athena Pro, Athena Blended, Canna Coco A+B | Part A holds Ca + N; Part B holds P + K + S. Mix into water separately, never bottle to bottle |
| **3-part** | GH Flora Series (Micro + Gro + Bloom), House & Garden | Micro holds Ca + micros; Gro holds N+K (veg); Bloom holds P+K (flower). Adjust ratio across stages |
| **3-component (Jack's 321)** | Jack's Part A (5-12-26) + Calcium Nitrate + Epsom | All three are dry salts. Mix each into water sequentially. The cheapest mineral system in cannabis |
| **1-part** | MegaCrop, Greenleaf, Front Row Ag | Uses chelation + dilute chemistry to keep all elements stable in one bag. Convenient, slightly less precise |

**"pH Perfect" decoded:** Advanced Nutrients pH Perfect uses a proprietary buffer chemistry (zwitterionic chelates per their own statements) that auto-corrects pH toward 5.6 over 10–14 days in lab conditions (Tier 2 — Advanced Nutrients technical statements). In practice it works in soft water, struggles in hard tap water with high alkalinity, and is significantly more expensive per EC than Athena or Jack's. Treat the pH-Perfect claim as "buffered, not magic" — measure pH anyway.

---

## NUTRIENT LINES

### Athena Pro (powder, A+B)

**Profile:**
- Form: dry powder, 2-part (Pro Core + Pro Grow OR Pro Bloom)
- Targets: hydro, coco, RO water mandatory
- Headline: fully-defined commercial line, no hidden chelators, transparent labels
- NPK at full mix: ~3-1-3 (veg), ~2-1-3 (bloom)

**Pros:**
- Most predictable line on the market
- Salt purity is exceptional — runs clean in fertigation systems
- Identical results from bag to bag, year to year
- Cheap per EC at scale (cost-per-pound math beats every liquid line)
- Stack with Athena Stack additives or run base alone

**Cons:**
- Requires RO — high tap alkalinity wrecks the buffer
- Powder mixing requires a stir or paddle (not shake-and-pour)
- Schedule defaults are aggressive (target 2.0 EC veg / 2.7 EC flower) — designed for high-PPFD CO2 rooms, lower for ambient setups
- Premium price point; not the cheapest hobby option

**Best-fit:** intermediate to commercial growers in coco/hydro with RO. Especially good for fertigation systems that benefit from clean salts.

**Schedule shape (Tier 2 — Athena official):**
- Seedling/clone: 0.8 EC
- Early veg: 1.2–1.6 EC
- Late veg: 1.8–2.0 EC
- Stretch: 2.0–2.2 EC
- Mid flower: 2.4–2.7 EC
- Late flower: 2.0–2.4 EC

**Common pitfalls:**
- Mixing Pro Core + Pro Bloom in the same concentrate tank → precipitation
- Running schedule at 3.0+ EC without high PPFD/CO2 to match → toxicity
- Using on tap water with alkalinity >100 ppm CaCO3 → pH instability

### Athena Blended (liquid, A+B)

**Profile:**
- Form: liquid concentrate, 2-part (Blended Veg + Blended Bloom)
- Same chemistry philosophy as Pro but in liquid
- Slightly more forgiving than Pro — designed for coco/hydro/soilless

**Pros:**
- Easier to mix than powder (pour and stir)
- More forgiving on water quality than Pro
- Same clean salts, same predictability

**Cons:**
- More expensive per EC than Pro powder
- Concentrate density is high — measure carefully, easy to overdose

**Best-fit:** intermediate growers wanting Athena chemistry without the powder-mixing step.

### Canna Coco A+B (and Hydro / Terra)

**Profile:**
- Form: liquid concentrate, 2-part
- Coco version optimized for coco substrate; Hydro for inert; Terra for soil
- EU standard, available globally
- NPK varies by part — typical full mix ~2-1-3

**Pros:**
- Medium-specific tuning is real — Coco includes Ca for coco's CEC, Hydro doesn't need extra
- Long track record, very consistent
- Pairs cleanly with Canna Boost, Canna PK 13/14, Cannazym additives
- Documentation is excellent

**Cons:**
- Multiple medium-specific SKUs — must order the right one
- Boost / PK / Cannazym ecosystem encourages additive sprawl
- Mid-range cost — not the cheapest, not the most expensive

**Best-fit:** intermediate growers in coco who want a complete system with documented support.

**Schedule shape (Tier 2 — Canna official):**
- Seedling: 0.25 ml/L A + 0.25 ml/L B, pH 5.7
- Early veg (day 14+): 0.5 ml/L A + 0.5 ml/L B
- Veg: 0.5–0.75 ml/L A + B
- Flower: 1.0–1.5 ml/L A + B (depending on strain demand)
- Pre-soak new coco: 20–30 ml/10L A+B with 40 ml/10L Rhizotonic before planting
- Target pH: 5.8–6.2

### General Hydroponics Flora Series (Flora Micro / Gro / Bloom)

**Profile:**
- Form: liquid concentrate, 3-part (Micro + Gro + Bloom)
- The longest-running hobby hydro line; reference for "3-part nutes"
- Micro contains Ca and micros; Gro is N-heavy; Bloom is PK-heavy
- Flora Micro available in two versions: regular (for soft/RO) and Hardwater (for tap >150 ppm hardness)

**Pros:**
- Cheap, available everywhere (even hardware stores)
- Good documentation, well-known Lucas formula and 3-2-1 / 2-1-1 / 1-2-3 ratios
- Forgiving of mistakes
- Can be tuned across stages by adjusting Gro:Bloom ratio without changing base

**Cons:**
- Liquid concentrate is heavy and bulky
- Some growers report inconsistent batches
- Not as "clean" in fertigation systems as Athena/Canna

**Best-fit:** beginner to intermediate hobbyists, hydro and coco. The default first-line many growers learn on.

**Mixing order (mandatory, Tier 2 — GH official):** water → CalMag (if using) → Micro → mix → Gro → mix → Bloom → mix → adjust pH. Reversing order causes calcium phosphate precipitation.

**Common stage ratios:**
- Lucas formula (DWC simplification): 0 ml Gro + 5 ml Micro + 10 ml Bloom per gallon, all stages
- Standard veg: 3 ml Micro + 2 ml Gro + 1 ml Bloom
- Standard flower: 1 ml Gro + 2 ml Micro + 3 ml Bloom (or 1-2-3)

### Jack's Nutrients 321 (dry, 3-component DIY)

**Profile:**
- Form: dry salts, 3 components
- Part A: Jack's Hydroponic 5-12-26 (the "complete" formula minus Ca/Mg)
- Part B: Calcium Nitrate (15.5-0-0)
- Part C: Magnesium Sulfate (Epsom salts)
- Cheapest mineral nutrient system in cannabis on a cost-per-EC basis
- Food-grade salts, no dyes, no proprietary additives

**Pros:**
- Cheapest by far at scale (commercial growers buy 25 lb bags)
- Transparent — every element is on the label
- Clean salts, runs perfectly in fertigation
- Works across all hydroponic systems and coco
- Dry storage doesn't degrade

**Cons:**
- DIY mixing required — must weigh grams, can't squeeze a bottle
- Three separate components to track
- Mixing order matters (A → Epsom → B last)
- Some hobbyists find the gram-precision tedious

**Best-fit:** intermediate to advanced growers comfortable with DIY measuring. Especially good for coco/hydro at any scale.

**The 321 recipe (Tier 2 — Jack's official):**
- Per gallon water (full strength, ~750 ppm @ 500 scale, ~1.5 EC):
  - 3.6 g Part A (Jack's 5-12-26)
  - 2.4 g Part B (Calcium Nitrate)
  - 1.2 g Part C (Epsom Salt)
- Newer official ratio: 3.79 / 2.52 / 0.99 g
- 50% strength: 1.5 / 1.0 / 0.5 g
- Mixing order (mandatory): Part A first → Epsom second → Calcium Nitrate last (reversing causes precipitation)

**Common pitfalls:**
- Mixing Calcium Nitrate before Part A → calcium phosphate precipitate (white cloud)
- Using non-food-grade calcium nitrate (greenhouse grade is fine; technical grade may have impurities)
- Not weighing — eyeballing grams is unreliable at small scale

### MegaCrop / Greenleaf Nutrients (1-part dry)

**Profile:**
- Form: dry, 1-part single bag
- Contains all 14 mineral elements + chelators in one formula
- Hobby-tier price ($25–60 for enough to grow many plants)
- NPK ~9-7-20 (varies by version — MegaCrop, MegaCrop A, etc.)

**Pros:**
- Single bag — simplest possible feeding
- Cheap
- All elements included, no separate Cal-Mg needed for some setups
- Good for unattended setups

**Cons:**
- Less precise than multi-part — can't shift Ca:N ratio independently
- Not as clean in fertigation as Athena/Jack's
- Some users report variable batch quality
- Single ratio means compromise between veg and flower demands

**Best-fit:** budget hobby growers, autoflowers, set-and-forget setups.

### Advanced Nutrients pH Perfect Connoisseur

**Profile:**
- Form: liquid concentrate, 2-part (Connoisseur Grow + Bloom, A+B each = 4 bottles)
- Premium-priced boutique line
- pH Perfect technology — proprietary buffer that holds pH in 5.5–6.3 range without manual adjustment
- Heavy additive ecosystem (Big Bud, Bud Candy, Voodoo Juice, etc.)

**Pros:**
- Auto-pH claim works in clean RO/soft water — saves the pH-down step
- Marketing/support infrastructure for hobbyists who want hand-holding
- Rich additive lineup if you want it

**Cons:**
- Most expensive line per EC
- pH Perfect doesn't hold reliably in hard tap water with high alkalinity
- Additive sprawl is a sales funnel — most additives don't outperform a clean base
- "Perfect" claim oversold — measure pH regardless

**Best-fit:** hobby growers who value convenience over cost and want a single ecosystem.

### Fox Farm Trio (Big Bloom + Grow Big + Tiger Bloom)

**Profile:**
- Form: liquid concentrate, 3-part
- Big Bloom: 0.01-0.3-0.7 (organic-blended bloom helper)
- Grow Big: 6-4-4 (synthetic veg)
- Tiger Bloom: 2-8-4 (synthetic bloom)
- Available everywhere in US, common starter

**Pros:**
- Easy to find at any garden store
- Documentation is dead-simple
- Works well in Fox Farm soil mixes (Ocean Forest, Happy Frog) — designed to pair
- Beginner-friendly

**Cons:**
- Not optimal for coco/hydro — designed for soil
- Not as clean or precise as Athena/Canna/Jack's
- Big Bloom is partially organic (bat guano + earthworm castings) — clogs hydro systems
- Most experienced growers move on after first 1–2 grows

**Best-fit:** first-time soil growers in the US.

### House & Garden Aqua Flakes (and Cocos A+B)

**Profile:**
- Form: liquid concentrate, 2-part
- Premium EU line
- Aqua Flakes for hydro/rockwool/NFT; Cocos A+B for coco
- Heavily mineral-loaded, predictable

**Pros:**
- Excellent quality control
- Professional-grade results
- Pairs with H&G's full additive line for diminishing-returns optimization

**Cons:**
- Expensive
- Not widely available in US
- Locked-in additive ecosystem if you buy the whole line

**Best-fit:** EU/UK growers in coco/hydro wanting premium consistency.

---

## Mixing Protocol — Order of Addition

The order is a chemistry requirement, not a preference. Reversing causes precipitation, lockout, and wasted product.

**Standard order for any 2-part or 3-part synthetic line:**
1. Plain water in clean container
2. **Silica** if using (potassium silicate or mono-silicic) — raises pH, must be first
3. **Cal-Mg** if using — adds Ca buffer ahead of phosphate parts
4. **Calcium-bearing part** — Athena Pro Core / Canna A / GH Micro / Jack's Part A
5. Mix fully (30+ seconds, vortex if available)
6. **Phosphate-bearing part** — Athena Pro Bloom / Canna B / GH Bloom / Jack's Part B
7. Mix fully
8. **Micros / supplements** — bloom boosters, enzymes, root inoculants
9. **Adjust pH last** — to medium-appropriate target (see `05-water-quality.md`)

**Why each step matters:**
- Silica first because it's high pH (~10–11) and reactive with everything else
- Cal-Mg before phosphate so Ca is already in solution before P arrives
- Calcium part before phosphate part to dilute Ca before P concentration spikes
- Mix between additions to disperse before next concentration arrives
- pH last because every addition changes pH — adjusting earlier wastes acid

**Stock solution prep (commercial / repeat batches):**
- Keep Ca-tank and P-tank separate in concentrated form
- Inject through dosing pumps into mixed water at point of use
- Never bottle Ca and P concentrates together — they precipitate in hours

**Common precipitation symptoms:**
- White cloud forming in res = calcium phosphate
- Clear at first then white sediment after 24h = same, slow
- Brown sludge in dosing lines = chelated iron crashed out at wrong pH
- Cure: dump res, clean lines with food-grade citric acid or diluted phosphoric, restart

---

## Bloom Boosters, PK Bumps, and Additives

**The honest framing:** most additives produce small, hard-to-measure benefits. Some are useful in specific situations. Many are pure margin for the manufacturer. Bugbee's general position (Tier 1 — Utah State CPL) is that no scientific research supports bloom-booster claims for cannabis — he recommends a balanced 20-10-20 from start to finish. The Rx Green Technologies Bulk PK study (Tier 2) found a yield bump but no THC or terpene gain.

**Categories:**

| Additive type | Examples | Honest verdict |
|---|---|---|
| **Mono-PK / PK boost** | Canna PK 13/14, Athena Bloom Boost, RAW Bloom | Small yield bump in commercial trials, no quality gain. Use weeks 4–6 if at all |
| **Carbohydrate / sugar** | Bud Candy, Sweet, Molasses | Mostly placebo per Bugbee. Soil microbes might use it; synthetic feeds don't need it |
| **Bloom boosters (multi-ingredient)** | Big Bud, Overdrive, Bud Ignitor | Marketing-driven. Often just PK + buffers + dye |
| **Beneficial microbes (synthetic-compatible)** | Hydroguard (Bacillus), Mammoth P (P-solubilizing bacteria) | Hydroguard works in DWC for root rot prevention. Mammoth P modest in some setups |
| **Mycorrhizae** | Great White, Mykos | Useful in soil/coco transplant. Pointless in hydro (no surface) |
| **Enzymes** | Hygrozyme, Cannazym | Real effect in coco/hydro for breaking down dead root material — modest but legitimate |
| **B vitamins / kelp** | Rhizotonic, Superthrive | Stress reduction at transplant; weak ongoing benefit |
| **Silica** | Mono-Si, Power Si, Armor Si, potassium silicate | Real benefit (cell wall strength, heat tolerance, IPM resistance). Use through veg + early flower |

**Decision rule:** if a base nutrient line (Athena, Canna, Jack's) doesn't include it, ask whether the marginal benefit justifies the cost AND whether it interferes with the base chemistry. For a beginner, base + Cal-Mg + silica is enough. Additives are last-10% optimization.

---

## The Flush Debate

"Flushing" = running plain pH'd water for 1–14 days before harvest, intended to deplete leaf nutrients for smoother smoke and lighter ash.

**Folk wisdom:** flush 7–14 days, plant fades, smoke is smoother.

**The Rx Green Technologies study (Tier 2, peer-style methodology):**
- Compared 0, 7, 10, 14-day flush periods on Cherry Diesel
- **No yield difference** between any flush length
- **No potency difference** (THC equivalent across treatments)
- **No terpene difference**
- **Taste-test panel slightly preferred ZERO-day flush** — opposite of folk wisdom
- 14-day flush had higher Fe and Zn in flower (likely from depleted plant pulling micros from water)
- Conclusion: no benefit to flushing

**Bugbee's commentary (Tier 1):** consistent with general Utah State CPL position — plants don't "store" extra nutrients to be flushed out; nutrient content of finished flower is set by pre-harvest physiology, not late flushing.

**The middle path: tapering, not flushing**
- Drop EC gradually over weeks 6–8 (1.6 → 1.2 → 0.8)
- Plant fades naturally as it senesces
- No yield loss, no diagnostic value of flushing achieved without the cost
- Achieves visual fade some growers want without the dogma

**When flushing genuinely helps:**
- Salt buildup detected (runoff EC creep above 3.0) — flush to reset substrate
- Suspected toxicity (overfeeding, lockout cascade) — flush as corrective, not pre-harvest ritual
- Switching nutrient lines mid-grow — flush to clean slate

**Bottom line:** flushing as pre-harvest ritual is not supported by data. Tapering is fine. Salt-correction flushes are mechanically useful when needed. Don't flush "just because."

---

## Feed Schedule Construction

Most manufacturer-published "full" schedules are aggressive — they assume optimal PPFD, CO2, and high-vigor strains. Many growers run "lite" schedules (50–70% of full) and get equal or better results because the plant isn't fighting toxicity headwinds.

**When to run aggressive (full mfg or above):**
- High PPFD (>900 µmol·m⁻²·s⁻¹)
- CO2 supplementation (1000–1500 ppm)
- Sealed room with tight environmental control
- High-yielding heavy-feeder strains (Critical, Big Bud, Gorilla Glue heavy phenos)
- Coco daily fertigation at 10–20% runoff

**When to run lite (50–70% mfg):**
- Ambient CO2 (~400 ppm)
- Lower PPFD (<700 µmol·m⁻²·s⁻¹)
- Connoisseur strains, sativa-leaning, light feeders
- Soil with pre-amended starter mix
- Smaller containers (<3 gal)
- First-time growing the strain

**Custom Hoagland for fully-defined research:**
- Hoagland & Arnon (1933) modified solution: standard for plant research
- 210 ppm N, 31 ppm P, 235 ppm K, 200 ppm Ca, 48 ppm Mg, 64 ppm S, plus chelated micros
- Cannabis-modified versions raise K and adjust micros for flowering demand
- Used in academic papers (Caplan/Zheng, Bugbee) — useful reference for what "balanced" looks like

**Reading runoff to dial in:**
- Soil/coco: collect 20% runoff, measure EC and pH
- Target runoff EC = input EC ±0.3
- Runoff EC creeping up by 0.3+ over 3 feeds → reduce input or run a clearing
- Runoff EC dropping below input → plant consuming faster, raise input by 0.2

---

## Per-Medium Adjustment

| Medium | Synthetic feed strategy |
|---|---|
| **Synthetic-fed soil** | 50–70% mfg dose; feed every 2–3 waterings; rely on soil buffer; runoff infrequent |
| **Pre-amended soil (FFOF, FFHF, Subcool Super Soil)** | Plain water for first 2–4 weeks while charge runs out; light synthetic afterward |
| **Living soil** | Don't use synthetic — kills biology; see `06-nutrients-organic.md` |
| **Coco-perlite** | 90–110% mfg dose; daily fertigation 10–20% runoff; pre-buffer new coco |
| **Hydro / rockwool / NFT** | 80–100% mfg dose; res change weekly; track EC drift |
| **DWC / RDWC** | 60–80% mfg dose; constant root access means lower EC sufficient; air pumps essential |
| **Aero / fogponics** | 50–70% mfg dose; most efficient uptake; light hand needed |

---

## Quick Reference — Line Selection Decision Tree

```
START → What's your medium?

SOIL?
├── First grow, US, cheap → Fox Farm Trio
├── Living soil → Wrong file (06-nutrients-organic.md)
├── Pre-amended (FFOF/FFHF) → Plain water 2-4 weeks, then Jack's 321 lite
└── Synthetic-fed soil, intermediate → Jack's 321 or Canna Terra

COCO?
├── Beginner → Canna Coco A+B
├── Intermediate, budget → Jack's 321
├── Intermediate, want a stack → Canna Coco + Boost + PK
├── Advanced/commercial → Athena Pro
└── Premium EU → House & Garden Cocos A+B

HYDRO (any system)?
├── Beginner DWC → GH Flora Series (Lucas formula)
├── Beginner RDWC → Hydroguard + Jack's 321 or GH Flora
├── Intermediate any → Athena Blended or Jack's 321
├── Commercial fertigation → Athena Pro
└── Aero / NFT → Athena Pro or House & Garden Aqua Flakes

BUDGET-FIRST PATH?
├── Cheapest mineral system → Jack's 321
├── Single-bag simplicity → MegaCrop / Greenleaf
└── Cheapest available retail (US) → Fox Farm Trio

CONVENIENCE-FIRST PATH?
├── No-pH-adjust claim → Advanced Nutrients pH Perfect
├── Single-bag simplicity → MegaCrop
└── Pre-mixed feed kits → many brands sell starter kits
```

---

## Common Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| "Mfg schedule isn't working" | pH lockout cascade | Test runoff pH; if drift >0.5 from target, that's the cause, not the schedule |
| Tip burn → "salt buildup" | K toxicity from over-PK boost | Check K-bump dosing; reduce, run clearing, watch recovery |
| Tip burn → light burn | Top-of-canopy only burn | Light burn = top leaves; nute burn = consistent across plant |
| Dark-green claw → strain genetics | N toxicity (overfeeding) | Reduce N, watch new growth; if green stays dark + clawed = N tox confirmed |
| 800 ppm reading "too high" | 700-scale meter showing equivalent of 560 on 500-scale | Confirm scale; same EC reads different PPM by meter brand (see `05-water-quality.md`) |
| "Switched lines and crashed" | Nute conflict, residual buffer mismatch | Always flush 1.5x pot volume between line changes |
| "Athena schedule fried my plants" | Schedule designed for high-PPFD CO2 — without those, EC too high | Run 70% of Athena's published EC if no CO2 / under 800 PPFD |
| Mid-flower stall after PK boost | Lockout from over-PK pushing micros down | Reduce PK, return to balanced base, foliar Fe |
| Cloudy res after mixing | Calcium phosphate precipitation from wrong mixing order | Dump and remix in correct order |
| "Need bloom booster, plant looks tired week 6" | Senescence / programmed fade | Check trichomes — if ripening, you're seeing finish, not deficiency |

---

## Verification Questions Before Acting

1. What nutrient line is in use, and which parts/products?
2. Current EC of the input feed?
3. Runoff or res EC?
4. Input pH and runoff/res pH?
5. Stage and week-in-stage?
6. Medium and container size?
7. PPFD at canopy + CO2 status (ambient or supplemented)?
8. Source water type (RO/tap/well) and starting EC?
9. Last schedule change?
10. Cal-Mg, silica, additives in current mix?

If 4+ unknown → don't recommend nute changes. Get the data first.

---

## Sources

- **Tier 1** — Bugbee, B. (Utah State Crop Physiology Lab) — EC × PPFD interaction, position on PK boosters and balanced fertilization
- **Tier 1** — Caplan, D. & Zheng, Y. (University of Guelph) — cannabis-specific fertilizer rate trials, organic vs synthetic comparisons
- **Tier 1** — Hoagland, D. & Arnon, D. (1933) — original modified Hoagland solution standard
- **Tier 1/2** — Rx Green Technologies — flushing trial (no yield/quality benefit), Bulk PK booster study
- **Tier 2** — Athena Pro Line feed schedules and technical bulletins
- **Tier 2** — Canna Research (Canna Coco / Hydro / Terra technical documentation, feed charts)
- **Tier 2** — General Hydroponics Flora Series technical, mixing protocols, Lucas formula
- **Tier 2** — Jack's Nutrients (JR Peters) 321 official feeding chart, salt analysis
- **Tier 2** — Advanced Nutrients pH Perfect technology white papers
- **Tier 2** — Greenleaf Nutrients (MegaCrop) feeding guide
- **Tier 2** — Fox Farm feeding schedule
- **Tier 2** — House & Garden Aqua Flakes / Cocos technical
- **Tier 3** — Cervantes, J. *The Cannabis Encyclopedia* — nutrient chapter
- **Tier 3** — Rosenthal, E. *Marijuana Grower's Handbook* — synthetic feed schedules
- **Tier 3** — DeBacco University fertilizer lectures
- **Tier 3** — Mr. Canucks Grow line comparisons and reviews

---

## Cross-References

- Source water EC/alkalinity drives feed math → `05-water-quality.md`
- Medium-specific multipliers and pH targets → `04-medium-soil.md`, `04-medium-coco.md`, `04-medium-hydro.md`, `04-medium-living-soil.md`
- Organic alternative — different mental model entirely → `06-nutrients-organic.md`
- Toxicity symptoms (the symmetric risk) → `07-deficiencies.md`
- Flowering-specific PK timing → `12-flowering.md`
- Custom feed schedule generation workflow → `references/workflows/build-feed-schedule.md`
- Diagnostic flowchart that branches to nute issues → `21-troubleshooting-tree.md`
