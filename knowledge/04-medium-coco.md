# 04 — Medium: Coco

Coco coir cultivation — coco prep, buffering chemistry, Cal-Mg requirements, daily fertigation protocol, crop steering, and reuse. **Coco is hydroponic in soil's clothing** — the mental model is closer to RDWC than to soil. New growers who treat coco like soil run into Ca/Mg deficiency, pH lockout, and salt creep within weeks. Cross-reference with `04-medium-soil.md` (the contrast — different cycle, different pH, different feeding cadence), `04-medium-hydro.md` (closer cousin — runs many of the same fertigation principles), `05-water-quality.md` (RO + Cal-Mg requirement), `06-nutrients-synthetic.md` (coco-specific feed schedules — Athena Pro, Canna Coco A+B, Jacks 321), `07-deficiencies.md` (Ca, Mg, and Fe lockouts dominate coco diagnostic work).

## How to Use This File

Diagnostic order for any coco problem:

1. **pH first** — coco has zero buffer; runoff or substrate pH outside 5.5–6.3 = lockout
2. **EC second** — runoff EC creep above input is the salt warning
3. **Cal-Mg presence** — is supplementary Cal-Mg in the feed at adequate dose?
4. **Fertigation cadence** — too few feeds = nute starve + pH drift; too few runoffs = salt creep
5. **Coco prep state** — was it buffered? Pre-buffered RHP product or DIY raw brick?
6. **Brand quality** — sodium content, RHP certification, lignin chunk ratio

## Core Concepts

| Concept | What it means | Why it matters |
|---|---|---|
| **Coco is hydroponic, not soil** | Inert substrate that delivers feed solution to roots; no nutrient buffer worth relying on | Treating coco like soil = guaranteed deficiencies and lockout |
| **Daily (or multi-daily) fertigation is normal** | Production runs at 3–5 fertigations per day in mature flower | Coco is the wrong choice for "I water once a week" growers |
| **Cal-Mg from day 1, every feed** | Coco binds Ca and Mg at CEC sites; deficiency starts immediately without supplementation | Skipping Cal-Mg is the #1 coco beginner mistake |
| **pH range 5.5–6.3, narrow vs soil** | Hydroponic-style root pH window | Tight tolerance — calibrate pH meter monthly, never run >6.3 |
| **High CEC = buffering required first** | Cation exchange sites release K and Na in exchange for Ca and Mg until "filled" with calcium | Unbuffered raw coco starves plants for Ca even with Cal-Mg in feed |
| **Runoff every fertigation, every time** | 10–20% runoff prevents salt creep, refreshes substrate | Skipping runoff = EC stacking = osmotic uptake failure within weeks |
| **Don't let coco fully dry** | Recovery from full drydown is slow; can damage CEC structure and channel water past the substrate | Soil's "lift weight, water when light" rule does NOT apply |

## What Is Coco Coir

Coco coir is the **fibrous husk material between the inner shell and outer skin of a coconut**. It's a byproduct of coconut processing — historically discarded, now widely valued as a hydroponic substrate.

### Forms

| Form | Use case | Notes |
|---|---|---|
| **Compressed brick** (~5 kg → ~70 L expanded) | Low-cost bulk; storage convenience | Requires hydration + prep before use |
| **Loose bag** | Ready-to-use, often pre-buffered | Higher per-liter cost; standard for most home grows |
| **Slab** | Commercial drip systems; 1m × 15cm × 6cm typical | Drip-fed throughout cycle |
| **Coco cubes / blocks** | Propagation, clones | Convenient but $$$ per liter |

### Particle Mix
Coco is sold as different ratios of:
- **Fine pith / dust** — high water retention, packs tighter, slower drainage
- **Chunky fiber** — air pockets, faster drainage, lower water holding

A good production coco runs roughly **70% pith + 30% chunky fiber**. Pure pith stays wet too long; pure fiber dries too fast and channels water past roots.

## Coco Brands and Quality

The single most important quality marker is the **RHP certification** (Royal Horticultural Product, Dutch standard). RHP-certified coco has been:
- Triple-washed for low EC out of bag (typically <0.5 mS/cm)
- Buffered with Ca-Mg solution
- pH-stabilized
- Tested for low sodium and chloride

