# 03 — Lighting

PPFD, DLI, spectrum, photoperiod, fixture selection, hang-height math, and photoinhibition. Light is the prime input — once environment and nutrients are in spec, lighting sets the yield ceiling. Cross-reference with `02-environment.md` (CO₂ × PPFD coupling, leaf-temp interaction), `00-fundamentals.md` (photosynthesis, phytochrome biology, photoperiod), `12-flowering.md` (photoperiod transitions and stretch management), `06-nutrients-synthetic.md` (light intensity scales nutrient demand), `13-harvest.md` (finishing-stage light protocols).

## How to Use This File

When dialing or diagnosing lighting, work in this order:

1. **PPFD first** — what's actually hitting the canopy in µmol/m²/s. Manufacturer claims are not measurements.
2. **DLI second** — daily integration matters more than peak intensity; a long day at modest PPFD can equal a short day at high PPFD.
3. **Spectrum third** — secondary lever; intensity dominates spectrum effects in most decisions.
4. **Hang height fourth** — controls uniformity and burn risk; coupled with dimmer setting.
5. **Match to environment + CO₂** — high PPFD without matching CO₂ + temp wastes energy and stresses plants.

## Core Concepts

| Concept | What it means | Why it matters |
|---|---|---|
| **PPFD ≠ lumens ≠ lux** | Lumens and lux measure light *as the human eye sees it* (peaks at green). Plants use the whole 400–700 nm PAR band. | A "10,000 lumen" rating is meaningless for plants — demand µmol/s (PPF) or µmol/m²/s (PPFD) |
| **DLI is the right comparison metric** | DLI = PPFD × seconds × 10⁻⁶, in mol/m²/day. Two rooms with same DLI deliver similar growth even at different PPFD/photoperiod combos | Veg at 18/6 with 600 PPFD ≈ flower at 12/12 with 900 PPFD (~39 mol/m²/day) |
| **Intensity dominates spectrum** | Within reasonable broad-spectrum ranges, doubling PPFD doubles yield trajectory; spectrum tweaks add 5–15% | Don't pay 2× for "perfect spectrum" if you could buy more PPFD per dollar instead |
| **Light is the yield ceiling** (with env + nutes aligned) | Once VPD, CO₂, temp, and feed are in spec, more light = more yield up to ~1800 µmol/m²/s | Genetics caps potency/effect; light caps yield |
| **µmol/J is fixture efficiency** | Photons delivered per electrical joule consumed. Top LEDs hit 2.7–3.0 µmol/J; HPS ~1.7 µmol/J | Wattage alone misleads — a 600W fixture at 2.8 µmol/J outperforms a 1000W fixture at 1.7 µmol/J |
| **Manufacturer PPFD chart is a starting point, not gospel** | Real measured PPFD at canopy varies with hang height, room reflectivity, dimmer setting, fixture age | Buy or borrow a quantum sensor (or use Photone with the cosine corrector) — verify before trusting |

## PAR / PPFD / DLI / PPF / µmol/J — Definitions

| Term | Unit | Meaning | What it measures |
|---|---|---|---|
| **PAR** | nm range | Photosynthetically Active Radiation: 400–700 nm | The wavelength band plants use for photosynthesis |
| **PPF** | µmol/s | Photosynthetic Photon Flux | Total photons in PAR emitted per second by the fixture |
| **PPFD** | µmol/m²/s | Photosynthetic Photon Flux **Density** | Photons hitting one square meter per second AT THE CANOPY |
| **DLI** | mol/m²/day | Daily Light Integral | Total moles of photons delivered per square meter per day |
| **µmol/J (PPE)** | µmol/joule | Photosynthetic Photon Efficacy | How many photons the fixture produces per electrical joule consumed |
| **YPF** | µmol/s | Yield Photon Flux | PPF weighted by McCree relative quantum yield curve. Less commonly used now. |
| **Lumens / lux** | lm / lx | Luminous flux / illuminance | Light as seen by the human eye — peaks at ~555 nm. **Useless for plant work.** |

### Why µmol/J Beats "Watts"

A "1000W LED" rating tells you the electrical draw, not the photons delivered. The right comparison is **µmol/J at the fixture (not the chip)**:

