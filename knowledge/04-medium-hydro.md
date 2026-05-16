# 04 — Medium: Hydroponics

True hydroponic cannabis cultivation — DWC, RDWC, NFT, ebb & flow, aeroponics, and the operational discipline they all share. Hydro has **zero substrate buffer**: every reading IS the root environment. Recovery from mistakes is hours, not days. Reward is faster growth and bigger plants; the cost is daily attention and zero tolerance for negligence. Cross-reference with `04-medium-soil.md` and `04-medium-coco.md` (the contrast — mediums with buffer), `04-medium-living-soil.md` (opposite end of philosophy), `05-water-quality.md` (RO is mandatory; chlorinated tap kills roots), `06-nutrients-synthetic.md` (Jacks 321, GH Trio, Athena Pro hydroponic schedules), `07-deficiencies.md` (manifests in hours not days), `09-disease.md` (pythium / root rot is the #1 hydro killer).

## How to Use This File

Diagnostic order for any hydro problem:

1. **Roots first** — visual + smell. White and clean = continue. Brown, slimy, smelly = stop everything, diagnose pythium
2. **Reservoir temperature** — above 22°C is a yellow flag, above 24°C a red flag
3. **DO (dissolved oxygen)** — air pump function, airline integrity, water surface agitation
4. **pH** — drift up daily is normal; sudden swings = problem
5. **EC** — drift up = water uptake > nute uptake; drift down = nute uptake > water uptake
6. **System-specific failure modes** — match symptoms to system type's known issues

## Core Concepts

| Concept | What it means | Why it matters |
|---|---|---|
| **Hydro = zero substrate buffer** | The reservoir is the root environment, period | Mistakes manifest in hours, not days; vigilance required |
| **Root health is the master variable** | Brown slimy roots = run-ender. Healthy white roots = everything else can be fixed | Daily root inspection in DWC/RDWC; visual access matters |
| **DO is as important as nutrients** | Roots need oxygen for respiration; low DO = root death + pythium opening | Air pump failure kills runs in 2–4 hours, especially during lights-off |
| **Reservoir is a chemistry beaker** | Daily-attention required: pH, EC, temp, DO | Hydro is the wrong choice for "set and forget" growers |
| **Recovery from mistakes is hours** | A pH crash visible at 8am can save the plants if caught by 10am | Daily monitoring is mandatory, not aspirational |
| **System type determines everything else** | DWC, NFT, ebb&flow, aero have completely different failure modes and operating disciplines | Don't apply DWC advice to NFT or vice versa |
| **Single-point-of-failure risk** | Pump dies → roots die. Power outage → emergency. Airline kinks → suffocation | Build redundancy: backup air pump, UPS, alarm sensors |
| **Beneficial microbes OR H₂O₂ — never both** | Two opposing philosophies for keeping pythium out; mixing them cancels both | Pick one approach and commit |

## The Hydroponic Systems

### Deep Water Culture (DWC)

**How it works:** plant suspended in a net pot at the top of a 5-gal bucket; roots dangle into 4 gal of nutrient solution; air stone + air pump bubble the solution continuously.

**Plant scale:** 1 plant per 5-gal bucket; suitable for monster plants (huge root mass + root real estate = fast growth).

**Capital cost:** $50–100 per plant (bucket + pump + stone + lid + net pot + reservoir control hardware).

**Complexity:** moderate to high. Beginner-friendly conceptually, but daily attention required.

**Failure modes:**
- Air pump failure → DO crash → suffocation in 2–4 hr (lights-off particularly dangerous; nobody watching)
- Reservoir temp creep → pythium → root rot
- pH drift unmonitored → lockout
- Light leaks into bucket → algae → DO competition + bad smell

**When DWC makes sense:** single-plant tents wanting maximum-yield monster plants; growers wanting to learn hydro fundamentals.

### Recirculating DWC (RDWC)

**How it works:** multiple DWC buckets connected at the bottom via a manifold; central reservoir or one designated bucket holds the bulk volume; pump circulates solution through all buckets continuously. All buckets equilibrate to the same chemistry — measure once, all plants experience the same.

**Plant scale:** 4–32+ plants per system; commercial-friendly.

**Capital cost:** $200–800 for a 4-plant home system; $5,000+ for commercial 16-plant setups (Current Culture H₂O is the industry leader).

**Complexity:** higher than DWC due to plumbing; lower than DWC operationally because monitoring one reservoir covers all plants.

**Failure modes:**
- Manifold leaks (every fitting is a potential failure point — silicone everything)
- Recirc pump failure → still oxygenated by air pumps but no nutrient distribution → lockout patches
- Same DO/temp/pH issues as DWC, scaled

**When RDWC makes sense:** multi-plant home systems, growers comfortable with plumbing, and users who can monitor water temperature, DO, pH, and leaks consistently.

### Nutrient Film Technique (NFT)

**How it works:** plants in net pots above sloped channels (PVC pipe with cutouts); a thin film of solution flows continuously down the slope, contacting roots; drains back to a central reservoir; pump returns it to the top.

**Plant scale:** small-to-medium plants. Cannabis works but root mass can clog channels; aggressive root pruning or training required.

**Capital cost:** $300–1500 for a home system; large-system cost varies widely.

**Complexity:** moderate. Plumbing-heavy.

**Failure modes:**
- **Pump failure → roots dry out in 30–60 min** (the fastest kill mode of any hydro system; thin film leaves no water reserve)
- Channels clog with root mass, water diverts past roots, sections die
- Algae growth in light-exposed channels
- Slope wrong → solution pools or runs too fast

**When NFT makes sense:** lettuce / leafy greens / herbs (it's the lettuce industry standard). For cannabis, less common; works but offers no advantage over DWC unless space is the limit.

### Ebb & Flow (Flood and Drain)

**How it works:** plants in pots filled with hydroton (clay pebbles) or rockwool; pots sit in a tray; pump floods the tray with nutrient solution at intervals (typically 4–6 times daily for 15 min); solution drains back to reservoir.

**Plant scale:** 2–24+ plants per tray; flexible.

**Capital cost:** $200–600 for a home system (tray + pump + reservoir + timer + net pots + media).

**Complexity:** low to moderate. Beginner-friendly compared to DWC because pump failures don't kill plants for 12+ hours (media holds water).

**Failure modes:**
- Pump or timer failure → media dries out gradually (slow death, more recoverable than DWC)
- Reservoir pH/EC drift goes unmonitored because plants tolerate it longer
- Hydroton dust clogs pumps if not pre-rinsed
- Salt buildup in media over weeks (rockwool especially)

**When ebb & flow makes sense:** beginners wanting hydro simplicity, growers wanting modular scale, climates with frequent power blips.

### Aeroponics

**How it works:** plants suspended in a sealed chamber; roots hang in air; nutrient solution is **misted onto roots at intervals** — every 30–60 sec for low-pressure aero (LPA), every 1–5 min for high-pressure aero (HPA). Roots in air = maximum DO; mist = precise nutrient delivery.

**Plant scale:** small to medium; commercial cloning operations heavy users.

**Capital cost:** $500–3,000+ for a home system; $10,000+ for serious HPA.

**Complexity:** highest of any hydro. HPA requires accumulator tanks, pressure regulators, micron-rated nozzles, and very clean nutrient solution (clogs kill).

**Failure modes:**
- Nozzle clog → that root section dies in hours
- Pump failure → roots dry in 15–30 min (faster than NFT)
- Solution chemistry drift while you're not watching
- Biofilm in nozzles requires monthly disassembly + clean

**When aero makes sense:** experienced growers chasing maximum growth rate; commercial cloning (Aero-Cloners are the industry standard for clone production); R&D operations.

### Drain-to-Waste (DTW)

**How it works:** rockwool, hydroton, or coco-perlite in pots; timed drip emitters deliver nutrient solution at scheduled intervals; runoff drains to waste (not recirculated). Often called "hydro" but is technically media-based fertigation. Closer to high-frequency coco than to true recirculating hydro.

**Plant scale:** any.

**Capital cost:** moderate. Drip lines + reservoir + timer + media + pots.

**Complexity:** moderate. Easier than recirculating because solution chemistry doesn't drift in the reservoir (you mix fresh and use it).

**Failure modes:**
- Dripper clog (single emitter blocked → that plant starves)
- Salt buildup in media over weeks if runoff insufficient
- Reservoir pH/EC stable since not recirculating, but media accumulates salts

**When DTW makes sense:** commercial production at scale (rockwool + drip is industry standard for greenhouses); growers wanting hydro yields without recirc complexity.

### Top-Feed DWC ("Bubbleponics")

**How it works:** DWC bucket + a top-drip line that feeds the seedling/young plant from above for the first 1–3 weeks until roots reach the reservoir. Then drip can be turned off.

**Plant scale:** same as DWC.

**Why it exists:** seedlings in DWC can't reach the reservoir water level for the first 1–2 weeks. Top-feed bridges that gap, cuts establishment time roughly in half.

**Failure modes:** all DWC failures plus drip clogs.

### Kratky Method (Passive Hydro)

**How it works:** plant in a net pot above a sealed reservoir; no pump, no air stones; as roots grow down, the water level drops, leaving an **air gap** that supplies oxygen to the upper roots while lower roots stay submerged in solution. No power required.

**Plant scale:** small plants only — herbs, lettuce, autoflowers in 5-gal Kratky setups.

**Capital cost:** ~$10 per plant.

**Complexity:** very low.

**Failure modes:**
- Reservoir runs dry before plant finishes → death
- No DO management → larger plants outgrow Kratky's passive oxygenation
- Pythium risk in warm passive water

**When Kratky makes sense:** small autoflower experiments; off-grid / no-power setups; teaching hydroponic principles. **Not viable for full-cycle photoperiod cannabis** — the plant runs out of water and DO before harvest.

## Reservoir Management

### Volume per Plant

| System | Reservoir vol per plant |
|---|---|
| DWC | 3–4 gal (in 5-gal bucket with 1 gal headroom) |
| RDWC | 5+ gal effective per plant via shared res |
| NFT | 0.5–1 gal in central res (channel fluid is minimal) |
| Ebb & Flow | 1–2 gal per plant in shared res |
| Aero | 1–2 gal per plant in shared res |
| Drain-to-waste | Reservoir volume isn't shared with plants — refill as used |

**Rule:** more reservoir volume = more chemistry stability = slower drift. Big res is forgiving. Small res requires more frequent intervention.

### Top-Up vs Full Change

**Top-up** = add water (or low-EC water + Cal-Mg) to compensate for transpiration. Maintains volume; doesn't reset chemistry.

**Full change** = drain reservoir, rinse, refill with fresh nutrient solution. Resets chemistry.

| System / scenario | Recommended cadence |
|---|---|
| DWC, 5-gal single bucket | Full change weekly OR top-up + full every 10–14 days |
| RDWC, central res | Full change every 7–14 days |
| NFT | Full change every 7–10 days |
| Ebb & Flow | Full change every 7–14 days |
| Drain-to-waste | Mix fresh per session — no res change concept |

**When to force a full change regardless of schedule:**
- pH unstable (won't hold target) → likely depleted buffers
- EC creep above input (salt accumulation, esp. in hot rooms with heavy transpiration)
- Roots show any sign of distress
- Color or smell off (cloudy, sour, "earthy" beyond normal)

### Top-Up Composition

When transpiration drops the reservoir, **what** you add depends on what drifted:

| EC drift | Meaning | What to add |
|---|---|---|
| EC unchanged, water down | Plant absorbing water + nutes proportionally — rare in hydro | Top up with full-strength solution at target EC |
| EC up, water down | Plant absorbing water faster than nutes — common | Top up with **plain pH'd water + Cal-Mg** to dilute back to target |
| EC down, water down | Plant absorbing nutes faster than water — uncommon, indicates very dialed setup | Top up with **above-target EC solution** |

**Math for dilution top-up:**
```
To bring (V_current × EC_current) to target EC by adding plain water:
V_water = V_current × (EC_current / EC_target − 1)
```

### Reservoir Hygiene

Biofilm accumulates on every wet surface. Between full changes:
- Wipe inside of bucket / res with clean cloth (no soap residue)
- Rinse air stones; replace every 30–60 days
- Keep reservoir dark — light = algae
- Lid seals matter (light leak prevention; pest exclusion)

## Dissolved Oxygen (DO)

### Why DO Matters
Roots respire. They consume oxygen and produce CO₂ in their root metabolism. **Without adequate DO, roots suffocate** — and the resulting weakened root tissue is the open door pythium needs.

### DO Targets

Saturated DO in pure water at 20°C = ~9 ppm. Target ranges:

| DO level (ppm at 20°C) | Status |
|---|---|
| 8 – 9+ ppm | Excellent — saturated, healthy roots |
| 6 – 8 ppm | Acceptable — most well-aerated DWC operates here |
| 4 – 6 ppm | Marginal — pythium risk increases |
| < 4 ppm | Dangerous — roots suffocate, pythium thrives |

(Tier 1 — multiple DO/root-zone studies; Tier 2 — North Slope Chillers, Current Culture, RDWC manufacturers all converge on these ranges.)

### Air Pump Sizing

Rule of thumb: **at least 1 watt of air pump per gallon of reservoir.** Bigger is fine; under-sizing is deadly.

For a 4-plant RDWC at 20 gal total: minimum 20W air pump (e.g., EcoPlus Commercial Air 1, Active Aqua Air Pump 4-outlet at 6W per outlet × 4). Most hydro veterans **double** this rule for hot rooms or summer operations.

### Aeration Methods

| Method | Pros | Cons |
|---|---|---|
| **Air pump + stones (lava-rock or ceramic)** | Cheap, simple, redundant | Pump failure = total DO loss; stones biofoul |
| **Air pump + diffusers** | Finer bubbles → better DO transfer | Same pump-failure risk |
| **Mazzei venturi** | No moving parts (pumps the water itself); high transfer rate | Requires pressure pump that's usually already in system |
| **Surface agitation** (waterfall, spray bar) | Continuous DO transfer; doesn't require air pump | Splash/water-noise issues |
| **Pure O₂ injection** | Maximum DO (commercial only) | Capital + safety + cost |
| **Hydrogen peroxide** (35% at 1–2 ml/L) | Releases O₂ as it breaks down; also kills pythium | Kills beneficials; must be re-applied every 12–48 hr |

**Best home setup:** large air pump + 2 air stones + waterfall return on RDWC (multiple redundant DO sources).

### DO Drops with Heat

DO saturation declines with rising water temp:
- 16°C: ~10 ppm saturated
- 20°C: ~9 ppm saturated
- 24°C: ~8.4 ppm saturated
- 28°C: ~7.8 ppm saturated
- 30°C: ~7.5 ppm saturated

The numbers look modest but **plant root oxygen demand goes UP with heat** while supply goes DOWN. The combination is why warm reservoirs kill hydro runs.

## Reservoir Temperature

### Targets

| Temp range | Status |
|---|---|
| 15 – 18°C (59 – 64°F) | Cold, plants slow, pythium suppressed; sometimes too cold for nute uptake |
| **18 – 22°C (64 – 72°F)** | **Optimal — DO holds, pythium suppressed, root metabolism strong** |
| 22 – 24°C (72 – 75°F) | Acceptable, watch DO carefully |
| 24 – 26°C (75 – 79°F) | Warning zone — pythium activates above 23°C |
| > 26°C (>79°F) | Pythium proliferation; runs are at risk |

(Tier 1/2 — pythium temperature thresholds well-documented; multiple sources agree.)

### Cooling Methods

| Method | Effectiveness | Cost |
|---|---|---|
| **Water chiller** (1/10 HP for home; 1/4–1 HP for commercial) | Excellent — gold standard | $200–1500+ |
| **Reservoir below grade** (basement, cellar) | Free — uses earth as heat sink | Real estate dependent |
| **Reservoir insulated** | Reduces ambient impact | $20–50 in foam panels |
| **Frozen water bottles in res** | Band-aid, drops temp 2–3°C for hours | Free; labor every 6–12 hr |
| **Lights-off to cool ambient** | Reduces room heat dump | Already happening; not enough alone in hot climates |
| **Pre-chill nutrient water** | Helpful when topping up | Refrigerator hours of lead time |

In any climate where summer ambient exceeds 28°C (82°F), a chiller is a near-mandatory hydro purchase. The cost is recovered by avoiding one lost run.

## pH Management in Hydro

### Range
- **Acceptable:** 5.5 – 6.3
- **Optimal target:** 5.8
- **Below 5.4:** root acid damage; Mg, Ca, Mo locked
- **Above 6.3:** Fe, Mn, Zn, B locked

Calibrate pH meter monthly. Replace probe every 12–18 months. Cheap pH meters drift fast — buy a Bluelab, Apera, or similar.

### Daily Drift

Cannabis in active growth absorbs nitrate (NO₃⁻) and other anions, releasing OH⁻ as a byproduct. This **drives reservoir pH UP** by 0.1–0.5 per day. Daily checks are not optional.

```
Day 1: pH set to 5.8
Day 2: pH 5.95
Day 3: pH 6.1
Day 4: pH 6.25 — adjust back down to 5.8
```

This drift pattern is healthy. Sudden swings (pH crashes downward, or jumps up faster than 0.5/day) signal problems.

### pH Down Chemistry

| Acid | Pros | Cons |
|---|---|---|
| **Phosphoric** (typical commercial pH-Down) | Stable, predictable, inexpensive | Adds P to solution — can stack over time in long runs |
| **Nitric** | Adds N (which depletes faster than P) | More dangerous to handle (concentrated nitric is corrosive) |
| **Sulfuric** | Adds S | Hazardous to handle |
| **Citric acid** | Organic, biodegradable | Microbes consume it within hours; pH bounces back; not for stable hydro |
| **Acetic acid (vinegar)** | Cheap, food-safe | Same biodegradation issue as citric |

For most hydro: phosphoric pH-Down is the default. Switch to nitric for high-N feeds in long flower runs if P stacking becomes an issue.

### pH Up
Potassium hydroxide (KOH) in commercial pH-Up products. Adds K (rarely a problem in flower; can be in late-flower if K is already high).

## EC/PPM Management

### Daily EC Check Required

Like pH, EC drifts in the reservoir as plants pull water and nutrients at different rates.

### Drift Interpretation

| EC trend | Meaning | Action |
|---|---|---|
| EC up, water down | Plant absorbing water faster than nutes — most common in hot rooms | Add plain pH'd water + Cal-Mg to bring EC back to target |
| EC down, water down | Plant absorbing nutes faster than water — uncommon, signal of well-dialed setup | Add target-EC solution to top up |
| EC stable, water down | Plant absorbing in proportion — rare | Add target-EC solution |
| EC creeps up over weeks despite top-ups | Salt accumulation — full change overdue | Drain, rinse res, fresh batch |

### Top-Up Math (Practical)

To bring 5 gal of EC 2.4 solution back to target EC 2.0 by adding water:
```
V_water = 5 × (2.4 / 2.0 − 1) = 5 × 0.2 = 1 gal water added
```

Don't forget Cal-Mg in the top-up water if running RO base.

## Reservoir Change Schedule

### The Default
**Full change every 7 days.** Safest, simplest, beginner-friendly.

### The Rolling Top-Up Approach
For dialed-in growers with stable readings:
- Daily top-up with chemistry-corrected water
- Full change every 14–21 days

This works if and only if:
- pH and EC are stable day-to-day
- Roots remain white
- No funky smells
- DO consistent

If any of those slip, default back to weekly changes until stable again.

### When to Force a Change Regardless

- pH won't hold target (drifting wildly within hours of correction)
- EC creep > 1.0 above input despite top-ups
- Visible root issue (any browning)
- Smell sour, sulfurous, or chemically "off"
- Room temperature spike that warmed the reservoir
- Any equipment incident (pump failure, power outage > 30 min)

## Beneficial Microbes vs H₂O₂ — The Philosophy Split

Two opposing approaches to keeping pythium at bay. **Pick one and commit. Mixing them cancels both.**

### The Beneficial Route

Inoculate the reservoir with **plant-friendly bacteria and fungi** that outcompete pythium for resources, secrete antimicrobial compounds, and protect roots.

Common products:
- **Hydroguard** (Botanicare) — Bacillus amyloliquefaciens primarily, plus B. subtilis, Paenibacillus polymyxa, B. circulans. Hydroponic-formulated, works at the cool reservoir temps that block other Bacillus products
- **Great White** — mycorrhizae blend (less impactful in pure DWC since mycos need media to colonize, but useful in ebb & flow with hydroton)
- **RAW Microbes Bloom / Grow** — soil-style inoculant; works in hydro-with-media
- **Mammoth P** — phosphorus-mobilizing bacteria

**Pros:** ongoing protection (bacteria multiply once established); no chlorine-like sterility; works with organic supplements
**Cons:** slower acting (3–7 days to colonize); incompatible with H₂O₂, chlorine, ZeroTol, copper, most sterilants

### The Sterile Route

Keep the reservoir **biologically inert** through chemical sterilants that kill pythium spores before they can colonize.

Common products:
- **Hydrogen peroxide (H₂O₂)** — 35% food-grade, 1–2 ml per gallon every 24–48 hr. Adds DO as it breaks down to water and oxygen
- **ZeroTol / OxiDate** — peroxyacetic acid commercial sterilant
- **Dilute bleach** (highly controlled) — 0.5 ml of 8% sodium hypochlorite per gallon as last-resort sterilization

**Pros:** fast-acting; predictable; cheap; bonus DO boost from H₂O₂
**Cons:** kills beneficials; requires re-application every 12–48 hr; higher concentrations damage roots

### Why You Can't Mix Them
H₂O₂ kills the Bacillus species in Hydroguard within minutes. Adding both = wasted Hydroguard cost and untrained microbiome.

If you commit to beneficial: **never** add H₂O₂ unless you've decided to kill the microbes and reset to sterile.
If you commit to sterile: **never** add Hydroguard or microbe products mid-cycle.

### Choosing
- **Beginner DWC, hot room:** sterile (H₂O₂) — easier to manage; failure mode is "needs more peroxide" not "is the culture alive?"
- **RDWC with chiller, mature setup:** beneficial — once established, it's set-and-forget protection
- **Aeroponics / NFT:** beneficial typically — biofilms in lines and nozzles benefit from healthy microbiome, sterile route requires aggressive cleaning
- **Drain-to-waste rockwool/hydroton:** either works; beneficial often included in feed lines

## System-Specific Operating Notes

### DWC / RDWC Daily Checks
1. Visual root check (lift lid, look at root tone) — white = healthy, brown = panic
2. Smell check — neutral/slightly sweet = healthy, sour/chemical/sulfurous = problem
3. pH and EC reading
4. Reservoir temperature
5. Water level (top-up if needed)
6. Air pump function (look for bubbles, listen for pump motor)
7. All buckets visually equilibrated (water levels even in RDWC)

### NFT Daily Checks
1. Pump function (cannot fail — even short interruption = drying roots)
2. Slope alignment (no pooling, no bypass channels)
3. Channels free of biofilm/blockage at outlets
4. Reservoir pH/EC/temp
5. Roots in channels white and healthy

### Ebb & Flow Daily Checks
1. Last flood cycle ran (timer + pump verification)
2. Reservoir levels and chemistry
3. Media surface NOT covered in salt crust (indicator of insufficient runoff)
4. Drainage path clear

### Aero Daily Checks
1. Nozzle output uniform (clogged nozzle = root section dies)
2. Pump pressure normal (HPA: psi reading)
3. Mist intervals firing on schedule
4. Reservoir chemistry
5. Nothing biofilming in lines

## Hydro-Specific Issues

### Pythium / Root Rot (#1 hydro killer)
**Symptoms:** brown-to-black slimy roots, foul smell (rotten, sulfurous, "swamp"), wilting top growth despite plenty of water, sudden plant decline.

**Causes:**
- Reservoir > 23°C
- DO < 5 ppm
- Light leak into reservoir feeding algae → DO competition
- Contaminated water source (well water, untreated tap)
- Tools / hands transferring spores between systems

**Recovery (if caught early):**
1. Drain reservoir completely
2. Rinse all surfaces — buckets, lines, air stones — with H₂O₂ at 5 ml/L
3. Trim dead/black root tissue with sterile scissors
4. Refill with fresh nutrient solution at full strength + 1 ml/L H₂O₂
5. Lower reservoir temp to 18–20°C immediately (chiller, ice bottles)
6. Maintain H₂O₂ daily for 3–5 days
7. Watch for fresh white root tips emerging within 5–7 days

**Severe cases:** may require complete system breakdown, sterilization, restart from scratch.

### Brown Roots (Other Causes)
- **pH crash below 5.0** — root acid burn (brown but firm, not slimy)
- **Chlorinated tap water** — chlorine kills root tips on contact (brown tips, otherwise healthy)
- **Mineral burn** (EC too high) — brown tips with hardened tissue
- **Old reservoir** (3+ weeks no change, no microbes, no peroxide) — gradual browning

### Air Pump Failure During Lights-Off
The deadliest scenario. Lights-off + warm res + no airflow = anaerobic in 2–4 hours; pythium colonization within 12 hr.

**Mitigation:**
- Backup air pump always plugged in (parallel to primary)
- Air pump on UPS for power-blip protection
- Audible water alarm or DO sensor with alert (Bluelab Guardian, Pulse Pro hydro sensor)

### Power Failure
Pumps stop. Reservoir warms toward ambient. DO drops.

**Protocol:**
- < 2 hr outage: usually OK; restart pumps, verify DO recovers
- 2–6 hr outage: check roots within 12 hr; preventive H₂O₂ dose
- > 6 hr outage: assume pythium exposure; full sanitation cycle, H₂O₂ reset, monitor for symptoms

UPS for air pumps + recirc pump is the cheap insurance ($100 covers 4-hour outages for a small RDWC).

### Algae
Green slime on reservoir walls, in lines, on lid undersides.

**Cause:** light leak.

**Fix:** opaque all surfaces (black tape, paint, opaque buckets), then drain + clean + refill.

### Mineral Precipitation When Mixing Concentrates
Calcium nitrate + phosphates/sulfates in concentrated form precipitate (calcium phosphate, calcium sulfate). Result: cloudy white solids in the bucket.

**Prevention:** mix base nutes in water FIRST (separate parts if multi-part), let dissolve, then add Cal-Mg. Never mix concentrates directly.

## Confusion / Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| Pythium | Brown roots from chlorinated tap | Slime + smell = pythium; firm brown tips only = chlorine |
| Pythium | pH crash root burn | Trace recent pH log; if pH crashed below 5.0 in last 24h, that's the cause |
| Slow growth | Low DO | Check air pump function and water temp before assuming nute/light issue |
| "EC went up, plant needs more nutes" | EC went up because plant absorbed water faster than nutes | Add plain water + Cal-Mg, NOT more nutes |
| pH won't hold target | Buffers depleted (old res); OR wrong acid (citric biodegrades fast); OR active root issue dumping organics into solution | Force full change; switch to phosphoric pH-Down |
| Air pump runs but no bubbles | Air stone biofouled or airline kinked | Replace stone; check airline integrity |
| "I added Hydroguard AND H₂O₂ for safety" | Just killed both | Pick one approach; if mixing happened, drain + restart |
| Wilting despite full reservoir | Root tissue dying (pythium) — plant can't uptake water | Inspect roots immediately |
| Lights-off pH crashes | Reservoir biology going anaerobic + organic supplements fermenting | Check DO; consider fewer organic additives in flower res |
| Plants wilt 1–2 hr after lights on, recover | Normal — peak transpiration outpaces uptake briefly; not a problem unless severe | Watch but don't panic-react |
| Roots look slimy but plants healthy | Beneficial biofilm (Hydroguard establishment) — different from pythium slime | Color: tan/sandy = beneficial; brown/black = bad |

## Quick Reference

### System Comparison Matrix

| System | Capital | Complexity | Beginner-friendly | Failure speed | Cannabis fit |
|---|---|---|---|---|---|
| DWC | $ | Med | Yes (with vigilance) | 2–4 hr (DO crash) | Excellent |
| RDWC | $$$ | High | No | 2–6 hr | Excellent (production) |
| NFT | $$ | High | No | 30–60 min | Marginal |
| Ebb & Flow | $$ | Low | Yes | 12+ hr | Good |
| Aero (HPA) | $$$$ | Very high | No | 15–30 min | Niche |
| DTW | $$ | Med | Yes | Slow (media buffer) | Excellent (commercial) |
| Kratky | $ | Very low | Yes | 1–2 weeks | Autoflower only |

### Reservoir Targets Card

| Reading | Target | Hard limit |
|---|---|---|
| pH | 5.8 | 5.5 – 6.3 |
| EC veg | 1.2 – 1.6 | per stage |
| EC flower | 1.6 – 2.2 | per nutrient line |
| Reservoir temp | 18 – 22°C | < 24°C absolute max |
| DO | 8+ ppm | > 6 ppm minimum |

### Daily Hydro Checklist
1. Roots — visual + smell
2. Reservoir temp
3. DO indicator (bubbling pattern, sensor reading)
4. pH (adjust if >0.3 from target)
5. EC (top-up logic per drift direction)
6. Water level (top-up volume)
7. Pump and airline function
8. Lights, environment per `02-environment.md` and `03-lighting.md`

### Beneficial vs Sterile Decision

| Setup | Default route |
|---|---|
| Beginner DWC, hot room | Sterile (H₂O₂) |
| Mature RDWC with chiller | Beneficial (Hydroguard) |
| Aero / HPA | Beneficial |
| NFT | Beneficial |
| DTW with media | Either |

### Pythium Recovery Protocol (One-Liner)
Drain → sanitize all surfaces → trim dead roots → refill at full EC + H₂O₂ 1 ml/L → drop res temp to 18–20°C → daily H₂O₂ for 3–5 days → watch for fresh white root tips.

## Sources

**Tier 1 — Peer-reviewed:**
- Caplan, D., Stemeroff, J., Dixon, M., & Zheng, Y. — *Vegetative propagation of cannabis by stem cuttings: effects of leaf number, cutting position, rooting hormone, and leaf tip removal.* Canadian Journal of Plant Science, 2018. (Hydroponic propagation methods.)
- Punja, Z. K., & Rodriguez, G. — *Fusarium and Pythium species infecting roots of hydroponically grown marijuana (Cannabis sativa L.) plants.* Canadian Journal of Plant Pathology, 2018.
- Punja, Z. K. — *Pathogens and molds affecting production and quality of Cannabis sativa L.* Frontiers in Plant Science, 2018.
- Bugbee, B. — root zone oxygen, hydroponic productivity research at Utah State.
- Bektas, A., et al. — *Hop Latent Viroid: A Hidden Threat to the Cannabis Industry* (clean-water and clean-clone discipline applies to hydro).

**Tier 2 — Manufacturer / industry technical:**
- Current Culture H₂O — RDWC industry leader; published grow-tip documentation.
- Botanicare — Hydroguard product literature, formulation data.
- General Hydroponics — Flora Series + hydroponic system documentation.
- Athena — Pro hydroponic feed schedule.
- Bluelab — pH/EC meter calibration documentation.
- North Slope Chillers — water chiller specs and root-rot prevention literature.
- Dutch Hydroponics — RDWC and NFT systems documentation.
- AROYA / Addium — substrate sensor data.
- Aero-Cloner — aeroponic propagation specs.

**Tier 3 — Master growers / educators:**
- Heisenberg DWC method (community-validated; rollitup/grasscity forum-derived RDWC stabilization protocol).
- Mr. Canucks Grow — RDWC tutorials.
- DeBacco University (YouTube) — hydroponic horticulture lectures.
- Cervantes, J. — *Cannabis Encyclopedia* hydroponic chapters.

## Cross-References

- Soil cultivation (the buffered medium contrast) → `04-medium-soil.md`
- Coco cultivation (hydroponic-with-substrate cousin) → `04-medium-coco.md`
- Living soil (opposite philosophy) → `04-medium-living-soil.md`
- RO water requirement and chlorine handling → `05-water-quality.md`
- Hydro feed schedules (Jacks 321, GH Trio, Athena Pro) → `06-nutrients-synthetic.md`
- Hydro deficiency dynamics (faster manifestation) → `07-deficiencies.md`
- Pythium / Fusarium identification and management → `09-disease.md`
- VPD and transpiration coupling to nutrient uptake → `02-environment.md`
- Crop steering with substrate sensors → `04-medium-coco.md`
- Cloning in aeroponic cloners → `11-propagation.md`