| Brand | Pre-buffered? | RHP-certified? | Notes |
|---|---|---|---|
| **Canna Coco Pro / Pro Plus** | Yes | Yes | The industry gold standard. EC <0.6 out of bag, pH stabilized 6.0–6.5. Pro Plus contains Trichoderma. |
| **Char Coir** | Yes | Yes | Triple-washed, buffered, low EC. Strong reviews. Loose-fill, slabs, cubes available. |
| **Coco Bliss / Plantonix** | Yes | Yes (varies by SKU) | Mid-tier, decent quality |
| **House & Garden Cocos** | Yes | Yes | Premium European brand |
| **GH CocoTek** | Yes | Limited | Big-box availability |
| **Mother Earth Coco** | Yes | No | Budget, mixed reviews on consistency |
| **Pelemix bricks** | No | No | Lowest cost compressed bricks; full DIY prep required |
| **Generic / unbranded compressed** | No | No | High Na content risk, lignin chunks, prep mandatory |

### Quality Red Flags (Out of Bag)
- **EC > 0.8 mS/cm** — unwashed, high salt content (suspect Na)
- **pH > 7.0 or < 5.5** — not pH-stabilized
- **Visible long lignin chunks** — woody material that won't break down, channels water
- **Sour or fermented smell** — anaerobic processing or contamination
- **Dried-blood-red color** — typically older / oxidized; lower CEC available

## Coco Prep / Buffering

### Why Buffering Matters
Coco's negatively-charged CEC sites are filled with **K (potassium) and Na (sodium)** as it comes from the coconut. When Ca²⁺ or Mg²⁺ ions hit those sites in solution, they **displace** the K and Na (because divalent cations bind more strongly than monovalent). Until the CEC sites are pre-loaded with Ca and Mg ("buffered"), every Cal-Mg dose you add gets absorbed by the substrate instead of reaching the plant — guaranteeing Ca-Mg deficiency.

Failing to buffer is the #1 reason new coco growers see Ca-Mg deficiency despite running Cal-Mg supplements. (Tier 2 — Coco For Cannabis, Botanicare, Shogun all confirm.)

### Pre-Buffered Products (the easy path)
RHP-certified products (Canna Coco Pro, Char Coir, etc.) are pre-buffered at the factory. **Recommended:** still flush once with pH 5.8 RO + 1 ml/L Cal-Mg before first use to refresh and verify substrate state — but the heavy lifting is done.

### DIY Buffering Protocol (Raw Coco Bricks)

**Step 1 — Hydrate.** Place the brick in a container, add 5–7× brick volume of warm dechlorinated water. Wait 1 hour for full expansion.

