# 02 — Environment

VPD, temperature, humidity, CO₂, and airflow targets per stage, plus equipment-sizing math for AC, dehumidification, CO₂, and ventilation. Environment is the most consequential variable after genetics and the most common silent killer of grows. Cross-reference with `03-lighting.md` (PPFD/DLI determines optimal temp and CO₂ ceiling), `07-deficiencies.md` (Ca and B problems are usually transpiration problems = VPD problems), `08-pests.md` and `09-disease.md` (most pest/pathogen pressure is RH-driven), `12-flowering.md` (stage transitions force climate shifts), `14-drying.md` (drying environment is environment too).

## How to Use This File

When diagnosing or dialing environment, always check in this priority order:

1. **VPD first** — too low or too high is upstream of most other "environment" problems
2. **Temperature** — day, night, and root zone separately; under-spec'd AC is a hidden ceiling
3. **Humidity** — RH alone misleads; check dew point gap as secondary check
4. **CO₂** — only matters if PPFD is also high; otherwise wasted
5. **Airflow** — two systems (air exchange + canopy circulation); both must work
6. **Stage match** — confirm targets match the current life-cycle stage

## Core Concepts

| Concept | What it means | Why it matters |
|---|---|---|
| **VPD is the master variable** | Vapor pressure deficit drives stomatal behavior, transpiration, and nutrient delivery — temp and RH alone are partial views | Two rooms can have identical temp + RH and very different VPD if leaf temp differs |
| **Day vs night divergence** | Targets shift when lights turn off — temp drops, RH naturally rises | Hitting day target with same setting at night = botrytis or excess VPD |
| **Leaf temp ≠ ambient temp** | Transpiring leaves run 1–3°C below ambient under LED; under intense direct beam without good airflow, leaf temp can exceed ambient | IR thermometer at canopy gives real VPD; ambient gauge lies |
| **CO₂ is light-coupled** | Adding CO₂ above ambient only helps if PPFD is high enough to use it (>800 µmol/m²/s) | Enrichment under modest light = wasted money |
| **Stage-progressive shifts** | Warmer + wetter early, cooler + drier late | Same recipe across the cycle either stresses early or rots late |
| **Two airflows, not one** | Intake/exhaust (room air exchange) and canopy circulation (leaf surface flutter) are separate systems with separate jobs | Killing one to "save space" causes Ca def, PM, gnats |

## VPD — The Master Variable

### What VPD Actually Is
Vapor pressure deficit (VPD) is the difference between the moisture the air *could* hold at saturation and the moisture it *actually* holds, expressed in kilopascals (kPa). When VPD is high, the air "pulls" water out of the leaf strongly via the stomata. When VPD is low, the air is near-saturated and water doesn't leave the leaf efficiently.

Because nutrient delivery to the upper plant rides on the transpiration stream, VPD directly controls how Ca, B, and S reach new growth (see `00-fundamentals.md`).

### Calculation (Magnus Approximation)

```
e_sat (kPa) = 0.6108 × exp((17.27 × T) / (T + 237.3))
   where T is leaf temperature in °C

VPD (kPa) = e_sat × (1 − RH/100)
```

**Practical:** use a VPD calculator app or chart — but the inputs that matter are **leaf temperature** (not ambient) and **RH**.

### Leaf Temperature Offset (Critical)

Transpiring leaves run **1–3°C below ambient air temperature** under LED lighting because evaporative cooling. Under HPS (more radiant heat), the offset is smaller or absent. Under intense direct beam with poor canopy airflow, leaf temp can *exceed* ambient.

| Lighting type | Typical leaf-vs-ambient offset |
|---|---|
| LED, good airflow, healthy transpiration | Leaf is 1–3°C cooler |
| LED, low VPD, weak transpiration | Leaf ≈ ambient |
| HPS / CMH | Leaf ≈ ambient or warmer (radiant heat load) |
| Underpowered fan + dense canopy | Leaf can be 2–4°C *warmer* than ambient |

**Diagnostic:** point an IR thermometer (~$15) at a mature fan leaf at canopy height. The reading is your real VPD input. Calculations using ambient air temp routinely understate VPD by 0.2–0.4 kPa.

