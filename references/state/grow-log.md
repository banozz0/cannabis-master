# Grow Log

Append-only journal of significant events across all grows. The agent reads the last 5 entries by default at session start (per SKILL.md Rule 1) and appends new entries as events occur (per Rule 6). Past entries are **never edited** — corrections go in a new `correction` entry that references the original date.

**Format:** Strictly chronological forward — oldest at top, newest at bottom. Each entry is a Markdown H2 header (`## YYYY-MM-DD — <type> — <stage>`) followed by standardized fields and free-form details.

**What belongs here vs. elsewhere:**

| Goes in `grow-log.md` | Goes elsewhere |
|---|---|
| Harvests (every one) | Routine daily/weekly feed values → `grow-context.md > Current Feed` |
| Issues + their resolution | Permanent equipment list → `grow-context.md > Lighting / Climate Control / etc.` |
| Schedule pivots (nute change, light schedule change) | Permanent user prefs → `user-profile.md` |
| Environmental events (heat spike, AC failure) | Recurring SOPs (how you always defoliate) → not stored here at all |
| Pheno selections (keeper / cull) | Per-feed routine readings — only log if anomalous |
| Equipment changes (with reason) | |
| Milestones (top, transplant, flip, harvest) | |
| Corrections to past entries | |

---

## Entry Template

Use this skeleton for every entry. Body fields between `strain(s):` and `outcome:` vary by type — see per-type conventions below.

```
## YYYY-MM-DD — <type> — <stage>
- strain(s): <names + count, or "all" or "n/a">
- <type-specific body fields — see conventions>
- outcome: <result, or "pending">
- follow_up: <YYYY-MM-DD + what to check, or "none">
- linked_entries: <YYYY-MM-DD of related past entries, or "none">
```

**Valid `<type>` values:** `harvest`, `issue`, `schedule-change`, `environment`, `pheno-note`, `equipment`, `milestone`, `correction`, `other`.

**Valid `<stage>` labels:** `seedling`, `veg-wN` (e.g., `veg-w2`), `flower-wN` (e.g., `flower-w5`), `late-flower`, `harvest`, `dry`, `cure`, `archive` (applies to plants no longer in an active grow cycle — mother plants, seed stock, long-term keepers).

### Per-type body field conventions

| Type | Required body fields |
|---|---|
| `harvest` | day_of_flower, wet_weight, dry_weight (when known), trichome_read, quality_notes |
| `issue` | Issue reported, Photo analysis (or Symptoms observed if no photo), Action plan, Follow-up — match `diagnose-from-photo.md` Pass 5 |
| `schedule-change` | What_changed, Why, Old → New values, Effective_date |
| `environment` | What_happened, Duration, Peak_values, Action_taken, Damage_observed |
| `pheno-note` | Pheno_ID, Observation, Decision (keeper / cull / monitor), Reason |
| `equipment` | What_changed, Why, Brand_model_added_or_removed |
| `milestone` | What_happened (top, transplant, flip, etc.), Method, Plants_affected |
| `correction` | Corrects_entry (date), What_was_wrong, What_is_now_true |
| `other` | Free-form, but always include a one-line `summary:` |

---

## Example Entries (REFERENCE FORMAT ONLY — NOT USER HISTORY)

⚠️ AGENT INSTRUCTION: The entries below the divider are FORMAT TEMPLATES. They use placeholder data (Wedding Cake strain, fictional 2025 dates). They are NOT the user's grow history. NEVER cite their content as if it happened to the user. NEVER include them in session-start log scans for follow-ups. Pattern-match the FORMAT only.

If no entries exist below the "## User Entries" header at the bottom of this file, the user has no logged grow history yet. Acknowledge this honestly.

---

## 2025-08-14 — milestone — veg-w2
- strain(s): Wedding Cake (Seed Junky), 2 plants
- What_happened: Topped both plants above the 5th node, started LST tie-down same day.
- Method: Clean razor blade, sterilized with isopropyl. Soft plant ties on side branches, anchored to fabric pot rim.
- Plants_affected: both
- Notes: Pheno #2 already showing tighter node spacing — flagging for keeper consideration.
- outcome: both recovering by 24h, no transplant shock
- follow_up: 2025-08-21 (1-week growth photo)
- linked_entries: none

## 2025-09-02 — issue — flower-w1
- strain(s): Wedding Cake #1
- Issue reported: lower-leaf interveinal yellowing, ~6 leaves on bottom third of plant
- Photo analysis: Mg deficiency, MEDIUM confidence. Top 3: 1) Mg def 80%, 2) pH lockout 15%, 3) Fe def 5%. Runoff pH 5.9 (in range), runoff EC 1.2 (low side).
- Action plan: Add Cal-Mg at 1 ml/L starting next feed. Verify pH 5.8 in. Do NOT flush yet.
- Follow-up: 2025-09-05 (72h photo check, look for new growth color)
- outcome: pending
- linked_entries: none