**Step 2 — Initial rinse.** Drain the hydration water (it's full of Na, K, and tannins). Rinse with another 2× volume of plain RO/dechlorinated water until runoff EC < 1.0.

**Step 3 — Buffer with Cal-Mg solution.** Mix per ~5 gallons:
```
5 gallons RO/dechlorinated water
14 g calcium nitrate (Ca(NO₃)₂)  ≈ 0.5 oz
4 g magnesium sulfate (MgSO₄, Epsom salts)  ≈ 0.14 oz
pH adjusted to 5.8
Resulting EC ~1.5–1.8 mS/cm
```

OR simpler: 5 gal RO + 1.5 ml/L Cal-Mg supplement (Botanicare, GH CaliMagic, Athena Stack), pH 5.8.

**Step 4 — Soak.** 2 gallons of buffer solution per 1 gallon of coco. Apply in 2 stages (half, mix, half, soak ≥6 hr).

**Step 5 — Drain.** Allow to fully drain.

**Step 6 — Final rinse (optional).** 1 pot-volume of pH 5.8 RO. Some growers skip this; it removes excess buffer salts but isn't critical.

**Step 7 — Coco is ready.** It's now CEC-loaded with Ca and Mg, salt-free, pH-stable. Treat exactly like pre-buffered product going forward.

### Skipping Buffering
If you skip buffering on raw coco:
- Week 1: plants look OK
- Week 2–3: lower-leaf interveinal yellowing (Mg def) and new-growth tip distortion (Ca def)
- "I'm running Cal-Mg though" — yes, but the substrate is eating it before the plant can
- Result: chase deficiencies for 2–3 weeks until enough Ca finally saturates the CEC sites

## Coco-Perlite Ratios

| Ratio | Behavior | Best for |
|---|---|---|
| **100% coco** | Maximum water retention, longest dryback, requires fewer fertigations | Modern commercial high-frequency fertigation; small pots; auto-fertigation systems |
| **70/30 coco/perlite** | Moderate aeration, hand-watering friendly | Hobby tents, hand-watered grows, mid-frequency fertigation |
| **50/50 coco/perlite** | Maximum aeration, fast dryback | Large pots, hand-watering, hot rooms |
| **Pure perlite** | Drains instantly, no retention | Niche; clones / propagation |

**Default for most modern grows:** 100% coco for production drip systems, 70/30 for hand-watered tents.

## Container Selection for Coco

| Container | Coco use notes |
|---|---|
| **Fabric pot** | Excellent — fast dryback, air pruning. Most common coco choice. Sizes 1–7 gal. |
| **Plastic pot** | Works fine — drainage holes critical, slower dryback than fabric |
| **Air pot** | Excellent for long runs and mother plants |
| **Slab on tray** | Commercial drip — 1m slab × 4–6 plants, dripper per plant |
| **Net pot in coco-filled bucket** | Hybrid coco-DWC (coco-DWC); niche |

**Container size in coco runs smaller than soil** because frequent fertigation compensates for lower buffer:
- Soil: 5–7 gal final
- Coco: 3–5 gal final is plenty for the same plant size

## pH and EC for Coco

### pH
- **Range:** 5.5 – 6.3
- **Optimal target:** 5.8 – 6.0
- **Above 6.3:** Fe, Mn, B, Zn lockout — common cause of "iron deficiency" in coco that's actually pH drift
- **Below 5.5:** Ca, Mg lockout, plus risk of root acid damage

Calibrate pH meter monthly with fresh 4.0 + 7.0 calibration solutions. Replace solutions every 6 months.

### EC by Stage (Synthetic Feed in Coco)

| Stage | Input EC | Notes |
|---|---|---|
| Seedling / clone | 0.4 – 0.8 | Quarter-strength + Cal-Mg always |
| Early veg | 1.0 – 1.4 | Building up |
| Mature veg | 1.4 – 1.8 | |
| Flower stretch | 1.6 – 2.0 | Transition feed |
| Mid flower | 2.0 – 2.4 | Peak demand |
| Late flower | 1.8 – 2.2 | Slight taper or hold |
| Last 1–2 weeks | 0.4 – 1.0 | Plain water + Cal-Mg or final flush per preference (see flush debate `12-flowering.md`) |

These are mid-range targets. Athena Pro pushes higher (3.0 EC in flower) and relies on aggressive runoff; House & Garden / Canna run lower (1.6–2.0). Match to your nutrient line — see `06-nutrients-synthetic.md`.

### Runoff EC Interpretation

| Runoff finding | Meaning | Action |
|---|---|---|
| Runoff EC ≈ input EC | Steady state, coco refreshing | Continue normal cycle |
| Runoff EC 0.3–0.5 above input | Mild salt accumulation | Increase runoff % to 20% next feed |
| Runoff EC 1.0+ above input | Salt creep — plant stressed | Leach with low-EC pH 5.8 solution |
| Runoff EC below input | Plant absorbing more than feed delivered | Increase feed EC slightly OR plant signaling drought stress |

Athena Pro's protocol intentionally stacks higher runoff EC (4–6 from 3.0 input) under "continual flushing" — this is a different operating mode that depends on aggressive runoff every cycle. It works but isn't beginner-friendly.

## Feeding / Fertigation Protocol

### The Daily-Feed Rule

In coco, every irrigation event is a fertigation event. There are no plain-water days unless intentionally flushing or transitioning.

Why: coco buffer is small. Plain water on coco that's been holding nutrient solution creates a momentary dilution that destabilizes CEC equilibrium and can drop substrate pH suddenly. Constant fertigation at the target EC keeps the substrate chemistry steady.

### Fertigation Frequency

| Plant size / stage | Fertigations per day |
|---|---|
| Seedling (1-gal coco) | 1 (sometimes hand-mist between) |
| Early veg | 1 – 2 |
| Mature veg | 2 – 3 |
| Flower stretch | 2 – 4 |
| Mid flower (mature plant in 3–5 gal) | 3 – 5 |
| Late flower | 3 – 5 |

(Tier 2 — Coco For Cannabis, Canna Pro Plus protocol both confirm.)

### Runoff Every Time
**10–20% runoff per fertigation event, mandatory.** Skipping runoff for one or two cycles to "save nutes" is the fastest way to salt the substrate and trigger lockout. Runoff is nonnegotiable in coco.

### Cal-Mg in Every Feed
Every fertigation includes Cal-Mg (in addition to base nutrients):
- **RO water:** 1.5–2 ml/L (e.g., GH CaliMagic, Botanicare Cal-Mag Plus)
- **Soft tap water:** 1.0 ml/L
- **Hard tap water:** 0.5 ml/L or skip if alkalinity already high

Some single-part nutrient lines (Athena Pro, Jacks 321) include enough Ca and Mg in the base feed to skip Cal-Mg supplementation if input water is correct. Check the line.

### Substrate Moisture Management
Coco should never go fully dry. Acceptable VWC range:

| State | VWC % | Plant signal |
|---|---|---|
| Saturated (post-fertigation) | 65 – 75 | Healthy |
| Working dryback | 50 – 65 | Healthy |
| Approaching dry | 40 – 50 | Time for next fertigation |
| Dry | < 40 | Stress threshold |
| Bone dry | < 25 | Recovery slow; CEC may be damaged |

Without sensors, observe: leaves slightly droop in late dryback (recovers in 30 min after fertigation), pot weight noticeably lighter than post-feed.

## Crop Steering (Modern Commercial Approach)

Crop steering uses **deliberate dryback management** to push plants between vegetative and generative growth phases via hydraulic stress signals. Originated in tomato/cucumber drip irrigation; cannabis adopted it for commercial coco and rockwool. (Tier 2 — AROYA, Growlink, climatecontrol.com all publish protocols.)

### Vegetative Steering (early veg + flower stretch)
- **Goal:** maximize shoot/leaf growth
- **Dryback target:** 5 – 10% VWC drop between irrigations (shallow)
- **Fertigation frequency:** higher (more events per day, smaller volumes)
- **Substrate stays wet** — plant doesn't experience drought stress

### Generative Steering (bud development, late flower)
- **Goal:** maximize flower/cannabinoid/terpene development
- **Dryback target:** 15 – 25%+ VWC drop overnight (deep)
- **Fertigation frequency:** lower (fewer events, larger volumes)
- **Mild repeated drought stress** drives generative response, denser buds, more resin

### Transition Window
The transition from vegetative to generative steering happens around **flower week 2–3** as bud sites form — gradually deepen the overnight dryback over several days.

### What You Need for Crop Steering
- VWC sensor (TEROS-12, Acclima, AROYA pucks): essential. Without measurement you're guessing.
- Programmable fertigation controller (multi-cycle daily timer minimum, full controller better)
- Drip irrigation per plant (uniform delivery)
- Discipline to log dryback values and adjust

For hand-watered hobby grows, crop steering is overkill. For commercial coco, it's now the default operating mode.

## Coco-Specific Issues

### Cal-Mg Deficiency (#1 issue, 90% of all coco diagnostic calls)
**Causes:**
1. Raw unbuffered coco (substrate eating the Cal-Mg before plant gets it)
2. No Cal-Mg in feed
3. RO water with too low Cal-Mg dose
4. pH out of range (lockout, not deficiency)
5. Low transpiration (high RH, weak airflow — see `02-environment.md`)

**Fix:** verify buffering, verify Cal-Mg dose, verify pH 5.8, verify VPD/airflow. In that order.

### Iron Deficiency (#2 issue)
**Cause:** pH > 6.3 in coco — lockout, not actual shortage. 90% of "Fe deficiency" reports in coco are pH drift.

**Fix:** lower input pH to 5.6–5.8 immediately. Iron will recover within 48 hours. If pH was correct, then look at chelated Fe-DTPA supplement.

### Salt Buildup
**Cause:** insufficient runoff, EC creep over weeks.

**Fix:** flush with low-EC (0.6) pH 5.8 solution at 1.5–2× pot volume. Resume normal feed at lower input EC for 2–3 cycles to let plant catch up.

### Coco Compaction
**Cause:** long runs (10+ weeks) with constant wetting and gravity. Reduces aeration.

**Fix:** prevention is everything — fabric pot, ≥30% perlite for hand-watered grows, gentle drip placement. Late-stage you can poke aeration holes with a chopstick but it's a band-aid.

### pH Drift Down (acidification)
**Cause:** synthetic feeds (especially nitric-acid-based pH down) gradually acidify substrate. Microbial activity from organic supplements can also drop pH.

**Fix:** check substrate pH via slurry test (see `04-medium-soil.md` slurry method); raise input pH slightly (6.0–6.1) for 3 cycles to bring substrate back up.

### Reused Coco
Coco can be reused 1–2 cycles if managed:

| Step | What |
|---|---|
| 1. Remove root mass | Root ball pulls out cleanly from fabric pots |
| 2. Rinse substrate | Plain pH 5.8 RO water, 2× pot volume |
| 3. Re-buffer | Cal-Mg solution at 1.5 EC, soak 4–6 hr |
| 4. Inspect | Smell sour or musty? Compost it. Smell neutral? Reuse. |
| 5. Add 20–30% fresh coco | Compensate for compaction loss |

After 2 reuses, the structural integrity has degraded enough that fresh coco is worth the cost.

### Sodium Toxicity
**Cause:** unwashed cheap coco + tap water with Na > 50 ppm = compounded sodium load.
**Symptom:** burnt leaf tips that don't respond to flushing or pH correction.
**Fix:** switch to RHP-certified coco, switch to RO water, leach existing coco.

## Confusion / Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| "Cal-Mg deficiency despite running Cal-Mg" | Unbuffered coco eating the Cal-Mg | Verify coco was buffered or RHP-certified; if not, follow buffering protocol |
| Iron deficiency | pH drift above 6.3 | Check input AND runoff pH; lower to 5.8 first before reaching for Fe supplement |
| "Soil-style watering schedule isn't working" | Coco is hydroponic — fertigate daily, runoff every time | Switch to coco protocol: feed every event, 10–20% runoff |
| Sudden dryback / wilting between feeds | Coco channels formed (water bypasses substrate) | Re-saturate slowly; consider coco compaction if late in run |
| EC creeping up despite low input | No runoff or hot tap water (Na buildup) | Verify input water Na; force runoff to 20%+; consider RO switch |
| pH crashed overnight | Microbial activity in substrate (organic additives) OR root rot | Slurry test pH; check root health (clean white = OK; brown slimy = rot) |
| Coco "doesn't dry out" | Coco fully wet at 75% VWC; if it doesn't drop below 60% in 6 hrs, room is too humid OR plant transpiration suppressed | Check VPD, airflow, plant health |
| Plants stressed at high Athena EC | Stacking salts because runoff was insufficient | Increase runoff %; or drop input EC |
| "Buffered out of bag — no need to verify" | Some "buffered" cheap brands aren't truly RHP-certified | Test runoff EC and pH on first feed; if EC > 1.5 from plain water input, re-buffer |
| Brown root tips in coco | pH crash OR overfeeding OR pythium | Slurry pH test first; if pH OK, consider feed strength; if both OK, suspect pythium |
| Late-flower yellowing | Normal fade in coco too | Don't push N or Cal-Mg this late — it's the plant ripening |
| Crop steering with no sensor | Guessing — no real steering happening | VWC sensor required; without it, run conservative single-EC fertigation |

## Quick Reference

### Buffering Recipe (DIY Raw Coco Brick)
```
For 5 gallons of buffer solution:
  5 gal RO or dechlorinated water
  14 g calcium nitrate (or 1.5 ml/L commercial Cal-Mg)
  4 g Epsom salts (skip if using Cal-Mg supplement)
  pH adjust to 5.8
  EC ~1.5–1.8

Apply 2 gal per 1 gal coco, in 2 stages, soak 6+ hr, drain.
```

### pH/EC Card

| Reading | Coco target | Hard limit |
|---|---|---|
| Input pH | 5.8 – 6.0 | 5.5 – 6.3 |
| Runoff pH | 5.6 – 6.3 | < 5.4 or > 6.5 = problem |
| Input EC veg | 1.0 – 1.8 | per stage |
| Input EC flower | 1.6 – 2.4 | per nutrient line |
| Runoff EC vs input | Within 0.5 | > 1.0 above = leach |

### Fertigation Frequency Reference

| Plant stage | Events per day (mature plant in 3–5 gal coco) |
|---|---|
| Seedling | 1 |
| Veg | 2 – 3 |
| Flower stretch | 2 – 4 |
| Mid flower | 3 – 5 |
| Late flower | 3 – 5 |

### VWC Targets

| State | VWC % |
|---|---|
| Post-fertigation peak | 65 – 75 |
| Vegetative dryback (trough) | 60 – 70 |
| Generative dryback (trough) | 45 – 55 |
| Stress threshold | < 40 |

### Cal-Mg Dose by Water Source

| Water source | Cal-Mg dose |
|---|---|
| RO / distilled | 1.5 – 2.0 ml/L |
| Soft tap (Ca + Mg < 60 ppm) | 1.0 ml/L |
| Medium tap (Ca + Mg 60–120 ppm) | 0.5 ml/L |
| Hard tap (Ca + Mg > 120 ppm) | Often skip — verify with feed line first |

### Common Problem → First Fix

| Problem | First check |
|---|---|
| Interveinal yellowing on lower leaves | Mg — verify Cal-Mg dose + pH |
| Twisted distorted new growth | Ca — verify buffering + Cal-Mg + transpiration |
| Pale interveinal new growth | Fe — pH drift above 6.3 |
| Tip burn | Salt buildup OR EC too high — leach + reduce input EC |
| Wilting between feeds | Channels OR underfertigation OR root issue |
| EC stacking | Insufficient runoff |
| Slow growth, look starved | Substrate pH off OR coco unbuffered |

## Sources

**Tier 1 — Peer-reviewed:**
- Caplan, D., Dixon, M., & Zheng, Y. — *Optimal rate of organic fertilizer during the vegetative-stage for cannabis grown in two coir-based substrates.* HortScience, 2017.
- Caplan, D., Dixon, M., & Zheng, Y. — *Optimal rate of organic fertilizer during the flowering-stage for cannabis grown in two coir-based substrates.* HortScience, 2017.
- Bilodeau, S. E., Wu, B. S., Rufyikiri, A. S., et al. — *An Update on Plant Photobiology and Implications for Cannabis Production.* Frontiers in Plant Science, 2019. (Includes substrate moisture studies.)

**Tier 2 — Manufacturer / industry technical:**
- CANNA Research — Coco Pro / Pro Plus technical bulletins, RHP certification.
- Char Coir — RHP certified coco product documentation.
- Athena — Pro feed schedule for coco, crop-steering EC targets.
- House & Garden — Cocos A+B feed protocol.
- Coco For Cannabis (cocoforcannabis.com) — extensive coco-specific protocols cross-confirmed against multiple manufacturer schedules.
- AROYA / Addium — crop steering documentation, VWC and dryback science.
- Growlink — irrigation phase documentation.
- Botanicare — Cal-Mg + Coco line technical sheets.
- Shogun Fertilisers — coco-specific feed schedules.
- RHP (Royal Horticultural Product) standard documentation.

**Tier 3 — Master growers / educators:**
- Mr. Canucks Grow — practical coco fertigation tutorials.
- DeBacco University (YouTube) — coco horticulture lectures.
- Jeremy Silva (BAS / no-till) — coco vs living-soil comparison material.

## Cross-References

- Soil cultivation (different mental model entirely) → `04-medium-soil.md`
- Pure hydroponic systems (DWC, RDWC, NFT) → `04-medium-hydro.md`
- Living-soil cultivation → `04-medium-living-soil.md`
- RO water requirement, alkalinity handling → `05-water-quality.md`
- Coco-specific feed schedules (Athena Pro, Canna A+B, Jacks) → `06-nutrients-synthetic.md`
- Cal/Mg/Fe deficiency patterns (mostly pH-driven in coco) → `07-deficiencies.md`
- VPD targets (low transpiration → Ca def even with correct feed) → `02-environment.md`
- Slurry substrate pH test method → `04-medium-soil.md`
- Salt-creep flushing protocol details → `06-nutrients-synthetic.md`
- Pythium root rot in over-saturated coco → `09-disease.md`
- Crop steering for flower-stage cannabinoid maximization → `12-flowering.md`