| Fixture class | µmol/J typical | Notes |
|---|---|---|
| Top-tier broad-spectrum LED bar (Fluence SPYDR, Gavita 1700e LED, HLG 600 Rspec, Migro Aray) | 2.7 – 3.0 | Verified at fixture, not chip |
| Mid-tier LED quantum board | 2.2 – 2.6 | Common consumer / craft tier |
| Budget LED (no-name imports) | 1.8 – 2.2 | Often overstated on packaging |
| HPS double-ended (DE) | 1.9 – 2.1 | Best HPS class; e.g., Gavita Pro 1000 DE |
| HPS single-ended | 1.5 – 1.7 | Older fixtures, magnetic ballasts lower still |
| CMH / LEC 315W | 1.9 – 2.1 | Quality of spectrum often praised |
| T5 fluorescent | 0.7 – 0.9 | Propagation only; never for flower |
| Old LED COB (single chip-on-board) | 1.5 – 2.0 | Mostly superseded by bar/QB designs |

(Tier 1 — Bugbee USU testing for Fluence and others; Tier 2 — manufacturer published spec sheets, cross-confirmed.)

**Critical caveat:** efficacy at the chip vs. at the fixture differs by 10–50%. Driver losses, heat-derating, optical losses (lensing, diffusers), and high drive currents all reduce real-world output. Always quote and compare **fixture-level** efficacy.

## Spectrum

### The McCree Curve (Foundation)
The 1972 McCree action spectrum showed photosynthesis runs at high efficiency across most of PAR (400–700 nm), with peaks in red and blue. **Modern broad-spectrum white LEDs cover the curve adequately** — exotic spectrum claims rarely beat well-engineered white + supplemental red.

### Wavelength Effects Worth Knowing

| Wavelength band | Effect | Practical implication |
|---|---|---|
| **Blue (440–470 nm)** | Compactness, leaf morphology, chlorophyll synthesis, increases cannabinoid concentration (Magagnini et al. 2018, especially THC) | Higher blue % in veg → tighter internode spacing; lower blue % in flower → more stretch but slightly higher yield (PLOS One 2021) |
| **Green (500–600 nm)** | Penetrates deeper into canopy than red/blue (less absorbed at top); contributes to whole-canopy photosynthesis | Don't dismiss green — Bugbee research shows green photons are useful, not "wasted" |
| **Red (620–680 nm), peak 660 nm** | Drives phytochrome to active Pfr form; high quantum yield | Most efficient band per photon; supplemental red common in horticultural LEDs |
| **Far-red (700–760 nm), peak 730 nm** | Reverses Pfr → Pr; shade response (stretch promotion); Emerson effect when paired with red boosts photosynthesis; end-of-day applications can accelerate flowering signals | Low R:FR ratio = taller plants (Scientific Reports 2025); EOD far-red enables 13/11 schedules (see DLE section) |
| **UVA (315–400 nm)** | Modest effects on morphology and secondary metabolites; less defensive trigger than UVB | Often included in "full spectrum" LEDs |
| **UVB (280–315 nm)** | Defensive response — historically thought to boost trichome production / THC (Lydon et al. 1987). **Recent research disputes this** — Westmoreland & Bugbee 2022 (*Indoor grown cannabis yield increased proportionally with light intensity, but ultraviolet radiation did not affect yield or cannabinoid content*) found no THC or yield benefit from UV exposure | **Tier 1 conflict:** older studies (Lydon 1987 — Tier 1 historical) say yes; newer better-controlled studies (2022) say no. Default position: don't pay extra for UVB; if you have it, late-flower exposure can't hurt and might help on some genetics |

### The Practical Spectrum Reality

- **Modern broad-spectrum white LEDs** (3000K–4000K white + supplemental 660 nm red) cover what cannabis needs.
- **More blue in veg** = tighter structure (good for SCROG, indoor space limits).
- **Less blue in flower** = some yield bump, easier on plants (PLOS One 2021 — Cannabis lighting: Decreasing blue photon fraction increases yield).
- **Far-red supplementation** is the most-researched legitimate spectrum lever — Emerson effect plus stretch control plus EOD acceleration.
- **UV is contested.** Don't oversell. If running UV, late flower (last 2–3 weeks), short daily exposure (15–60 min), with grower PPE.

**Intensity beats spectrum in practical decisions.** A 2.7 µmol/J broad-spectrum LED at 1000 PPFD will outperform a 2.2 µmol/J "perfect cannabis spectrum" LED at 700 PPFD nearly every time.

