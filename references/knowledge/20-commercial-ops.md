# 20 — Commercial Operations

How cannabis cultivation changes when scaled to commercial production. Covers facility design, biosecurity zones, SOP construction, compliance and tracking (METRC), HVAC and lighting economics, IPM at scale, yield benchmarks, OPEX structure, labor formalization, and the failure modes that separate viable operations from collapsing ones.

This is a strategic primer, not a turnkey blueprint. Regulations and CAPEX vary heavily by jurisdiction. Specific cultivation techniques covered here at scale-context only — pair with the relevant knowledge file for technique detail.

Cross-reference:
- HVAC and climate fundamentals → `02-environment.md`
- Lighting → `03-lighting.md`
- IPM and disease at scale → `08-pests.md`, `09-disease.md`
- HLVd testing programs → `09-disease.md`, `19-tissue-culture.md`
- Mother room and clone management → `11-propagation.md`
- Dry/cure/trim throughput → `14-drying.md`, `15-curing.md`, `16-trimming.md`
- Extraction operations → `17-extraction-basics.md`
- Breeding stock at scale → `18-breeding.md`, `19-tissue-culture.md`

## How to Use This File

1. Identify your scale tier from the table below (craft / small / mid / large / outdoor)
2. Match scale to facility model and SOP requirements
3. Use cost framework to model your specific market
4. Cross-reference with technique files for cultivation specifics
5. Use this file's failure-modes table as a pre-mortem before scaling up

## Core Concept — Scale Tiers

Different scales have different problems and different unlocks. Operating like a craft grow at industrial scale (or vice versa) destroys margins.

| Tier | Canopy | Plants/cycle | Annual production | Typical CAPEX | Typical staff |
|---|---|---|---|---|---|
| Craft / micro | <500 sqft | 50-200 | 100-500 lbs | $50k-300k | 1-3 |
| Small commercial | 500-2500 sqft | 200-1000 | 500-2500 lbs | $300k-1.5M | 3-10 |
| Mid commercial | 2500-10000 sqft | 1000-5000 | 2500-10k lbs | $1.5M-10M | 10-50 |
| Large industrial | 10000+ sqft | 5000+ | 10k+ lbs | $10M+ | 50-500 |
| Outdoor light-dep | acres | thousands | wildly variable | $500k-10M | seasonal scaling |

## Core Concept — What Changes at Scale

Hobby-grow problems become catastrophic at scale. In return, scale unlocks options unavailable to small operations.

**What gets harder:**
- Pest outbreaks spread fast — one PM patch in week 6 can collapse an entire flower room
- Genetic drift — a mom room of 50 plants drifts more than 5; one infected mom contaminates hundreds of clones before symptoms show
- Climate uniformity — dead zones and microclimates appear within rooms past ~25 ft
- Labor errors compound — uncalibrated pH meter or wrong feed batch hits hundreds of plants before catching
- Drying and trim bottlenecks — undersized post-harvest pipeline strands hundreds of pounds in dry rooms
- Compliance overhead — every gram traceable, every movement logged
- Energy and water are higher % of OPEX than expected

**What unlocks:**
- Lab testing budget (routine pesticide screen, HLVd RT-qPCR, COA per batch)
- Specialized labor (head grower, IPM specialist, post-harvest manager)
- Volume nutrient pricing (Athena, Canna, Jacks drop 30%+ at bulk)
- In-house genetics programs (TC, breeding, clean stock)
- Branded distribution channels
- Redundant systems (HVAC N+1, mom backups, generators)

---

## FACILITY DESIGN

### One-way workflow

Plants flow in one direction; cross-contamination risk drops. No backflow from "dirty" zones (flower, harvest) to "clean" (mom, clone, veg).

```
Genetics intake (quarantine 4+ wk, HLVd test)
    ↓
Mother room (clean zone, biosecurity-strict)
    ↓
Clone / propagation (enclosed, high RH)
    ↓
Veg rooms (multiple, staggered)
    ↓
Flower rooms (multiple, staggered for perpetual harvest)
    ↓
Harvest room (transient, sanitized between batches)
    ↓
Dry rooms (separate, climate-controlled)
    ↓
Cure / vault (long-term storage)
    ↓
Trim / processing (separate, sanitized)
    ↓
Packaging / vault
    ↓
Outbound shipping
```

### Biosecurity zones