### VPD Targets per Stage

| Stage | Target VPD (kPa) | Notes |
|---|---|---|
| Clone / seedling | 0.4 – 0.8 | Roots are immature; high transpiration stresses rootless cuts |
| Early veg | 0.8 – 1.0 | Building leaf mass; moderate transpiration |
| Mature veg | 1.0 – 1.2 | Dialing toward flower targets |
| Flower stretch (wk 1–3) | 1.0 – 1.3 | Transition window |
| Mid flower (wk 3–6) | 1.2 – 1.5 | Peak transpiration / nutrient demand |
| Late flower (wk 6+) | 1.2 – 1.5 | Drier air than mid-flower; botrytis prevention. ("Finishing" stage in next row deliberately pushes higher.) |
| Drying | 0.8 – 1.0 (room VPD, not leaf) | Slow water loss, terpene preservation — see `14-drying.md` |

(Sources: Tier 1 — Bugbee VPD/transpiration research; Tier 2 — Pulse Pro published targets, Quest Climate cultivation guides; values cross-confirmed across all sources.)

### What Goes Wrong at the Extremes

**VPD too low (humid, cool, weak transpiration):**
- Ca and B deficiency despite correct feed (transpiration too weak to deliver immobile nutrients)
- Powdery mildew risk explodes
- Botrytis in late flower if RH > 60%
- Slow growth, watery brittle leaves
- Stomata don't close at night → energy waste

**VPD too high (dry, hot, excess transpiration):**
- Leaf taco / curl up (defensive stomatal closure)
- Wilting between waterings
- Salt accumulation in substrate (plants drink water faster than nutes)
- Burnt leaf tips
- Growth slows because stomata are closed → no CO₂ uptake

## Temperature

### Day vs Night Targets per Stage

Without CO₂ enrichment (ambient ~420 ppm):

| Stage | Day temp °C | Night temp °C | DIF (day−night) |
|---|---|---|---|
| Seedling | 22 – 25 | 20 – 22 | 2 – 3°C |
| Veg | 22 – 26 | 19 – 22 | 3 – 5°C |
| Flower stretch | 24 – 26 | 19 – 22 | 4 – 6°C (large DIF reduces stretch) |
| Mid flower | 22 – 26 | 18 – 21 | 4 – 6°C |
| Late flower | 20 – 24 | 16 – 20 | 4 – 6°C (cool nights deepen color, terpene hold) |

With CO₂ enrichment (~1200–1500 ppm) **and high PPFD (≥800 µmol/m²/s):**
- Add **+3 to +4°C** to day temperatures across all stages.
- Optimal photosynthesis under enriched CO₂ shifts to **28–30°C** at the leaf (Tier 1 — Chandra et al., 2008).
- Night temps unchanged.

### Day-Night Differential (DIF)

DIF is **day temp minus night temp**. Plants integrate the difference into growth signaling:
- **Large DIF (5–8°C)** suppresses stem elongation. Use to limit stretch in flower wk 1–3.
- **Small DIF (1–3°C) or negative DIF** (night warmer than day) maximizes stretch. Useful for short cultivars in tall rooms; rarely intentional.
- DIF effect operates within the first 2 hours of lights-on — that's when stem-elongation hormones are most plastic.

### Hard Thresholds

| Threshold | Effect |
|---|---|
| **Canopy >30°C** | Photorespiration losses begin, leaf taco starts (low VPD masks this until late) |
| **Canopy >32°C sustained** | Heat stress, terpene volatilization accelerates, foxtailing in flower, herm risk |
| **Canopy >35°C** | Acute damage, bract burn, rapid quality loss |
| **Canopy <15°C** | P uptake stalls (purpling stems often), enzyme rates drop, root growth halts |
| **Canopy <10°C** | Cold stress damage, anthocyanin accumulation cosmetic but warning sign |
| **Root zone <15°C** | Calcium and phosphorus uptake plummet — common winter problem in concrete-floor grows |
| **Root zone >25°C** | Root rot risk in hydro skyrockets (pythium thrives 25–30°C) |
| **Root zone hydro target** | 18–22°C — narrow window, often the limiting factor in summer hydro |