## PPFD Targets per Stage

Without CO₂ supplementation (ambient ~420 ppm):

| Stage | PPFD target (µmol/m²/s) | DLI target (mol/m²/day) | Photoperiod |
|---|---|---|---|
| Clones / seedlings | 100 – 300 | 7 – 15 | 18/6 (lower duty cycle ok) |
| Early veg | 300 – 500 | 19 – 32 | 18/6 |
| Mature veg | 500 – 700 | 32 – 45 | 18/6 |
| Flower stretch (wk 1–3) | 600 – 900 | 26 – 39 | 12/12 |
| Mid flower (wk 3–6) | 800 – 1000 | 35 – 43 | 12/12 |
| Late flower (wk 6+) | 800 – 1000 | 35 – 43 | 12/12 |
| Last 7–10 days | 700 – 900 | 30 – 39 | 12/12 (some growers reduce ~10%) |

With CO₂ supplementation (1200–1500 ppm) **and matching temp (28–30°C):**
- Push PPFD ceiling 50–80% higher: **1200–1800 µmol/m²/s in flower**.
- DLI ceiling moves up — Rodriguez-Morrison & Zheng 2021 found yield increased linearly to **1800 PPFD / 78 mol/m²/d DLI** even at ambient CO₂; with CO₂ enrichment, the ceiling moves further.

(Tier 1 — Rodriguez-Morrison, Llewellyn, Zheng 2021. Their study tested 120–1800 PPFD across 12-week flower runs and found dry inflorescence yield increased linearly with canopy PPFD; leaf-level photosynthesis saturated well below, but whole-canopy yield kept gaining due to deeper light penetration.)

### Cultivar Sensitivity
Some cultivars bleach or photoinhibit at lower PPFD than others (often older HPS-bred genetics). Push intensity progressively over 3–5 days if increasing more than 200 µmol/m²/s — let plants acclimate.

## DLI (Daily Light Integral)

DLI is the total moles of photons delivered per square meter per day. It's the right metric for comparing across schedules.

### Calculation

```
DLI (mol/m²/day) = PPFD (µmol/m²/s) × hours × 3600 / 1,000,000
                 = PPFD × hours × 0.0036
```

### Quick Conversions

| PPFD | 12/12 DLI | 18/6 DLI | 20/4 DLI | 24/0 DLI |
|---|---|---|---|---|
| 200 | 8.6 | 13.0 | 14.4 | 17.3 |
| 400 | 17.3 | 25.9 | 28.8 | 34.6 |
| 600 | 25.9 | 38.9 | 43.2 | 51.8 |
| 800 | 34.6 | 51.8 | 57.6 | 69.1 |
| 1000 | 43.2 | 64.8 | 72.0 | 86.4 |
| 1200 | 51.8 | 77.8 | 86.4 | 103.7 |
| 1500 | 64.8 | 97.2 | 108.0 | 129.6 |
| 1800 | 77.8 | — | — | — |

### Why DLI Is the Right Metric

A flower room at **12/12 + 900 PPFD** delivers 38.9 DLI.
A veg room at **18/6 + 600 PPFD** delivers 38.9 DLI.

The same plant biology (carbon fixation budget) is going on. This is why veg-stage plants under shorter intense bursts can match longer-photoperiod softer light, and why 12/12 hard-flower lighting is *more* punishing per hour than veg.

### Practical DLI Caps

| Use case | Practical DLI ceiling |
|---|---|
| Clones / seedlings | 12–15 (above stresses immature roots) |
| Veg, no CO₂ | 35–45 |
| Veg, with CO₂ | 50–60 |
| Flower, no CO₂ | 35–45 (limited by 12/12 at safe PPFD ~1000) |
| Flower, with CO₂ | 50–65 (push PPFD to 1500–1800) |
| Research/commercial maxima (Rodriguez-Morrison 2021) | 78 (linear yield up to here, at 1800 PPFD) |

## DLE (Daily Light Extension) and End-of-Day Far-Red

### The Mechanism (Tier 1 — Kusuma, Westmoreland, Zhen, Bugbee 2021)

In a normal 12/12 flower schedule, the flowering signal depends on **active Pfr phytochrome dropping below a threshold during the dark period.** Pfr converts back to Pr through "dark reversion" — a slow process taking 1–2+ hours.