- **Clean zone:** mom, clone, veg — strict entry, change protocols, dedicated PPE
- **Dirty zone:** flower, harvest, processing — less strict but still one-way flow
- No staff backflow from dirty → clean within a shift (or change clothes/shoes)
- Foot baths and hand wash stations between zones
- Some operations: dedicated coveralls or scrubs per zone

### Per-room specs (flower room)

- Sealed (CO2 supplementation viable; required for sealed-room economics)
- HVAC sized for peak heat + dehumidification + CO2 + N+1 redundancy
- Even airflow — no dead spots; vertical air movers + horizontal canopy circulation
- Sensor coverage: 3+ temp/RH points per room, central VPD calculation
- Backup generator or UPS for at least lights + HVAC during transitions
- Watertight floors, drainage, easy-clean walls (FRP panels, sealed concrete)
- Anteroom or airlock for higher-biosecurity rooms (mom especially)

### Cultivation systems

| System | Best for | Pros | Cons |
|---|---|---|---|
| Coco in pots, hand-water | Craft, single-batch quality focus | Low CAPEX, flexible | Labor-intensive |
| Coco fertigation drip | Mid commercial | Automated feed, consistent | Plumbing complexity, monitoring needs |
| Rockwool slabs (hydroponic) | Mid-large | Standardized, predictable inputs | Disposal cost, vendor lock-in |
| Living soil beds (no-till) | Craft to small-mid | Quality, low ongoing input | Slow turnaround, harder pest control |
| DWC / RDWC | Mid commercial | Fast growth, no medium cost | Single-point failure (root rot cascade) |
| Aeroponic | Specialty / R&D | Fast growth, low water | Complex, failure cascades fast |
| Vertical multi-tier | Large with ceiling height | 2-3x yield/sqft | Complex HVAC, lighting heat layering |
| Greenhouse light-dep | Mass production | Lowest cost/g, partial sun | Weather risk, slower swap cycles |

---

## SOPs (Standard Operating Procedures)

A commercial operation runs on documented procedures, not on the head grower's memory. Every recurring task gets an SOP.

### Minimum SOP set

1. Mother plant maintenance (feeding, pruning, IPM scouting)
2. Cloning protocol (cut, root, transfer schedule)
3. Veg transition checklist
4. Flower flip checklist
5. Daily room walk-through (what to inspect, log fields)
6. Feed mixing protocol (mix order, EC verify, pH verify, batch logging)
7. IPM scout schedule (zones, frequency, what to record)
8. Harvest workflow (cutting, hanging, room sanitization between batches)
9. Drying environment management (RH, temp, days, RH curve)
10. Curing protocol (jar/bin schedule, burping/circulation, target Aw)
11. Trim line workflow (machine vs hand, QC checkpoints)
12. Packaging and weighing (compliance + waste accounting)
13. Sanitization between cycles (room turnover protocol)
14. Pest outbreak response (quarantine, treatment, escalation, communication)
15. HLVd testing schedule (mom stock, intake quarantine, periodic)
16. Equipment calibration (pH/EC meters, room sensors, scales)
17. Emergency response (power outage, HVAC fail, flood, fire)
18. Visitor / contractor entry (biosecurity)
19. Inventory and METRC compliance
20. Training and onboarding new staff

### Per-SOP structure

- Title + version + date + author
- Purpose and scope (when this SOP applies)
- Required materials / PPE
- Step-by-step procedure (numbered, atomic)
- Decision points / what to do if X
- Documentation/logging required
- Escalation path (when to call manager)
- Review schedule (annual minimum, triggered by failure)

---

## COMPLIANCE AND TRACKING

Most US legal markets require track-and-trace via **METRC** (or BioTrack, Leaf Data — varies by state). Canada: Health Canada CTLS. Germany: BfArM tracking. Markets vary; baseline functions are universal.

### Universal compliance functions

- Plant tagging — every plant from sprout/clone to sale, RFID or barcode
- Waste log — destroyed material weighed, witnessed, recorded
- Movement records — room transfers, inventory shifts, sale movements
- Sale records — invoice, weights, batch numbers, customer
- Test results upload — COA per batch
- Periodic inventory audits — state may inspect with or without notice
- Security camera retention — typically 30-90 days, sometimes longer

### Testing requirements (typical, varies by state/country)

- Cannabinoid profile (THC, CBD, often full panel)
- Terpene profile (often optional, increasingly required)
- Pesticide panel (state-specific list, ppm limits)
- Heavy metals (As, Cd, Pb, Hg)
- Microbials (TYM = total yeast/mold; sometimes E. coli, Salmonella, Aspergillus species)
- Mycotoxins (aflatoxin, ochratoxin)
- Residual solvents (extracts only)
- Water activity / moisture content
- Foreign matter

