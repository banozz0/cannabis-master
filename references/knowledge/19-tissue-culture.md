# 19 — Tissue Culture

In vitro culture of cannabis tissue in sterile, hormone-controlled media. Used for mass propagation, disease elimination (HLVd recovery via meristem rescue), and long-term genetic preservation via cryopreservation. Most growers should not attempt TC — this file explains when it makes sense and what it actually requires.

This file is operational for serious hobbyists and small labs. For routine clone production, cuttings remain the right answer. For HLVd recovery, this file pairs with disease detail in `09-disease.md`.

Cross-reference:
- HLVd biology and detection → `09-disease.md`
- Traditional cloning and mother management → `11-propagation.md`
- Breeding stock preservation context → `18-breeding.md`
- Commercial-scale considerations → `20-commercial-ops.md`

## How to Use This File

1. Decide if TC fits your goals — most growers should NOT do TC
2. Read core concepts to understand what TC actually does (and doesn't do)
3. Match goal to stage protocol
4. Cost-check equipment and time before committing
5. For one-off needs (HLVd cleanup of one cultivar) — contract a service, don't build a lab

## Core Concept — What TC Is and What It Isn't

**TC IS:**
- A way to multiply identical plants from a single explant under sterile conditions
- The ONLY reliable way to eliminate viroids (HLVd) and most viruses from infected stock
- A way to store genetics for years to decades (cold storage / cryopreservation)
- A way to produce thousands of clean clones from one source

**TC ISN'T:**
- A faster routine production method than cuttings (slower per cycle; scales differently)
- A genetic improvement (DNA is the same — TC cleans tissue, doesn't change the genome)
- An "alternative" to mother rooms for the average grow (overkill)
- Tolerant of skipped sterile technique — one slip ruins a run

## Core Concept — Sterile Technique

The single most important skill in TC. Without it, nothing else matters.

**Required infrastructure:**
- Laminar flow hood (HEPA-filtered downflow over work surface)
- Autoclave for media and tools (15-20 min at 121°C / 15 psi)
- 70% ethanol for surface sterilization (workspace, gloves, vessel exteriors)
- Bleach (10-20% for explant sterilization; 10% for work surfaces)
- Sterile gloves, mask, hairnet for serious work
- Tools sterilized between cuts: autoclave or flame-dip in 95% ethanol

**Discipline:**
- Move deliberately, slow gestures over the work surface
- Never reach over open vessels
- Flame-sterilize tools between every cut
- Pre-sterilize all vessel exteriors before opening
- Discard any vessel showing contamination immediately — quarantine to prevent spread to neighbors

The single biggest TC mistake is rushing. A run that takes one extra hour but no contamination is faster than three contaminated runs.

## Core Concept — Plant Hormones in TC

Hormone ratio determines what the tissue becomes. Cannabis is sensitive to specific cytokinin choice.

| Hormone class | Examples | Function | Cannabis-specific notes |
|---|---|---|---|
| Auxin | IAA, IBA, NAA, 2,4-D | Cell elongation, root initiation, callus | IBA for rooting; avoid 2,4-D in cannabis (heavy callus, somaclonal risk) |
| Cytokinin | BAP, kinetin, TDZ, mT | Cell division, shoot multiplication | **TDZ causes hyperhydricity in cannabis — avoid or low dose only.** mT (meta-Topolin) is the modern cannabis standard |
| Gibberellin | GA3 | Cell elongation, dormancy break | Rare in cannabis TC |
| Abscisic acid | ABA | Stress response, dormancy | Used in cryopreservation prep |

**Auxin : cytokinin ratio determines tissue fate:**
- High auxin, low cytokinin → roots
- Low auxin, high cytokinin → shoots
- Balanced → callus (undifferentiated mass — generally avoid in cannabis; high somaclonal variation risk)

## STANDARD 4-STAGE PROTOCOL

### Stage 0 — Mother plant prep

- Healthy, vigorous mother under controlled environment
- Reduce systemic contamination (clean leaves, possibly antifungal pre-treatment)
- Time explant collection for active growth (2-4 week-old shoot tips)
- Multi-day surface clean before excision (bleach foliar, alcohol wipe daily)

### Stage 1 — Initiation

- Excise nodal section (~1 cm) or shoot tip
- Surface sterilize: 70% ethanol 30s → 10-20% bleach 10-15 min → triple sterile water rinse. Use plain sodium hypochlorite bleach only — splash-less, scented, or "thick" bleach contains surfactants that damage tissue. Add 1-2 drops Tween-20 per 100ml bleach solution as wetting agent.
- Place on initiation medium: MS basal + low cytokinin (mT 0.1-0.5 mg/L) + low or no auxin
- 2-4 weeks for shoot to emerge
- Expect 50-90% contamination losses in first attempts — this is normal

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

The killer use case for TC in cannabis. HLVd lives in vascular tissue but does not consistently invade the meristematic dome (the actively dividing apex of the shoot tip). Excising just the meristem can produce a viroid-free plant.

### Process

1. Take healthy-looking shoot tip from HLVd+ mother
2. Aggressive surface sterilization (70% ethanol → 15-20% bleach → triple rinse)
3. Under stereo microscope at 40-80x magnification, dissect off ALL leaf primordia
4. Excise the meristematic dome — visible as small bright translucent dome, ~0.2-0.5 mm
5. Plate on initiation medium
6. Grow out for 4-8 weeks
7. Test resulting plant via RT-qPCR for HLVd at certified lab
8. If clean → multiply via Stage 2 → use as new clean mother stock
9. If positive → repeat with smaller meristem cut

### Success rates and reality

- Skilled operator: 30-70% clean plants per attempt
- Smaller meristem cut = higher clean rate, lower survival rate
- Multiple attempts often needed for resistant cultivars
- Some cultivars are easier (apparently due to anatomical differences in meristem invasion)

### Cost reality

- Commercial meristem rescue service: $500-2500 per cultivar attempt, results not guaranteed
- DIY: thousands in equipment + months of learning, plus per-attempt failure rate
- For one or two cultivars, contract a service; for an ongoing program, build the lab

## CRYOPRESERVATION

Liquid nitrogen storage of meristem tissue at -196°C. Indefinite storage with negligible drift.

### Why use it

- Backup against catastrophic mom room loss
- Decade+ preservation of breeding stock (heirloom, landrace, IBL)
- Industry use: maintain cultivars without active mother rooms
- Safety net for HLVd-cleaned lines (re-contamination becomes recoverable)

### Process (advanced — research-lab-grade work)

1. Cold-acclimate source plant (4°C for 1-3 weeks)
2. Excise meristem (similar to HLVd rescue)
3. Loading solution (sucrose + glycerol bath, 20-60 min)
4. Vitrification solution (PVS2 or PVS3 — cryoprotectants, exposure 10-30 min)
5. Plunge into LN2 (vials or droplet vitrification on aluminum foil strips)
6. Store at -196°C indefinitely
7. Thaw rapidly in warm unloading solution when needed
8. Recover on standard medium

Cannabis-specific cryopreservation protocols are still being optimized. Recovery rates: 40-65% in research labs depending on cultivar (Uchendu et al., 2019).

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
**Commercial lab:** $50k-500k+ depending on throughput.

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

**Use TC when:** cleaning HLVd, preserving heirloom/landrace, large-scale commercial production, breeding stock backup.
**Use cuttings for:** everything else.

## DECISION TREE

```
WHY TISSUE CULTURE?

→ HLVd-positive line you want to save
   ├── One or two cultivars → CONTRACT meristem rescue service ($500-2500/line)
   └── Ongoing program → build in-house TC lab

→ Long-term backup of breeding stock (heirloom, landrace, IBL)
   └── CRYOPRESERVATION (advanced; consider partnering with research lab)

→ Commercial-scale clean clone production
   └── Build TC lab OR contract with established TC nursery (Dark Heart, Phylos, Front Range)

→ Just want clones for your home grow
   └── DON'T do TC. Use cuttings (see 11-propagation.md)

→ Research / curiosity / learning
   └── Start with kits ($300-500 starter), expect months of contaminated plates before consistent runs
```

## CONFUSION TRAPS

| Belief | Reality |
|---|---|
| "TC produces stronger plants" | Same genetics. Vigor benefit comes from removing systemic disease (HLVd, viruses), not from TC itself. |
| "TC is faster than cuttings" | Slower per cycle. Scales differently — exponential multiplication can outpace cuttings only at large scale. |
| "Meristem rescue always works" | 30-70% per attempt. Often takes multiple tries; not 100% clean. |
| "Anyone can do TC at home" | Possible but $5k+ investment, steep learning curve, months of failed runs typical. |
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

**Tier 2 — Commercial labs / suppliers:**
- Dark Heart Nursery — commercial HLVd elimination protocols, clean stock standards
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
- Commercial-scale clean stock context → `20-commercial-ops.md`
- Sterile-technique principles cross-applicable to → `08-pests.md` (quarantine), `09-disease.md` (sanitation)