**End-of-Day (EOD) far-red treatment** at the moment lights go off accelerates Pfr → Pr conversion via direct far-red absorption, bypassing the slow natural reversion. This gives growers two practical levers:

1. **Photoperiod extension:** run **13/11 or 13.5/10.5** instead of 12/12, gaining 1–1.5 hours of high-PPFD light per day (a meaningful DLI bump) while still delivering the "long-night" signal.
2. **Some flowering acceleration** in light-sensitive cultivars (cited 3–7 day finish acceleration, Tier 3 — community reports, less consistent than the DLI gain).

### Practical Setup
- Far-red panel (730 nm peak) on a separate timer
- Activates **at the moment main lights turn off** (or last 5 minutes of main light cycle)
- Duration: 10–15 minutes of far-red
- Then full darkness through normal "night" period

### When NOT to Use EOD Far-Red
- If your main flower run is already at the PPFD ceiling — the extra hour of light is the actual benefit, but if you can't sustain it without overheating, skip it.
- Some cultivars don't respond to EOD acceleration (Tier 3 reports vary by chemovar).
- DLE is not a substitute for proper environment — running 13/11 in an underspec'd room just bakes plants longer.

## Fixture Types Comparison

| Type | µmol/J (fixture) | Heat | Lifespan | Strengths | Weaknesses | Best for |
|---|---|---|---|---|---|---|
| **Top LED bar / quantum board** (Fluence, Gavita LED, HLG, Migro) | 2.7 – 3.0 | Low (driver heat only) | 50,000+ hr | Best efficiency, dimmable, even canopy coverage | High capital cost | All stages, sealed rooms, commercial |
| **Mid-tier LED** (Mars Hydro, Spider Farmer, ViparSpectra) | 2.2 – 2.6 | Low to medium | 30,000–50,000 hr | Affordable, broad-spectrum white | Variable QC, dimmer noise on some | Hobby tents, beginners |
| **HPS double-ended (DE)** | 1.9 – 2.1 | High (radiant) | 8,000 hr | Cheap photons, classic flower spectrum, easy ramp-up | Heat dump, electricity, bulb degradation 6mo | Flower-only commercial, vented rooms, cold climates |
| **CMH / LEC 315W** | 1.9 – 2.1 | Medium-high | 16,000 hr | Best HID spectrum (broad, high CRI), full-spectrum incl. some UV | Moderate efficacy, hot, requires special socket | Veg, dual-purpose, growers wanting "natural" spectrum |
| **HPS single-ended** | 1.5 – 1.7 | High | 8,000 hr | Cheapest entry | Outdated, inefficient | Legacy systems only |
| **T5 fluorescent** | 0.7 – 0.9 | Low | 10,000 hr | Cool, gentle, cheap | Useless for flower; PPFD ceiling ~250 | Clones, mother plants, seedlings |
| **MH (metal halide)** | 1.4 – 1.6 | High | 12,000 hr | Veg spectrum (high blue) | Inefficient compared to LED | Mostly superseded |

### LED Has Won
For new builds in 2025+, top-tier LED is the default unless capital constraints or specific climate (cold rooms benefiting from HID heat dump) push otherwise. The efficiency gap (~50% more photons per watt vs HPS) compounds across years of operation.

### LED Bar vs Quantum Board
- **Bars** (Gavita 1700e, Fluence SPYDR) — better edge coverage, ideal for large rooms, multi-fixture installs
- **Quantum boards** (HLG 600, similar) — lower hang height tolerance, ideal for tents and small rooms

## Hang Height Math

PPFD falls off **roughly with the inverse square** of distance close to the source, then more linearly farther out as the canopy spreads.

### Manufacturer PPFD Charts
Reputable LED manufacturers publish PPFD-at-distance charts (Fluence, Gavita, HLG do; some no-name brands lie). Use these as starting points:

```
Example (HLG 600 Rspec at 100% drive, center reading):
  12 inches: ~1100 µmol/m²/s
  18 inches: ~750 µmol/m²/s
  24 inches: ~500 µmol/m²/s
  30 inches: ~370 µmol/m²/s
```

Apply to current stage:
- Seedling (200 PPFD target): 30+ inches OR dim the fixture
- Veg (500 PPFD target): 24 inches at 100% OR 18 inches at 70%
- Flower (900 PPFD target): 14–18 inches at 100%

