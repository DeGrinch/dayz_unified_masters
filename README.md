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

This repo exists primarily to provide a unified config for my own map design and needs, however as this is dayz and as the desire to use all dayz assets within a build means that I would require at least all of said official map assets data in a single foundation of configs I am going to create that foundation of unified files, here. These default files in this repo will provide:

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
- may contain some configurations which work for my map build specifically
- may possibly contain some asset configurations which you will want to modify for your use case.

I will do my best to simply create a unified OFFICAL configs repo here
and then pull this repo into an even more specific repo for my own map needs
to be honest for most of these files within the dayz economy environments where we develop beyond the scope of dayz' official developments it is always 
best to chain to additional customized configurations or overrides with your additional code / configs. 

Both outcomes are acceptable.

---

## Contributions / missing files

If a file is missing or should be included in the unified set, you can reach out here:

**Discord:**  
https://discord.gg/DWXTaEXyUe

---

Pew Pew Pew!
