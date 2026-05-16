# 19 — Tissue Culture

In vitro culture of cannabis tissue in sterile, hormone-controlled media. Used for mass propagation, disease elimination (HLVd recovery via meristem rescue), and long-term genetic preservation via cryopreservation. Most growers should not attempt TC — this file explains when it makes sense and what it actually requires.

This file is educational and safety-bounded for serious hobbyists considering specialist work. For routine legal home-grow cloning, cuttings remain the right answer. For HLVd recovery, this file pairs with disease detail in `09-disease.md`.

Cross-reference:
- HLVd biology and detection → `09-disease.md`
- Traditional cloning and mother management → `11-propagation.md`
- Breeding stock preservation context → `18-breeding.md`
- Operations hygiene and safe scaling boundaries → `20-commercial-ops.md`

## How to Use This File

1. Decide if TC fits your goals — most growers should NOT do TC
2. Read core concepts to understand what TC actually does (and doesn't do)
3. Match goal to stage protocol
4. Cost-check equipment and time before committing
5. For one-off needs (HLVd cleanup of one cultivar) — contract a service, don't build a lab

## Core Concept — What TC Is and What It Isn't

**TC IS:**
- A way to multiply identical plants from a single explant under sterile conditions
- A specialist pathway that can sometimes recover clean plants from infected valuable stock when paired with repeated testing
- A way to store genetics for years to decades (cold storage / cryopreservation)
- A way for specialist labs to multiply clean, tested stock at scale

**TC ISN'T:**
- A faster routine production method than cuttings (slower per cycle; scales differently)
- A genetic improvement (DNA is the same — TC cleans tissue, doesn't change the genome)
- An "alternative" to mother rooms for the average grow (overkill)
- Tolerant of skipped sterile technique — one slip ruins a run

## Core Concept — Sterile Technique

The single most important skill in TC. Without it, nothing else matters.

**Required infrastructure:**
- Laminar flow hood or validated sterile workspace appropriate to plant TC
- Autoclave for media and tools (15-20 min at 121°C / 15 psi)
- 70% ethanol for surface sterilization (workspace, gloves, vessel exteriors)
- Label-compatible disinfectants for explants/surfaces; concentrations and contact times must come from a vetted TC protocol/SDS
- Sterile gloves, mask, hairnet for serious work
- Tools sterilized between cuts by autoclave, sterile disposables, or another validated non-hazardous protocol; avoid open-flame alcohol handling unless trained/equipped

**Discipline:**
- Move deliberately, slow gestures over the work surface
- Never reach over open vessels
- Sterilize or replace tools between cuts using a validated protocol
- Pre-sterilize all vessel exteriors before opening
- Discard any vessel showing contamination immediately — quarantine to prevent spread to neighbors

The single biggest TC mistake is rushing. A run that takes one extra hour but no contamination is faster than three contaminated runs.

## Core Concept — Plant Hormones in TC

Hormone ratio determines what the tissue becomes. Cannabis is sensitive to specific cytokinin choice.

| Hormone class | Examples | Function | Cannabis-specific notes |
|---|---|---|---|
| Auxin | IAA, IBA, NAA, 2,4-D | Cell elongation, root initiation, callus | IBA for rooting; avoid 2,4-D in cannabis (heavy callus, somaclonal risk) |
| Cytokinin | BAP, kinetin, TDZ, mT | Cell division, shoot multiplication | **TDZ can cause hyperhydricity in cannabis — avoid as a default or use only in validated protocols.** mT (meta-Topolin) is commonly supported in cannabis TC literature |
| Gibberellin | GA3 | Cell elongation, dormancy break | Rare in cannabis TC |
| Abscisic acid | ABA | Stress response, dormancy | Used in cryopreservation prep |

**Auxin : cytokinin ratio determines tissue fate:**
- High auxin, low cytokinin → roots
- Low auxin, high cytokinin → shoots
- Balanced → callus (undifferentiated mass — generally avoid in cannabis; high somaclonal variation risk)

## STANDARD 4-STAGE PROTOCOL

### Stage 0 — Mother plant prep

- Healthy, vigorous mother under controlled environment
- Reduce contamination pressure with clean mother-plant care and pest/disease screening
- Time explant collection for active growth (young shoot tips)
- Avoid harsh bleach/alcohol treatments on live mother plants unless following a validated lab protocol

### Stage 1 — Initiation

- Excise nodal section (~1 cm) or shoot tip
- Surface-disinfect explants using a vetted TC protocol with appropriate PPE, sterile rinses, and chemical compatibility. Do not improvise bleach/alcohol recipes; scented/splash-less household products can damage tissue and add unknown residues.
- Place on initiation medium: MS basal + low cytokinin (mT 0.1-0.5 mg/L) + low or no auxin
- 2-4 weeks for shoot to emerge
- Expect high contamination losses in first attempts — this is normal

### Stage 2 — Multiplication

- Transfer surviving shoots to multiplication medium: MS + mT 0.5-1 mg/L
- Sub-culture every 3-6 weeks (cut shoots, replate on fresh medium)
- Each shoot generates 3-10 axillary shoots per cycle
- Monitor for: somaclonal variation, hyperhydricity, browning
- Cap subculture cycles (typically 6-10 max per line). After 6-10 cycles, somaclonal variation accumulates — point mutations, epigenetic drift, chromosomal abnormalities. Re-initiate from a fresh explant of the original mother to reset.

### Stage 3 — Rooting

- Transfer to rooting medium: low/no cytokinin + IBA 0.5-1 mg/L
- 2-3 weeks for visible roots
- Alternative: skip in vitro rooting and root ex vitro in sterile plug under high humidity

### Stage 4 — Acclimatization

- Most TC failures happen here. Plant has been in 100% humidity, sugar-fed, low light.
- Move to sterile potting medium under dome at 90%+ RH
- Gradual hardening over 2-4 weeks: progressively reduce humidity, increase light
- Once leaves develop normal cuticle and roots establish, treat as standard clone

## Media Composition

Standard cannabis TC uses **Murashige & Skoog (MS) basal medium**:

| Component | Typical concentration | Role |
|---|---|---|
| MS macronutrients | full or half strength | N, P, K, Ca, Mg, S |
| MS micronutrients | full strength | Fe, Mn, Zn, B, Cu, Mo |
| MS vitamins | full (myo-inositol, thiamine, nicotinic acid, pyridoxine) | Cofactors |
| Sucrose | 20-30 g/L | Energy — TC plants don't fully photosynthesize |
| Agar | 6-8 g/L | Semi-solid matrix |
| pH | 5.7-5.8 (before autoclave) | Optimal nutrient availability |
| Hormones | per stage | See hormone table |
| Activated charcoal | 0.5-2 g/L (optional) | Absorbs phenolics in cannabis |

DKW or B5 base media also occasionally used; MS is overwhelmingly standard for cannabis.

## MERISTEM RESCUE (HLVd Recovery)

The highest-value use case for TC in cannabis is clean-stock recovery. HLVd distribution can be lower or absent in tiny meristematic tissue, so specialist meristem culture plus repeated testing can sometimes recover a clean plant.

### Process

1. Take healthy-looking shoot tip from HLVd+ mother
2. Surface-disinfect explants with a validated protocol and PPE
3. Under a stereo microscope, dissect away surrounding tissue as required by the protocol
4. Excise a very small meristem/explant; smaller cuts may clean better but survive worse
5. Plate on initiation medium
6. Grow out for 4-8 weeks
7. Test resulting plant via RT-qPCR or another validated lab assay for HLVd
8. If repeatedly clean → multiply cautiously and keep quarantine until status is confirmed
9. If positive → repeat with smaller meristem cut

### Success rates and reality

- Skilled operators may recover clean plants, but success varies widely by cultivar, protocol, and infection status
- Smaller meristem/explant cuts often improve cleaning odds but reduce survival
- Multiple attempts often needed for resistant cultivars
- Some cultivars are easier (apparently due to anatomical differences in meristem invasion)

### Cost reality

- Specialist meristem rescue service: often hundreds to thousands per cultivar attempt, results not guaranteed
- DIY: thousands in equipment + months of learning, plus per-attempt failure rate
- For one or two cultivars, contract a reputable service; build a lab only if the learning curve, safety, and cost are justified

## CRYOPRESERVATION

Liquid nitrogen storage of meristem tissue at -196°C. Indefinite storage with negligible drift.

### Why use it

- Backup against catastrophic mom room loss
- Decade+ preservation of breeding stock (heirloom, landrace, IBL)
- Industry use: maintain cultivars without active mother rooms
- Safety net for HLVd-cleaned lines (re-contamination becomes recoverable)

### Process (advanced — research-lab-grade work)

1. Prepare clean source material under a validated protocol
2. Excise meristem/explant material in sterile conditions
3. Use cryoprotectant/loading/vitrification steps from peer-reviewed or lab protocols
4. Store in liquid nitrogen using proper cryogenic PPE and facility procedures
5. Recover and re-test material before relying on it

Cannabis-specific cryopreservation protocols are still being optimized. Recovery varies by cultivar and lab; plan for losses.

## EQUIPMENT (Realistic Costs)

| Equipment | Use | Approx cost |
|---|---|---|
| Laminar flow hood | Sterile work | $1500-5000 |
| Autoclave | Sterilization (media, tools) | $1000-5000 (used to large) |
| Stereo microscope | Meristem dissection | $300-2000 |
| pH meter (lab grade) | Media prep | $100-300 |
| Magnetic stirrer + hot plate | Media prep | $150-500 |
| Analytical balance (mg accuracy) | Hormone weighing | $200-1000 |
| Scalpels, forceps, dishes | Consumables | $200/yr+ |
| MS media powder | Media base | $50-200/kg |
| Hormones (mT, IBA, BAP) | Per stage | $100-500 each |
| Culture vessels (Magenta jars, plates) | Containers | $300-1000 starter |
| Growth room/cabinet w/ light | TC plant culture | $500-3000 |
| LN2 dewar | Cryopreservation | $1000-5000 |

**Realistic startup for serious hobbyist:** $5000-15000 + 6+ months learning curve before consistent results.
**Dedicated professional lab:** $50k-500k+ depending on throughput.

## COMMON PROBLEMS

| Problem | Cause | Fix |
|---|---|---|
| Mold/bacterial contamination | Sterile technique failure | Discard infected, audit technique step-by-step |
| Hyperhydricity (glassy, water-logged shoots) | TDZ overuse, high cytokinin, low agar | Switch to mT, reduce cytokinin, increase agar to 8 g/L |
| Phenolic browning (tissue darkens, dies) | Cannabis is high in phenolics; oxidation | Add activated charcoal, ascorbic acid in medium, transfer often |
| No multiplication | Cytokinin too low | Increase mT 0.2 mg/L step at a time |
| No rooting | Auxin too low or too high | Adjust IBA 0.1-2 mg/L; sometimes auxin pulse-dip works better than continuous |
| Vitrification when transferring out | Sudden humidity drop | Slower acclimatization, dome covers, gradual RH reduction over 2-4 weeks |
| Somaclonal variation (DNA changes from culture) | Long subculture history, callus phase, high cytokinin | Avoid callus phase, limit subculture cycles, refresh from new explant periodically |
| Loss of vigor over years | Cumulative culture stress | Re-initiate from a fresh explant of the same genetics |
| Endophytic bacterial bloom (bacteria from inside the plant emerge in vitro) | Mother carried internal bacteria | Antibiotic-supplemented media, or restart from a different mother of same genetics |

## TC vs TRADITIONAL CLONING

| Factor | Tissue Culture | Cuttings |
|---|---|---|
| Time per cycle | 2-6 weeks per stage | 1-2 weeks total |
| Setup cost | $5k-500k+ | $50-200 |
| Skill barrier | High (months to years) | Low (weeks) |
| Genetic stability long-term | Excellent (esp. cryo) | Moderate (mom drift, disease accumulation) |
| Disease cleaning | Yes (meristem rescue) | No |
| Routine production efficiency | Low | High |
| Scaling | Exponential at multiplication stage | Linear (limited by mom plants) |
| Storage between uses | Cold storage / cryo | Mom must stay alive |
| Failure mode | Contamination wipes whole batch | One bad cut, one lost cutting |

**Use TC when:** specialist clean-stock recovery, valuable genetics preservation, or breeding stock backup justify the cost and safety requirements.
**Use cuttings for:** everything else.

## DECISION TREE

```
WHY TISSUE CULTURE?

→ HLVd-positive line you want to save
   ├── One or two cultivars → CONTRACT meristem rescue service ($500-2500/line)
   └── Ongoing program → build in-house TC lab

→ Long-term backup of breeding stock (heirloom, landrace, IBL)
   └── CRYOPRESERVATION (advanced; consider partnering with research lab)

→ Clean-stock multiplication beyond normal home cloning
   └── Contract with an established TC nursery/lab unless you have real lab capability

→ Just want clones for your home grow
   └── DON'T do TC. Use cuttings (see 11-propagation.md)

→ Research / curiosity / learning
   └── Start with non-cannabis practice material or kits, use PPE/SDS, and expect months of contaminated plates before consistent runs
```

## CONFUSION TRAPS

| Belief | Reality |
|---|---|
| "TC produces stronger plants" | Same genetics. Vigor benefit comes from removing systemic disease (HLVd, viruses), not from TC itself. |
| "TC is faster than cuttings" | Slower per cycle. Scales differently — exponential multiplication can outpace cuttings only at large scale. |
| "Meristem rescue always works" | Success varies widely. Often takes multiple tries and repeated testing; not guaranteed clean. |
| "Anyone can do TC at home" | Possible to learn, but sterile technique, chemical safety, equipment cost, and months of failed runs are typical barriers. |
| "Cryopreserved plants pop right back" | 30-60% recovery rate even in pro labs. Plan for losses. |
| "Hyperhydricity is just bad genetics" | Almost always TDZ overuse or media issue, fixable. |
| "TC clones don't drift like mom-room clones" | Less drift, but somaclonal variation is real with high cytokinin or callus phase. Limit cycles. |
| "Tissue culture purifies the strain" | TC removes pathogens; it does NOT change the underlying genome. Same DNA as the source. |
| "TC plants from a service are guaranteed clean" | Reputable services test post-rescue; ask for COA / RT-qPCR results. Don't assume. |
| "All cytokinins work equally" | False. TDZ is famously problematic in cannabis (hyperhydricity). mT is the cannabis-validated choice. |

## SOURCES

**Tier 1 — Peer-reviewed:**
- Lata, H. et al. (2009) — *In Vitro Cellular & Developmental Biology - Plant* — first reproducible cannabis micropropagation protocol with mT cytokinin
- Page, S. R. G., Monthony, A. S., Jones, A. M. P. (2021) — *Plant Cell, Tissue and Organ Culture* — meta-Topolin (mT) outperforms TDZ in cannabis; reduces hyperhydricity
- Monthony, A. S. et al. (2021) — *Plants* — comprehensive review of cannabis micropropagation systems and recurring challenges
- Adhikary, D. et al. (2021) — *Plants* — cannabis tissue culture review with somaclonal variation and stability discussion
- Wróbel, T. et al. (2020) — *South African Journal of Botany* — meristem culture protocols and viroid elimination considerations
- Uchendu, E. E. et al. (2019) — *In Vitro Cellular & Developmental Biology - Plant* — cryopreservation protocols for cannabis germplasm via droplet vitrification
- Warren, J. G. et al. (2019) — *Plant Disease* — HLVd in cannabis and rationale for meristem-based elimination

**Tier 2 — Labs / suppliers:**
- Dark Heart Nursery — HLVd elimination protocols, clean stock standards
- Front Range Biosciences — cannabis tissue culture industry guides
- Phylos Bioscience — clean stock production methodology
- PhytoTech Labs — MS media, hormone supply, technical bulletins
- Caisson Labs — plant tissue culture supplies and reference protocols

**Tier 3 — Master practitioners and educators:**
- Caplan lab (Guelph, Andrew Maxwell Phineas Jones group) — extension content for cannabis TC
- *Cannabis Tissue Culture* (book — practical-grower-focused content; cross-confirm hormone ratios with peer-reviewed)
- DeBacco University TC lectures
- Industry conferences (Emerald Conference, CannMed) — TC sessions

**Tier 4 — Community consensus (cross-confirm before applying):**
- /r/CannabisTissueCulture, ICmag TC subforum

## CROSS-REFERENCES

- HLVd biology, detection, prevention → `09-disease.md`
- Mother management and traditional cuttings → `11-propagation.md`
- Breeding stock preservation rationale → `18-breeding.md`
- Operations hygiene / safe scaling boundaries → `20-commercial-ops.md`
- Sterile-technique principles cross-applicable to → `08-pests.md` (quarantine), `09-disease.md` (sanitation)