### Hang Height vs Dimmer Trade-off
- **Higher hang + higher dimmer setting** = more uniform canopy coverage (better for SCROG/even canopy)
- **Lower hang + lower dimmer setting** = more peak intensity at center, falloff at edges (better for solo-plant tents)

Most growers should hang as high as possible while still hitting target PPFD at canopy. Uniformity > peak intensity for total yield.

### Verification Tools

| Tool | Cost | Accuracy | Use case |
|---|---|---|---|
| **Apogee MQ-500** | ~$500 | Lab-grade | Commercial dialing, breeder QC |
| **Apogee MQ-100 / SQ-110** | ~$300 | Excellent | Serious hobby / craft commercial |
| **Photone app + cosine corrector** | $5 + $30 hardware | Good (±10%) | Hobby growers — best per-dollar |
| **Photone app, no corrector** | $5 | Mediocre (±20%+) | Rough check only |
| **Ali / no-name PAR meters** | $40–80 | Variable | Distrust unless cross-checked |

The Photone app with a cosine corrector is the breakthrough for hobbyists — it turns a phone into a usable quantum sensor.

## Light Burn / Bleaching / Photoinhibition

### Three Distinct Failure Modes

| Mode | Cause | Symptom | Fix |
|---|---|---|---|
| **Light burn (radiant heat)** | HPS/HID hung too close, leaf surface heated by IR | Top-leaf bleach/curl, scorched edges, only on leaves nearest fixture | Raise fixture, increase canopy airflow |
| **Photobleaching** | Excessive PAR intensity, typically >1500 PPFD without CO₂ + matching temp | White/pale-yellow tops, often along stretched colas, often only the most-exposed buds | Lower PPFD via dimmer or raise fixture; add CO₂ if pushing high PPFD intentionally |
| **Photoinhibition** | Stomata close defensively under excess light; photosynthesis stalls; plant growth slows | Slow growth, leaf taco, plants "stop" responding; less visible damage than bleaching | Reduce PPFD; ensure VPD and CO₂ are within range; check leaf temp |

### Bleaching Threshold
Without CO₂ + matched temp: **~1500 µmol/m²/s** is the typical bleach onset. Some genetics tolerate 1800; older HPS-bred genetics may bleach at 1100–1200.

With CO₂ at 1200–1500 ppm + temp 28–30°C: bleach threshold pushes to **1800–2100 PPFD**.

### Foxtailing
Late-flower abnormal bud structure where new pistil clusters emerge from existing buds, producing tall narrow "fox tail" shapes.

| Cause | Tell |
|---|---|
| Genetics | Pure sativa or sativa-leaning genetics foxtail naturally regardless of conditions |
| Heat stress | Foxtails appear suddenly during late flower with canopy >30°C, especially under intense LED |
| Light intensity | Top colas closest to fixture foxtail; rest of plant doesn't |

If foxtailing on multiple cultivars in same room → environment (heat / light intensity). If only on one cultivar → genetics, accept it.

## Photoperiod Schedules

### Veg Schedules

| Schedule | Pros | Cons | When to use |
|---|---|---|---|
| **18/6** | Standard, plant rest period, energy savings | Modest growth speed | Default for most growers |
| **20/4** | Faster growth, marginally more DLI | Higher electricity, more heat | Production veg, when speed matters |
| **24/0** | Maximum DLI possible | Plants need rest period — debated yield gain; common in commercial | Commercial only; not for stress-prone genetics |
| **6/2 (gas-lantern)** | Saves 2 hours of light vs 18/6 | More controller complexity | Cost-saving in long veg cycles; some breeder use |

### Flower Schedules

| Schedule | Use |
|---|---|
| **12/12** | Standard for photoperiod cultivars; works for nearly every cultivar |
| **13/11 with EOD far-red** | DLI extension via far-red trick (see DLE section) |
| **11/13 or 10.5/13.5** | Faster ripening, may boost cannabinoid maturation in some cultivars; often used last 2 weeks of flower (Tier 3 — community trick, less consistent than 12/12) |

### Autoflowers
Run **18/6 or 20/4 throughout the cycle.** Autos don't respond to photoperiod, so the question is purely DLI vs electricity cost. Most growers run 20/4 for max DLI given the fixed 8–12 week window.

