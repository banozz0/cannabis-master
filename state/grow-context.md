# Grow Context

Persistent state of user's current grow setup, equipment, and active grow. The agent updates this file only after showing a draft and receiving explicit user confirmation, then summarizes confirmed changes at session end (per SKILL.md Rule 6).

**Format:** Markdown with YAML-style key:value pairs inside fenced sections. Empty values = `[unset]`. Update fields, don't restructure.

---

last_updated: [unset]
last_updated_by: [unset — agent or user]
source_workflow: [unset]

## Space

```
location: [unset]              # tent / indoor room / outdoor / greenhouse / mixed
tent_or_room_size: [unset]     # e.g. 4x4 ft, 120x120 cm, 3x3 m
ceiling_height: [unset]        # cm or ft — affects light hang range
external_climate: [unset]      # e.g. Malta — hot/dry summer 30-35C, mild winter 12-18C, high humidity coastal
sealed_or_active: [unset]      # sealed room w/ AC+CO2 / active intake-exhaust / mixed
```

## Lighting

```
fixture_make_model: [unset]    # e.g. Mars Hydro TS3000, Gavita 1700e, HLG 600 Rspec
type: [unset]                  # LED quantum board / LED bar / HPS / CMH / fluorescent
wattage_at_wall: [unset]       # actual draw, not advertised
ppfd_target: [unset]           # measured at canopy if possible
hang_height_cm: [unset]        # current distance to canopy
photoperiod: [unset]           # 18/6, 20/4, 12/12, autoflower, light-dep schedule
schedule_on_off: [unset]       # e.g. on 06:00 off 00:00
dimmer_setting: [unset]        # % or specific control
```

## Climate Control

```
temp_day_target: [unset]       # °C or °F — be explicit
temp_night_target: [unset]
rh_day_target: [unset]         # %
rh_night_target: [unset]
vpd_target: [unset]            # kPa, per stage
co2: [unset]                   # ppm if supplemented; otherwise "ambient"
intake_cfm: [unset]
exhaust_cfm: [unset]
carbon_filter: [unset]         # Y/N + size
ac: [unset]                    # btu, mini-split, portable
dehumidifier: [unset]          # pints/day
humidifier: [unset]            # type, capacity
heater: [unset]
oscillating_fans: [unset]      # number + size
```

## Sensors / Monitoring

```
controller: [unset]            # Pulse Pro, Trolmaster, AC Infinity, none
ph_meter: [unset]              # make/model, last calibration date
ec_meter: [unset]
ppm_scale: [unset]             # 500 / 700 (NaCl vs KCl)
microscope: [unset]            # USB / loupe magnification
camera: [unset]                # any in-tent
```

## Medium & Containers

```
medium: [unset]                # soil mix / coco-perlite ratio / DWC / RDWC / aero / living soil
medium_brand: [unset]          # FFOF, FFHF, Coco Bliss, Canna Coco, custom mix
container_size: [unset]        # gal or L
container_type: [unset]        # fabric / plastic / air-pot / net pot / smart pot
plants_per_container: [unset]
total_plant_count: [unset]
```

## Water Source

```
source: [unset]                # RO / tap / well / rainwater / mixed
input_ec: [unset]              # EC of water before nutes
input_ppm: [unset]
input_ph: [unset]
alkalinity: [unset]            # ppm CaCO3 if measured (matters for organic)
hardness: [unset]              # ppm
ro_system: [unset]             # if used: stage count, filter age
```

## Nutrient Line

```
brand: [unset]                 # Athena Pro, Canna Coco, GH Trio, Jacks 321, MegaCrop, custom
schedule_followed: [unset]     # full mfg / lite / aggressive / custom
silica: [unset]                # Y/N + product
cal_mg: [unset]                # Y/N + product
beneficials: [unset]           # mycos, bacillus, trichoderma — list
ph_down: [unset]               # phosphoric / nitric / citric (organic) / sulfuric
ph_up: [unset]
```

## Current Feed (Most Recent)

```
date: [unset]
ec_in: [unset]
ph_in: [unset]
volume_per_pot_ml: [unset]
runoff_ec: [unset]
runoff_ph: [unset]
runoff_volume_pct: [unset]     # % of input volume
feed_frequency: [unset]        # daily / 1-on-1-off / when dry / fertigation X times daily
```

## Active Grow

```
strain_1: [unset]              # name + breeder
strain_2: [unset]
strain_3: [unset]
seed_or_clone: [unset]
photoperiod_or_auto: [unset]
phenotype_notes: [unset]       # if pheno-hunting
```

## Stage Tracking

```
current_stage: [unset]         # seedling / veg-week-X / flower-week-X / late-flower / flush / harvest / dry / cure
veg_started: [unset]           # date
flip_date: [unset]             # date 12/12 started
expected_harvest: [unset]      # date — flowering time + flip date
days_in_current_stage: [unset]
```

## Training Applied

```
techniques_used: [unset]       # comma list: topping, fim, lst, mainline, scrog, defoliation
top_count: [unset]             # number of mains
last_defoliation_date: [unset]
scrog_screen: [unset]          # Y/N + spacing
trellis_layers: [unset]
```

## Active Issues

```
issue_1: [unset]               # short description + status (active/resolved/monitoring)
issue_2: [unset]
issue_3: [unset]
```

## Goals

```
priority: [unset]              # yield / quality / terps / specific cannabinoid / breeding stock
target_yield: [unset]          # if specified
constraints: [unset]           # space, electricity, time, budget
```

## Notes

```
freeform: [unset]              # anything not captured above
```

---

## Schema Rules (for the agent)

1. **Update by replacing values, never restructure sections.** New fields go under `## Notes > freeform`.
2. **Every agent write sets `last_updated`, `last_updated_by`, and `source_workflow`.**
3. **If a field becomes obsolete (e.g. user switched from soil to hydro), don't delete — mark as `[changed YYYY-MM-DD: was: X]`** so history is preserved without mess.
4. **For multi-strain grows**, use `strain_1`, `strain_2`, etc. and per-strain notes in freeform.
5. **Confirm before destructive changes** (e.g. wiping active grow because new grow started → archive old to grow-log.md first).
6. **Initial population, destructive changes, first diagnostic logs, and durable issue entries require preview + explicit confirmation.** Every durable update requires preview and explicit confirmation, then a session-end summary.