Failure outcomes: re-test, remediation (irradiation/ozone/X-ray in some states), or destruction. Build sample retention and re-test budget into operating model.

---

## CLIMATE AT SCALE

### HVAC sizing rules of thumb

- **Heat load:** every watt of input becomes heat (3.412 BTU/hr/W is the W→BTU conversion). Total heat = lighting wattage + pump/fan motor wattage. Of this, ~30-50% becomes latent (moisture) load via transpiration in late flower; the rest is sensible. Size HVAC for both.
- **Transpiration:** flower canopy moves ~1 pint water/day/sqft at peak
- **Sensible vs latent split:** flowering cannabis is HIGH latent load (moisture-heavy)
- **Sealed room:** precise control but full HVAC + dehumidification + CO2 system required
- **Mini-splits** scale poorly past 4-5 ton total — commercial chillers + fan coils for serious operations
- **Redundancy:** minimum N+1 (one extra unit can fail without losing the room)

### Dehumidification (most underspec'd system)

- Whole-room industrial dehumidifiers (Quest 506, Anden A710, Desert Aire) sized to peak flower load
- OR chilled water systems with reheat coils for combined heat/moisture management
- Without proper dehumidification → mold, PM, botrytis at flower week 4+
- Common rookie error: spec dehumidification for veg/early flower, then crash in late flower

### CO2

- Worth supplementing only in sealed rooms (otherwise leaks out)
- Target 800-1500 ppm in flower; diminishing returns past ~1500 ppm at high light intensity (Chandra et al., Bugbee work). 1200 ppm is the practical economic sweet spot — past that, gas cost outpaces yield gain in most markets.
- **Burner** (LP/NG combustion) — heat byproduct, useful in cool climates
- **Tank** — clean, no heat, expensive at scale
- Monitor + alarm — CO2 above 5000 ppm = human safety risk

---

## LIGHTING AT SCALE

### LED vs HPS economics (~2024-2026)

- **LED:** higher CAPEX, 40-50% less power for same PPFD, less heat (reduces HVAC load)
- **HPS:** lower CAPEX, easy to find used, more heat (useful in cold climates as heating)
- LED quality varies enormously — top tier (Fluence, Gavita LED, Sananbio, Photontek) vs cheap imports (often misrated PPFD)
- Crossover point: at $0.10-0.15/kWh, LED payback ~24-36 months. Below $0.08/kWh, payback can stretch past 5 years. Above $0.18/kWh, payback under 18 months. Run the math for your specific rate before deciding.

### PPFD targets (commercial-validated, Bugbee/Caplan)

- **Veg:** 400-600 µmol/m²/s
- **Flower:** 800-1200 µmol/m²/s standard; with CO2 enrichment can push 1500+
- Diminishing returns past 1500 PPFD without CO2 → no extra yield, more bleaching/heat damage

### Greenhouse light-dep

- Blackout schedule for flower trigger (12/12)
- Supplemental HPS or LED for low-light months
- Highest dollar/watt efficiency in mild climates with strong winter sun

---

## YIELD BENCHMARKS (Indoor, Commercial)

| Quality tier | Per sqft canopy | Per kW lighting |
|---|---|---|
| Beginner commercial | 30-40 g/sqft | 0.6-0.8 g/W |
| Solid commercial | 40-50 g/sqft | 0.8-1.0 g/W |
| Top tier | 50-65 g/sqft | 1.0-1.4 g/W |
| Reported best (rare, peer-validated) | 70+ g/sqft | 1.5+ g/W |

Per-sqft assumes ~50 W/sqft lighting and properly trained canopy. Outdoor yields wildly variable: 0.5-3 lbs/plant in moderate climate, more in prime conditions.

---

## ECONOMICS

### OPEX category breakdown (typical indoor commercial)

| Category | % of OPEX |
|---|---|
| Labor | 30-45% |
| Energy (electricity, gas) | 15-25% |
| Nutrients + media | 5-10% |
| Genetics / clones | 2-5% |
| Compliance / testing | 3-8% |
| Pest management | 2-5% |
| Packaging + supplies | 5-10% |
| Rent / mortgage | 10-20% |
| Other (insurance, banking, security) | 5-10% |

### Production cost benchmarks (USD per pound dry, ~2024-2026)