### Light Leak Threshold
Cannabis cannot perceive light below **~10 nmol/m²/s** during dark period (Bugbee research; cross-ref `00-fundamentals.md` Photoperiod Biology). A bright moon, brief phone screen, or distant power LED is below threshold. A room light flicked on, sliver of sun under door, or a status LED inches from canopy can exceed it. Conservative: black out fully because the cost of leak (herm) >> cost of blackout material.

## Confusion / Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| "1000W LED" with weak yield | Fixture draws far less than advertised, OR low µmol/J | Measure actual draw at wall; check fixture spec sheet for real µmol/J at the fixture |
| "Lumens claim" on grow light | Marketing — plants don't see lumens | Demand PPF (µmol/s) and PPFD chart; reject lumens-only product |
| Light burn on top buds | Could be heat (HPS), bleaching (LED), or both | HPS hand test (uncomfortable in 30s = too close); LED uses PPFD reading |
| "Spectrum is wrong, my yield is low" | Almost always intensity, not spectrum | Check PPFD with meter before changing spectrum |
| Edges yielding less than center | Hang too low, beam too narrow | Raise fixture; verify PPFD across canopy with spot measurements |
| Foxtailing in early flower | Heat or genetics, not "light burn" | Check leaf temp, check cultivar history |
| "EOD far-red doubled my yield" | DLI extension provided the gain, far-red made the schedule possible | Compare 13/11+EOD to 13/11 without EOD (latter herms), not to 12/12 |
| HPS "more potent" than LED | HPS buds often have more "popcorn" growth from heat — not real potency advantage | Lab COA tells the truth |
| Plants stretching too much in flower | Likely small DIF (warm nights) AND/OR low blue % spectrum | Check night temp first, then spectrum |
| Manufacturer chart says 800 PPFD at 18 inches; my plants act starved | Chart is at center under ideal conditions; edges and aging fixtures lower | Spot-check with quantum sensor across the canopy |
| "DLI of 78 in flower with 24/0" | 24/0 is impossible in flower — would re-veg the plant | Confirm photoperiod; may be confusing veg DLI with flower DLI |
| UVB "boosted my THC by 30%" | Older Lydon 1987 study said yes; Westmoreland/Bugbee 2022 said no in better-controlled study | Tier 1 conflict — present both views; default skeptical until more research |

## Quick Reference

### PPFD/DLI by Stage (No CO₂)

| Stage | PPFD | DLI |
|---|---|---|
| Clones / seedlings | 100 – 300 | 7 – 15 |
| Early veg | 300 – 500 | 19 – 32 |
| Mature veg | 500 – 700 | 32 – 45 |
| Flower stretch | 600 – 900 | 26 – 39 |
| Mid flower | 800 – 1000 | 35 – 43 |
| Late flower | 800 – 1000 | 35 – 43 |

### PPFD/DLI by Stage (With CO₂ 1200–1500 ppm)

| Stage | PPFD | DLI |
|---|---|---|
| Veg | 700 – 1000 | 45 – 65 |
| Flower stretch | 900 – 1200 | 39 – 52 |
| Mid flower | 1200 – 1600 | 52 – 69 |
| Late flower | 1200 – 1800 | 52 – 78 |

### Hang Height Quick Reference (Top-Tier LED at 100%)

| Stage | Approximate hang height |
|---|---|
| Clones / seedlings | 30+ inches OR dim to 30% |
| Veg | 24 inches at 70%, or 30 inches at 100% |
| Flower | 14–18 inches at 100% |

### Fixture Efficiency Tier List (µmol/J at fixture)

| Tier | Range | Examples |
|---|---|---|
| Top | 2.7 – 3.0 | Fluence SPYDR, Gavita 1700e LED, HLG 600 Rspec, Migro Aray |
| Strong | 2.4 – 2.7 | Mars Hydro FC-E, Spider Farmer SE series (newer), AC Infinity Ionframe Evo |
| Mid | 2.2 – 2.4 | Older quantum boards, mid-tier Chinese exports |
| HPS / CMH | 1.7 – 2.1 | Gavita Pro DE 1000, Sun System LEC 315 |
| Avoid for serious work | <2.0 LED | No-name imports without third-party PAR data |

### Common Problem → Fix