### Common Temperature Mistakes

- **Measuring at gauge height instead of canopy.** Heat rises; canopy temp can exceed thermostat reading by 2–4°C under intense lighting.
- **Ignoring root zone temp.** A 24°C ambient room with a 14°C concrete floor = unhappy roots in fabric pots.
- **Same setpoint day and night.** AC continues to cool through lights-off → night temp drops too far → cold stress.
- **Overreliance on AC dimming light to compensate.** Cutting PPFD to fight heat sacrifices yield; fix the heat dump first.

## Humidity (RH)

### RH Targets per Stage

| Stage | Day RH | Night RH | Notes |
|---|---|---|---|
| Seedling / clone | 65 – 75% | 70 – 80% | Roots immature; high RH protects against transpiration shock |
| Early veg | 55 – 70% | 60 – 70% | Tapering down |
| Mature veg | 50 – 65% | 55 – 65% | Building toward flower targets |
| Flower stretch (wk 1–3) | 50 – 60% | 55 – 65% | RH still moderate |
| Mid flower (wk 3–6) | 45 – 55% | 50 – 60% | Stay below 60% lights-off |
| Late flower (wk 6+) | 40 – 50% | 45 – 55% | Botrytis cliff: every +5% above 50% multiplies risk in dense colas |
| Final 7–10 days | 35 – 45% | 40 – 50% | Dry air "finishes" buds, hardens for harvest, bumps trichome production marginally |

### The Botrytis Cliff (Late Flower)

Botrytis (gray mold, "bud rot") thrives when:
- RH >60% sustained
- Temperature 17–23°C (the indoor sweet spot — cruel coincidence)
- Free water on bud surfaces (condensation, foliar spray, contact watering)
- Dense bud structure trapping moisture inside

**Dew-point gap rule of thumb:** keep **room temperature minus dew point ≥ 6–8°C** in flower. Dew point gap is a better botrytis predictor than RH percentage alone, because it accounts for temperature swings during lights-off when condensation forms on the coolest surfaces (often inside-bud).

```
Quick dew-point calc (approximate):
DP (°C) ≈ T (°C) − ((100 − RH) / 5)
Example: 22°C, 55% RH → DP ≈ 22 − 9 = 13°C → gap = 9°C → safe
Example: 22°C, 75% RH → DP ≈ 22 − 5 = 17°C → gap = 5°C → bot risk
```

### Low RH Stress

- Below 35% RH in veg → growth slows, leaves taco
- Below 30% RH → spider mite explosion (mites love hot dry air)
- Bone-dry winter air (sub-25%) without humidification → seedling death

### Day-Night RH Behavior

When lights turn off, **temperature drops but absolute moisture in air stays the same** for the first hour. Result: RH spikes up. A room at 25°C / 50% RH at lights-off cooling to 19°C without dehumidification will hit ~70% RH within an hour. Late-flower rooms need either: (1) night dehumidification cycle, or (2) AC + dehumidifier coordination, or (3) acceptance of higher RH only in mid-veg or earlier.

## CO₂

### Ambient vs Enriched

- **Ambient atmosphere** is ~420 ppm CO₂ (and rising globally).
- **Cannabis photosynthesis saturates at ~1500 ppm CO₂** with high PPFD (Tier 1 — Chandra 2008; cross-confirmed in Bugbee CO₂ work).
- Above ~1500 ppm, returns diminish sharply; above ~2000 ppm, no benefit and increasing safety/cost issues.

### The PPFD Coupling

CO₂ supplementation only delivers gains when **light is also high**. The relationship:

| PPFD (µmol/m²/s) | CO₂ enrichment payoff |
|---|---|
| <400 | None — light is the limit, CO₂ wasted |
| 400 – 800 | Marginal — small yield improvement |
| 800 – 1200 | Moderate — measurable yield improvement |
| 1200 – 1800 | Strong — typical commercial CO₂ recipe operating range |
| >1800 | Diminishing — also approaches PPFD photoinhibition threshold for cannabis |