| Production type | Cost/lb |
|---|---|
| Outdoor light-dep, well-run | $100-300 |
| Greenhouse, mid-scale | $300-600 |
| Indoor, large efficient | $500-900 |
| Indoor, small craft | $1000-2000 |

California has compressed to $400-1200/lb at typical quality with periods below $400 during oversupply cycles 2022-2024; emerging markets often $1500-3000+/lb. Margin compression dominates mature markets — operations without top-quality + cost-discipline don't survive.

---

## LABOR AT SCALE

### Roles to formalize past ~10 employees

- Head Grower / Cultivation Manager
- Assistant Growers (per room or zone)
- IPM Specialist
- Post-Harvest Manager (dry, cure, trim)
- Trim Lead
- Compliance Officer
- Maintenance / Facilities
- Quality Control / Lab Liaison

### Training discipline

- New employees shadow before solo task
- SOP-based training, not "tribal knowledge"
- Quarterly cross-training so no single point of failure in any role
- Document who is certified for which SOP
- Annual review against compliance audits

---

## QUALITY CONTROL

- **In-house:** pH/EC for feed, water activity (Aw) meter for cure, weight scales for inventory
- **Outsourced:** full panel test per batch via state-licensed lab
- **Visual QC** at intake, transfer, harvest, post-cure, packaging
- **Trim grades** (A, B, C — different distribution channels and pricing)
- **Smell QC** at packaging (off-aromas indicate cure or contamination issue)
- **Sample retention:** minimum 90 days, often 1 year; per-batch shelf samples for retroactive testing if a problem emerges

---

## COMMON COMMERCIAL FAILURES

| Failure mode | Cause | Prevention |
|---|---|---|
| HLVd outbreak destroys mom stock | Skipped intake testing | RT-qPCR on all incoming genetics, 4+ wk quarantine |
| Botrytis sweep through flower week 5+ | Underspec'd dehumidification | Size dehumid for peak flower load (2x veg) |
| PM appears week 4, infects whole room | Late detection, no IPM scouting cadence | Daily/weekly canopy inspection SOP, scout log |
| Crop fails pesticide panel | Cross-contamination (drift, residue, supplier) | Document every spray, test approved-product list, supplier audit |
| Yields drop 30% over 18 months | Genetic drift in mom room, accumulating disease load | Refresh moms via TC or test-clean reference seeds |
| Energy bills 50% higher than projected | HVAC undersizing, inefficient lights, leaky envelope | MEP engineer for facility design, don't DIY past craft tier |
| Labor cost runs up | No SOPs, redoing tasks, bad training | Build SOP library before scaling staff |
| Compliance violation / shutdown | Bad METRC tracking, missing tags | Compliance officer, weekly internal audit |
| Backup grower quits, no one knows the system | Knowledge concentrated in one person | Document everything, cross-train, rotate |
| Trim bottleneck strands 200 lbs in dry rooms | Drying/trim throughput < flower harvest cadence | Match dry/trim capacity to flower output before scaling flower |
| Wholesale price drops 40%, can't reduce cost | Optimization deferred to "later" | Continuous cost reviews, never run lean-only on growth assumption |
| Aspergillus failure on TYM panel | Cure room or storage RH too high (Aw>0.65) | Aw meter, target 0.55-0.62 for cured flower storage |

---

## DECISION TREE — SCALING UP

```
WHERE ARE YOU NOW?

→ Hobby grow → first commercial license
   ├── Start craft tier (<500 sqft)
   ├── DON'T over-invest CAPEX before proving production
   └── Build SOPs from day 1, even if running solo

→ Craft → small commercial (500 → 2500 sqft)
   ├── Hire head grower if not already
   ├── HVAC and dehumidification redesign mandatory
   ├── Formalize SOPs and training docs
   └── Add HLVd testing + intake quarantine

→ Small → mid commercial (2500 → 10000 sqft)
   ├── MEP engineering required for HVAC/electrical
   ├── Dedicated compliance officer
   ├── Specialized roles (IPM, post-harvest, trim lead)
   ├── Standardize cultivation system (rockwool, fertigation, etc.)
   └── Lab partnership for routine testing

→ Mid → large industrial (10000+ sqft)
   ├── Engineering firm + cultivation consultant
   ├── Multi-room perpetual harvest cadence
   ├── In-house TC / clean stock program
   ├── Distribution and brand strategy
   └── Continuous cost-engineering, not one-time CAPEX

→ Indoor → outdoor / greenhouse expansion
   ├── Different skillset; consult outdoor experts
   ├── Light-dep schedule + blackout systems
   ├── Different IPM approach (broader pest pressure)
   └── Weather contingency planning
```

