# dayz_unified_masters

### Unified DayZ Standalone Server Configs

This repository contains **unified configuration files** for **DayZ Standalone servers**, intended to simplify working with multiple official map assets in a single build.

The focus is on files such as:

- `types.xml`
- `mapgroupproto.xml`
- other map-dependent `mpmission` configuration files

---

## What problem this repo solves

DayZ official maps (Chernarus, Livonia/Enoch, Sakhal, etc.) each ship with their **own `mpmission/` config files**.

Important details:

- Each map’s config files are **map-specific**
- Many of these files contain **overlapping data**
- Some values **change subtly per map**
- Assets unique to one map **do not exist** in another map’s configs

This becomes a problem when you want to:

- Build a **custom map**
- Use **assets from multiple official maps**
- Avoid manually re-merging files every time you update or test

---

## Simple example

### Case 1: Single-map build (easy)

If you are building a map that **only uses Chernarus assets**:

- You can safely use the default Chernarus `mpmission` configs
- No merging is required
- Everything works as expected

---

### Case 2: Multi-map asset build (problematic)

If you want to use:

- Chernarus assets **plus**
- Sakhal assets **or**
- Livonia (Enoch) assets

You now have an issue:

- Each map’s `mpmission` files only define **their own assets**
- Many files contain **duplicate definitions**
- Some proto values differ by map
- Assets from Sakhal or Enoch **do not exist** in Chernarus configs

If you simply apply the default Chernarus setup:

- Missing assets will not spawn
- Protos may be incomplete or incorrect
- Manual fixes become repetitive and error-prone

---

## What this repository provides

This repo exists to provide:

- **Unified, de-duplicated configuration files**
- A **single “true” master list** per file
- Coverage for **all official map assets**
- A way to avoid constantly reworking the same configs

The intent is to:

- Merge map-specific configs
- Remove duplicates
- Preserve correct proto variations
- Maintain one authoritative version per file

---

## Scope and expectations

- This repo is maintained **as needed** during active map development
- Files will be added or updated incrementally
- The repo may become outdated or obsolete over time
- CI/CD automation may be added later

This project may be:

- Very useful to some
- Of little or no use to others

Both outcomes are acceptable.

---

## Contributions / missing files

If a file is missing or should be included in the unified set, you can reach out here:

**Discord:**  
https://discord.gg/DWXTaEXyUe

---

Pew Pew Pew!