(Tier 1 — Rodriguez-Morrison et al. 2021 found dry inflorescence yield increased linearly with PPFD up to **1800 µmol/m²/s** in their study, though leaf-level photosynthesis saturated well below — explained by deeper canopy penetration delivering useful light even after individual leaves saturated.)

### Temperature Coupling

Enriched CO₂ raises the optimal temperature window:
- **Ambient CO₂:** optimum photosynthesis 22–26°C
- **Enriched CO₂ (1200+ ppm):** optimum 26–30°C

This is why CO₂-enriched rooms typically run a few degrees warmer — and why running ambient-CO₂ rooms hot is just stress without the gain.

### Supplementation Methods

| Method | Pros | Cons |
|---|---|---|
| Compressed CO₂ tank + regulator + controller | Clean, precise, no heat | Tank refills, capital cost |
| Propane/natural gas burner | Cheap CO₂ per ppm | Adds heat + humidity (gas combustion = water vapor) |
| Fermentation buckets / yeast | Cheap, low-tech | Inconsistent, peaks too low for full enrichment |
| Compost pile / mushroom grow nearby | Passive | Tiny bump, not real enrichment |
| CO₂ generator (combustion unit) | High output | Heat + humidity load + safety |

### Sealed vs Vented Requirement

CO₂ enrichment **requires a sealed room**. In a vented room, supplemented CO₂ vents straight out the exhaust — you're paying to fertilize the outside.

- **Sealed:** AC + dehumidifier + CO₂ supplementation. Air doesn't leave the room. All temp/RH control is internal.
- **Vented (active intake/exhaust):** ambient CO₂ only. Replace warm humid air with fresh outdoor air on a fan duty cycle.
- **Hybrid:** vented during lights-on with CO₂ off, sealed during lights-off — generally not worth the complexity.

### Safety Thresholds

- **OSHA 8-hour exposure limit:** 5,000 ppm
- **Headache / impaired judgment:** ~10,000 ppm
- **Acute danger:** 30,000+ ppm
- **Always have a CO₂ alarm** in a CO₂-enriched room, especially if it's in a basement or below grade (CO₂ is denser than air and pools low).

## Airflow

Two distinct systems serve different purposes:

### System 1 — Air Exchange (Intake/Exhaust)
**Purpose:** replace stale, warm, humid air with fresh CO₂-rich outdoor air.
**Applies to:** vented (active) rooms only. Sealed rooms skip this.

**Sizing:**
```
CFM_baseline = Room volume (ft³) / Exchange interval (minutes)
```
- **Aggressive (light + heat heavy):** 1-minute exchange → CFM = volume in ft³
- **Standard cannabis room:** 2–3 minute exchange → CFM = volume / 2–3
- **Low-load:** 4–5 minute exchange (HID without LEC dimming, very hot climates needing more cycling)

Multiply baseline by:
- **×1.25** for carbon filter (back-pressure reduces effective CFM)
- **×1.5** for ducting >5 m or multiple bends
- **×1.5–2** for HPS/HID lighting (radiant heat)

Example: 4×4×7 ft tent (112 ft³), LED, carbon filter, 3-min exchange:
```
Baseline: 112 / 3 = 37 CFM
With filter: 37 × 1.25 = 47 CFM
→ Use a 6-inch inline fan rated 200+ CFM dialed to 25%
```

Always size larger than calculated and dial down — running a small fan at 100% wears it out faster than a larger fan at 30%.

### System 2 — Canopy Circulation
**Purpose:** move air across leaf surfaces, prevent dead air zones, strengthen stems, distribute CO₂ to stomata.
**Applies to:** every room — sealed and vented.

**Goal:** every leaf in the canopy should have **gentle continuous flutter** (not flag-snapping wind, not still). Stems develop strength via slight stress; dead air = Ca def, PM, fungus gnats.

**Placement:**
- Above-canopy (LED) — ceiling-mounted clip fans, oscillating
- Sub-canopy — small fan(s) blowing horizontally under the canopy to break up stagnant zones
- Avoid blasting one fan at one direction — alternates with oscillation