---

## CONFUSION TRAPS

| Belief | Reality |
|---|---|
| "Bigger HVAC means safer climate" | Oversized HVAC short-cycles, fails to dehumidify properly. Right-size with 10-20% headroom, not 100%+. |
| "LEDs run cool so HVAC can be smaller" | LEDs reduce sensible heat, not latent (transpiration moisture). Dehumid still needs full sizing. |
| "We can train staff on the job" | Possible but creates compounding errors. SOPs + structured training = profit margin. |
| "Once we scale we'll fix the problems" | Problems multiply with scale. Fix at small first or carry the bug into bigger rooms. |
| "Top genetics = top profit" | Genetics is necessary, not sufficient. Cost-engineering and consistency drive margin. |
| "Pesticide-free is automatic if we don't spray" | Cross-contamination from neighboring grows, water source, or staff residues. Test, don't assume. |
| "The market will reward the highest quality" | Mature markets compress prices. High quality + competitive cost both required. |
| "We can clean up METRC errors later" | Compliance retrofitting costs more than doing it right. Don't accumulate compliance debt. |
| "Vertical farming is automatically more efficient" | Sometimes, in expensive real estate. Otherwise added complexity > yield/sqft savings. |
| "Outdoor is just weed in dirt" | Modern outdoor light-dep is precision agriculture with weather risk; not casual. |
| "Insurance covers crop loss" | Most cannabis policies exclude crop or have crippling deductibles. Read the policy. |
| "We don't need an IPM specialist until we have a problem" | By the time a generalist sees the problem, infestation is established. Specialist prevents, doesn't react. |

---

## SOURCES

**Tier 1 — Peer-reviewed:**
- Caplan, D. et al. (2017) — *HortScience* — fertilizer rates for indoor cannabis (foundational for fertigation design at scale)
- Rodriguez-Morrison, V. et al. (2021) — *Frontiers in Plant Science* — high light intensity yield response with CO2 supplementation; defines diminishing-returns thresholds
- Eichhorn Bilodeau, S. et al. (2019) — *Frontiers in Plant Science* — review of commercial cannabis lighting including LED economics
- Mills, E. (2012) — *Energy Policy* — energy use of indoor cannabis; foundational reference for HVAC and lighting economics
- Vanhove, W., Van Damme, P., Meert, N. (2011) — *Forensic Science International* — yield potential and economic analysis of indoor cultivation
- Eaves, J. and Eaves, S. (2018) — *Canadian Journal of Agricultural Economics* — economics of cannabis production and pricing dynamics
- Punja, Z. K. et al. (2019) — *Frontiers in Plant Science* — review of cannabis pathogens at commercial scale, including Botrytis and Fusarium

**Tier 2 — Industry / manufacturer:**
- Athena Pro commercial fertigation white papers
- Quest Dehumidifiers / Anden technical sizing guides
- Fluence / Gavita / HLG PPFD design tools for commercial canopies
- METRC compliance documentation (state-specific)
- Resource Innovation Institute (RII) — facility energy benchmarking and best-practice guides
- Authority Having Jurisdiction (AHJ) inspection checklists per state

**Tier 3 — Master practitioners / consultants:**
- Allison Justice (The Hemp Mine, formerly Outco) — commercial cultivation operations writing
- Ryan Douglas — facility design consultant content
- Cannabis Business Times — operational case studies
- Marijuana Venture — commercial economics and facility writing
- Mr. Canucks Grow — commercial-scale technique content
- Greg Mohr — commercial grower educator

**Tier 4 — Community consensus (cross-confirm before applying):**
- ICmag commercial section, Cannabis Industry Journal forums

---

## CROSS-REFERENCES

- HVAC, VPD, climate fundamentals → `02-environment.md`
- PPFD, DLI, spectrum specs → `03-lighting.md`
- Pest scouting and IPM at scale → `08-pests.md`
- Disease pressure at scale (HLVd, Botrytis, Fusarium, PM) → `09-disease.md`
- Mother room and clone production → `11-propagation.md`
- Drying/curing throughput sizing → `14-drying.md`, `15-curing.md`
- Trim room layout and throughput → `16-trimming.md`
- Extraction operations and licensing → `17-extraction-basics.md`
- Breeding stock at scale → `18-breeding.md`
- TC and clean-stock programs → `19-tissue-culture.md`
