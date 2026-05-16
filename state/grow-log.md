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

Reference examples live in `docs/grow-log-entry-examples.md`. They are format examples only, not user history.

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
11. **Archive convention:** when this file exceeds ~200 entries OR ~12 months of entries, move oldest to an archive file named `grow-log-archive-YYYY` in the same directory. Never archive entries with `outcome: pending` or open `follow_up`.
12. **Show the appended entry to the user at session summary** (per SKILL.md Rule 6) — never silent.
13. **`issue` entries from photo diagnosis must use the diagnose-from-photo.md Pass 5 format** (Issue reported / Photo analysis / Action plan / Follow-up) inside the standard skeleton — that workflow is the source of truth for issue-entry body fields.

---

## User Entries

<!-- Real user entries appended below this line by the agent. Empty until first logged event. -->