**Quantity rules of thumb:**
- 1×4 ft tent: 1 small (6") oscillating
- 2×4 ft tent: 2 oscillating
- 4×4 ft tent: 2–3 oscillating + 1 sub-canopy
- 5×5+ rooms: dedicated mounted oscillators above and below canopy

### Dead Air Zones — Diagnostic

If you find:
- Ca def appearing in flower despite proper feed → check airflow over the affected canopy area
- PM showing up in patches (one corner of the tent) → dead air zone
- Fungus gnats concentrated on certain pots → soil staying wet too long from low evaporation

These are airflow problems first, not nutrient/IPM problems.

## Stage-Specific Climate Recipes

| Stage | VPD (kPa) | Day temp °C | Night temp °C | Day RH | Night RH | CO₂ | Airflow notes |
|---|---|---|---|---|---|---|---|
| Seedling | 0.4 – 0.8 | 22 – 25 | 20 – 22 | 65 – 75% | 70 – 80% | Ambient | Gentle indirect, no direct fan on cotyledons |
| Early veg | 0.8 – 1.0 | 22 – 26 | 20 – 22 | 55 – 65% | 60 – 70% | Ambient or 800 ppm | Increase as plants size up |
| Mature veg | 1.0 – 1.2 | 22 – 26 | 19 – 22 | 50 – 60% | 55 – 65% | Ambient or 1000–1200 ppm | Full canopy circulation, leaf flutter at all heights |
| Flower stretch (wk 1–3) | 1.0 – 1.3 | 24 – 26 (large DIF to limit stretch) | 19 – 22 | 50 – 60% | 55 – 65% | 1000 – 1200 ppm | Sub-canopy fans on as canopy thickens |
| Mid flower (wk 3–6) | 1.2 – 1.5 | 22 – 26 (28 – 30 if CO₂ + PPFD ≥1200) | 18 – 21 | 45 – 55% | 50 – 60% | 1200 – 1500 ppm | Aggressive circulation; defoliation may be needed |
| Late flower (wk 6+) | 1.2 – 1.5 | 20 – 24 | 16 – 20 (cool deepens color, holds terps) | 40 – 50% | 45 – 55% | 1000 – 1200 ppm (some growers cut earlier) | Watch for inside-bud condensation at lights-off |
| Final 7–10 days ("finishing") | 1.5 – 1.7 | 18 – 22 | 14 – 18 | 35 – 45% | 40 – 50% | Ambient (CO₂ off) | Cool nights, dry air, prepare for harvest |
| Drying | 0.8 – 1.0 (room) | 16 – 18 | 16 – 18 | 55 – 60% | 55 – 60% | Ambient | Gentle indirect; never on bud surface — see `14-drying.md` |

## Sealed Room vs Active (Vented) Room

| Dimension | Sealed | Active |
|---|---|---|
| Air exchange | None — air recirculates | Continuous via intake/exhaust |
| CO₂ supplementation | Yes (necessary justification for the seal) | No (vents out) |
| AC requirement | Mandatory | Often optional for small tents in cool climates |
| Dehumidifier requirement | Mandatory | Often needed in flower depending on outdoor RH |
| Climate independence from outdoors | High | Low — outdoor RH and temp invade |
| Smell control | Self-contained, plus filter on exhaust loop | Carbon filter on exhaust mandatory |
| Capital cost | Higher | Lower |
| Operating cost | Higher (continuous AC + dehu + CO₂) | Lower (fan-driven) |
| Typical use case | Commercial production, year-round consistency | Hobby tents, seasonal grows, mild climates |

**Hybrid setups** (vented during lights-on, sealed during lights-off, etc.) are usually not worth the complexity. Pick one model.

## Equipment Sizing Math

### AC (BTU/hr) Sizing

```
BTU/hr = (Total light watts × 3.41)
       + (Other equipment watts × 3.41)   ← include dehumidifier!
       + (Occupants × 400)
       + Safety headroom (20%, or 30% for sealed rooms)
```

**Critical reminder:** dehumidifier wattage converts almost entirely to heat inside the room. A 300W dehumidifier adds ~1023 BTU/hr to your cooling load — frequently overlooked.

Example (4×4×7 ft tent, 600W LED, 200W dehu, sealed):
```
Light: 600 × 3.41 = 2046 BTU/hr
Dehu: 200 × 3.41 = 682 BTU/hr
Subtotal: 2728 BTU/hr
+30% headroom: 3546 BTU/hr
→ Round up to 5000 BTU portable or 6000 BTU mini-split
```

### Dehumidifier (Pints/Day) Sizing

Plants transpire **~95–97% of water given**. The dehumidifier must remove approximately what you're irrigating, plus ambient infiltration.

```
PPD_required ≈ Daily irrigation (gallons) × 8 (pints/gallon) × 0.95
             + Outdoor infiltration (varies)
```

Add **25–30% headroom** for peak transpiration and freshly watered plants.

**AHAM rating caveat:** dehumidifier ratings (AHAM DH-1) are at 80°F / 60% RH. Real capacity at typical grow conditions (75°F / 50% RH) is **30–40% lower** than label. Size accordingly.

Example (4×4 tent, 5 plants × 1 gal/day in mid-flower):
```
Transpiration load: 5 × 8 × 0.95 = 38 PPD
+30% headroom: 49 PPD
AHAM derating: 49 / 0.65 = 75 PPD label rating
→ Buy a dehumidifier rated 70–90 PPD AHAM
```

### CFM (Exhaust Fan) Sizing

Already covered in Airflow section. Quick recap:
```
CFM = Room volume (ft³) / Desired exchange interval (min) × adjustment factors (filter, ducting, lighting)
```

### Heater (Watts) Sizing

For unheated rooms in cold climates:
```
Watts ≈ Volume (m³) × 70 (basic insulated room)
      ≈ Volume (m³) × 100 (poorly insulated, garage, basement)
```

A 4×4×7 ft tent ≈ 3 m³ → 200–300W heater suffices for most climates.

### Humidifier (L/Day) Sizing

```
L/day_required ≈ Room volume (m³) × ambient RH deficit (%) × 0.05
```

Most veg/seedling tents need 1–4 L/day humidifier capacity in dry climates. Ultrasonic units are quieter but add no heat; evaporative units are larger and lower-precision.

## Confusion / Misdiagnosis Traps

| Looks like | Actually | How to tell |
|---|---|---|
| Calcium deficiency in late flower | Low VPD / weak transpiration | RH >60%, no leaf flutter at canopy → improve airflow + RH before adding Cal-Mg |
| Heat stress (taco leaves) | Low VPD with stomatal closure stress | If RH is high and leaves are limp + curled, it's not heat — it's drowning, drop RH first |
| Heat stress | Light burn | Heat affects whole canopy uniformly; light burn affects only the closest leaves to the fixture |
| "Lights-off temps too high" | Root zone temp is the actual issue | Measure at substrate, not air |
| Ambient air says 24°C | Canopy is 28°C | IR thermometer at leaf — heat rises, gauge often lies |
| CO₂ enrichment isn't producing yield gains | PPFD is too low to use the CO₂ | Check canopy PPFD with a real meter; need ≥800 µmol/m²/s for any gain |
| Botrytis showed up "out of nowhere" | RH spike at lights-off + dense buds | Track dew point gap, not just day RH |
| Mites despite spray program | Low RH + warm + dead air = mite paradise | Raise RH to 50%, add airflow; chemical alone won't work |
| "VPD chart says I'm in range" | Used ambient temp, not leaf temp | Leaf temp 2°C lower → real VPD 0.2–0.4 kPa higher than chart shows |
| Stretch is excessive in flower | Small DIF (warm nights) | Drop night temp 4–6°C below day to suppress stretch |
| Foxtailing late flower | Heat + light + genetics | Some sativa genetics foxtail under any heat; lower light + drop temp if happening early |
| AC undersized "but it ran fine yesterday" | Outside ambient changed | Heat load math must include peak-day outdoor temp, not yesterday's |

## Quick Reference

### VPD-By-Stage Quick Card (using leaf temp)

| Stage | VPD (kPa) | Typical setpoints |
|---|---|---|
| Clone / seedling | 0.4 – 0.8 | 24°C / 70% RH |
| Veg | 0.8 – 1.2 | 25°C / 60% RH |
| Flower stretch | 1.0 – 1.3 | 25°C / 55% RH |
| Mid flower | 1.2 – 1.5 | 24°C / 50% RH |
| Late flower | 1.2 – 1.5 | 22°C / 50% RH |
| Finishing | 1.5 – 1.7 | 20°C / 40% RH |

### Temperature Hard Limits

| Threshold | Effect |
|---|---|
| Canopy >30°C | Photorespiration + taco begins |
| Canopy >32°C sustained | Heat stress, herm risk, terp loss |
| Root zone <15°C | P uptake stalls |
| Root zone >25°C (hydro) | Pythium risk |

### CO₂ × PPFD Decision

| You have… | CO₂ recommendation |
|---|---|
| LED <500 µmol/m²/s | Don't bother — ambient is fine |
| LED/HID 500–1000 µmol/m²/s | Marginal — try 800–1000 ppm if cheap |
| LED/HID 1000–1500 µmol/m²/s | Worth it — 1000–1200 ppm |
| LED/HID 1500+ µmol/m²/s | Required for full yield — 1200–1500 ppm |

### Equipment Sizing Cheat Sheet

| Equipment | Formula | Typical 4×4 example |
|---|---|---|
| AC (BTU/hr) | (Watts × 3.41) + dehu_watts × 3.41 + 30% | 5000–6000 BTU |
| Dehumidifier (PPD) | Irrigation_gal × 8 × 0.95 × 1.3 ÷ 0.65 | 60–90 PPD |
| Exhaust CFM | Volume_ft³ ÷ 2 × 1.25 (filter) | 70–100 CFM |
| Heater (W) | Volume_m³ × 70–100 | 200–300W |
| Humidifier (L/day) | Volume_m³ × deficit% × 0.05 | 1–3 L/day |

## Sources

**Tier 1 — Peer-reviewed:**
- Bugbee, B. (Utah State University) — VPD, leaf temperature, transpiration, and CO₂ research; multiple papers and Pre-Print Series.
- Chandra, S., Lata, H., Khan, I. A., ElSohly, M. A. — *Photosynthetic response of Cannabis sativa L. to variations in photosynthetic photon flux densities, temperature and CO₂ conditions.* Physiology and Molecular Biology of Plants, 2008.
- Rodriguez-Morrison, V., Llewellyn, D., & Zheng, Y. — *Cannabis Yield, Potency, and Leaf Photosynthesis Respond Differently to Increasing Light Levels in an Indoor Environment.* Frontiers in Plant Science, 2021.
- Magagnini, G., Grassi, G., Kotiranta, S. — *The Effect of Light Spectrum on the Morphology and Cannabinoid Content of Cannabis sativa L.* Medical Cannabis and Cannabinoids, 2018.
- Eichhorn Bilodeau, S., et al. — Greenhouse cannabis production research, photoperiod and environment interactions.

**Tier 2 — Manufacturer / industry technical:**
- Pulse Pro / Pulse Grow — published target ranges for cannabis VPD, temp, RH per stage.
- Quest Climate — commercial cannabis HVAC and dehumidification engineering.
- Anden / Aprilaire / Quest dehumidifier sizing calculators and AHAM derating guidance.
- Trolmaster, AC Infinity controller documentation — environmental targets per stage.
- Dimlux — VPD and cultivation environment guides.

**Tier 3 — Master growers / educators:**
- Cervantes, J. — *Cannabis Encyclopedia*, environment chapters.
- Rosenthal, E. — *Marijuana Grower's Handbook*, environment chapters.
- DeBacco University (YouTube) — Penn State horticulture lectures on cannabis environment.

## Cross-References

- PPFD targets and DLI calculations → `03-lighting.md`
- Calcium and boron deficiency from low transpiration → `07-deficiencies.md`
- Powdery mildew, botrytis prevention via RH/airflow → `09-disease.md`
- Spider mite environmental conditions → `08-pests.md`
- Stretch management via DIF → `12-flowering.md`
- Drying environment (extension of this file) → `14-drying.md`
- Curing humidity targets → `15-curing.md`
- Medium-specific irrigation that affects transpiration load → `04-medium-coco.md`, `04-medium-hydro.md`
- Stage transitions that force climate shifts → `12-flowering.md`