## 2025-09-05 — issue — flower-w1
- strain(s): Wedding Cake #1
- Issue reported: follow-up to 2025-09-02 — checking Cal-Mg fix
- Symptoms observed: lower-leaf damage unchanged (won't recover, expected). New growth top third dark green, no new yellowing. No further progression down the plant.
- Action plan: Continue Cal-Mg at 1 ml/L for the rest of the run. Update `grow-context > Nutrient Line > cal_mg: yes, GH CaliMagic 1 ml/L`.
- Follow-up: none
- outcome: resolved — Mg deficiency confirmed, fix working
- linked_entries: 2025-09-02

## 2025-09-20 — schedule-change — flower-w3
- strain(s): all (both Wedding Cake plants)
- What_changed: Switched bloom feed from GH 3-part to Athena Pro Core + Bloom A+B
- Why: GH ratios skewed N-heavy in flower per Bugbee bloom research; Athena Pro 1-part-equivalent simpler to dial. Wanted denser bud per K-bias.
- Old → New: GH FloraMicro 5 ml + FloraBloom 10 ml + FloraGro 2 ml/gal at EC 2.0 → Athena Core 1.5 g + Bloom A+B 1.5 g + 1.5 g per gal at EC 2.4 (final ramp target)
- Effective_date: 2025-09-20 (first feed went in this evening)
- Ramp plan: 60% → 75% → 100% mfg dose over 3 feeds to avoid shock
- outcome: pending — runoff check at next feed
- follow_up: 2025-09-23 (runoff EC + pH after 2nd feed at 75%)
- linked_entries: none

## 2025-09-25 — environment — flower-w3
- strain(s): all (both plants in tent)
- What_happened: Heat spike to 32°C for ~6 hours during peak afternoon while AC compressor cycled off (overload trip). Lights still at 75% during the event.
- Duration: ~6 hours, 13:00–19:00 local
- Peak_values: tent ambient 32°C, canopy IR-gun 30°C, RH dropped to 38%, VPD spiked to ~1.9 kPa
- Action_taken: Dimmed LEDs to 35% within 20 min of noticing, lowered RH target to 50% on humidifier to widen VPD safety margin, opened tent door briefly to dump heat. AC tech scheduled for service before next forecast heat wave.
- Damage_observed: No leaf taco at the time, no bleaching. Trichomes still milky on macro check the next morning.
- outcome: no immediate damage; monitor for delayed stress signs over 7 days
- follow_up: 2025-10-02 (recheck for delayed hermie risk in flower)
- linked_entries: none

## 2025-10-30 — harvest — harvest
- strain(s): Wedding Cake (both plants), pheno #1 and pheno #2
- day_of_flower: 65
- wet_weight: 1,850 g total (pheno #1: 870 g, pheno #2: 980 g)
- dry_weight: pending (estimated 8–10 day dry)
- trichome_read: ~70% milky, 25% amber, 5% clear (jeweler's loupe 30x, sampled 3 colas per plant)
- quality_notes: Pheno #2 markedly denser buds, gas+cake nose. Pheno #1 looser structure, sweeter nose, still high quality. Took 4 clones from pheno #2 the day before chop.
- harvest_method: dry-trim approach, hung whole plants from rack
- dry_environment_target: 17°C / 58% RH, dark, gentle airflow not direct on buds
- outcome: pending — final dry weight + cure quality in 8 weeks
- follow_up: 2025-11-08 (dry weight + jar entry), 2025-12-15 (cure mid-check at week 6)
- linked_entries: 2025-08-14 (initial topping that produced this canopy)

## 2025-11-15 — pheno-note — cure
- strain(s): Wedding Cake pheno #2 (mother + 4 clones rooted)
- Pheno_ID: WC-#2
- Observation: 7-day cure check confirmed keeper. Smell: gas + cake, no hay smell. Bud density passed pinch test. Yield-per-plant 410 g dry vs pheno #1's 360 g. Trichome amber-up 4 days earlier than #1.
- Decision: keeper
- Reason: Best on every axis — yield, terps, density, finish time. Worth maintaining as mother for future runs.
- Action: 4 clones rooted under T5, transitioning to mother veg tent. Pheno #1 culled.
- outcome: keeper retained; mother program started
- follow_up: 2025-12-15 (mother health check after first month under T5)
- linked_entries: 2025-08-14, 2025-10-30

---

## Append Rules (for the agent)

1. **Always append to the end of the file.** Never edit past entries. Newest at the bottom.
2. **If a past entry is wrong, log a `correction` entry** referencing the original date in `linked_entries` and explaining what was wrong vs. now true.
3. **Date format YYYY-MM-DD always.** Convert relative dates ("yesterday", "last week") to absolute dates before writing.
4. **One entry per event.** Don't merge two events on the same day into one entry — append two entries.
5. **Stage label must match `grow-context.current_stage` at time of event** (not at time of writing). If logging a flower-w3 event two weeks later, write `flower-w3`.
6. **Don't log routine feed data here.** That belongs in `grow-context.md > Current Feed`. Only log a feed-related entry if something anomalous happened (EC spike, pH crash, runoff way off).
7. **Don't log every photo** — only when a diagnosis or decision results from one.
8. **Confirm with user before appending these entry types** (durable decisions): `harvest`, `pheno-note` with keeper/cull, `schedule-change`, `equipment` removal. Show the drafted entry, get confirmation, then write.
9. **`outcome: pending`** is valid — log the event when it happens, then update via a follow-up entry once known. Never go back and edit the original `outcome` line.
10. **Follow-up dates trigger reminders.** At session start, scan recent entries for `follow_up` dates ≤ today and surface them: "You have an open follow-up from [date]: [what to check]."
11. **Archive convention:** when this file exceeds ~200 entries OR ~12 months of entries, move oldest to `grow-log-archive-YYYY.md` in the same directory. Never archive entries with `outcome: pending` or open `follow_up`.
12. **Show the appended entry to the user at session summary** (per SKILL.md Rule 6) — never silent.
13. **`issue` entries from photo diagnosis must use the diagnose-from-photo.md Pass 5 format** (Issue reported / Photo analysis / Action plan / Follow-up) inside the standard skeleton — that workflow is the source of truth for issue-entry body fields.

---

## User Entries

<!-- Real user entries appended below this line by the agent. Empty until first logged event. -->