| Problem | First check |
|---|---|
| Yield under expectation | PPFD with quantum sensor — rarely matches the "1000W" claim |
| Bleached tops | Hang height OR dimmer setting too aggressive; check CO₂ + temp couple |
| Slow growth despite "good" setup | Light too far from canopy OR fixture older / less efficient than claimed |
| Stretchy veg | Low blue % spectrum or low PPFD |
| Foxtailing | Heat first, genetics second |
| Stretchy flower | Small DIF + spectrum + intensity all interact |

## Sources

**Tier 1 — Peer-reviewed:**
- Rodriguez-Morrison, V., Llewellyn, D., & Zheng, Y. — *Cannabis Yield, Potency, and Leaf Photosynthesis Respond Differently to Increasing Light Levels in an Indoor Environment.* Frontiers in Plant Science, 2021. (PPFD linear yield to 1800; DLI 78 mol/m²/d.)
- Westmoreland, F. M., Kusuma, P., & Bugbee, B. — *Cannabis lighting: Decreasing blue photon fraction increases yield but efficacy is more important for cost effective production of cannabinoids.* PLOS ONE, 2021.
- Westmoreland, F. M., & Bugbee, B. — *Indoor grown cannabis yield increased proportionally with light intensity, but ultraviolet radiation did not affect yield or cannabinoid content.* Frontiers in Plant Science, 2022. (Disputes Lydon 1987 UVB-THC claim.)
- Kusuma, P., Westmoreland, F. M., Zhen, S., & Bugbee, B. — *Photons from NIR LEDs can delay flowering in short-day soybean and Cannabis: Implications for phytochrome activity.* PLOS ONE, 2021. (EOD far-red mechanics.)
- Magagnini, G., Grassi, G., & Kotiranta, S. — *The Effect of Light Spectrum on the Morphology and Cannabinoid Content of Cannabis sativa L.* Medical Cannabis and Cannabinoids, 2018.
- Hawley, D., Graham, T., Stasiak, M., & Dixon, M. — *Improving Cannabis Bud Quality and Yield with Subcanopy Lighting.* HortScience, 2018.
- Lydon, J., Teramura, A. H., & Coffman, C. B. — *UV-B radiation effects on photosynthesis, growth and cannabinoid production of two Cannabis sativa chemotypes.* Photochemistry and Photobiology, 1987. (Original UVB-THC claim, contested by 2022 study.)
- McCree, K. J. — *The action spectrum, absorptance and quantum yield of photosynthesis in crop plants.* Agricultural Meteorology, 1972. (Foundation of PAR / PPFD as the right plant-light metrics.)
- Chandra, S., Lata, H., Khan, I. A., & ElSohly, M. A. — *Photosynthetic response of Cannabis sativa L. to variations in PPFD, temperature and CO₂ conditions.* Physiology and Molecular Biology of Plants, 2008.

**Tier 2 — Manufacturer / industry technical:**
- Fluence Bioengineering — published µmol/J data, PPFD charts, Bugbee USU validation results.
- Gavita Holland — fixture spec sheets and PPFD distribution maps.
- HLG (Horticulture Lighting Group) — quantum board efficacy data and Rspec spectrum documentation.
- Migro — independent fixture PAR testing channel and lab data.
- Apogee Instruments — quantum sensor calibration documentation; the de facto industry reference.
- Photone — phone-based PPFD measurement methodology and cosine corrector documentation.

**Tier 3 — Master growers / educators:**
- DeBacco University (YouTube) — lighting and PPFD protocols.
- Mr. Canucks Grow — practical hang heights, real-world PPFD verification.
- Migro YouTube — independent fixture comparisons and bleaching threshold testing.

## Cross-References

- CO₂ × PPFD coupling, leaf-temp + lighting interaction → `02-environment.md`
- Photosynthesis biology (C3, McCree action), phytochrome system → `00-fundamentals.md`
- Photoperiod transitions and stretch management → `12-flowering.md`
- Stretch reduction via DIF and spectrum together → `02-environment.md` + `12-flowering.md`
- Light intensity scales nutrient (especially K) demand → `06-nutrients-synthetic.md`
- Last-week light protocols (intensity drop, finishing) → `13-harvest.md`
- Light leak threshold and herm prevention → `00-fundamentals.md` Photoperiod Biology section
- Drying-room light (always dark) → `14-drying.md`
