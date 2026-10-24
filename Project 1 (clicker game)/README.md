# Energy Clicker — Plan and Update Log

## Project overview

Energy Clicker is a browser-based incremental game. Players generate energy by clicking, spend it on upgrades, complete missions, earn achievements, and reset through prestige for permanent bonuses. Progress is saved in the browser.

This document tracks the planned major updates and records what has been completed.

## Major update roadmap

| # | Major update | Scope | Status |
|---|---|---|---|
| 1 | Lab Management | Bulk-buy upgrades and track lifetime statistics. | **Done** |
| 2 | Research Tree | Add unlockable research branches with choices that shape a play style. | **Done** |
| 3 | Resource Crafting | Introduce another resource and recipes for specialized upgrades. | **Done** |
| 4 | Factory Builder | Let players arrange production modules and connect automation chains. | Planned |
| 5 | Exploration Map | Unlock locations with distinct production bonuses and visual themes. | Planned |
| 6 | Challenge Runs | Add optional scenarios with unique rules and rewards. | Planned |
| 7 | Artifact Collection | Add passive artifacts that players can collect and equip. | Planned |
| 8 | Story Campaign | Build a progression-based sequence of chapters, characters, and goals. | Planned |
| 9 | Accessibility & Localization | Expand language support and input, display, and assistive options. | Planned |
| 10 | Portable Saves | Support save-file export and import; consider cloud sync if a backend is added. | Planned |

The roadmap is a guide, not a fixed release schedule. Scope and order may change as the game evolves.

## Update log

### Update 1 — Lab Management

**Status:** Complete  
**Date:** 2026-10-23

- Added a shop quantity selector for buying 1, 10, or 100 upgrades at a time.
- Showed the total bundle price, recalculated sequential Efficient Circuits discounts, and handled its level cap during bulk purchases.
- Added lifetime counters for energy generated, clicks, upgrades purchased, and prestige cores.
- Saved the selected purchase quantity with existing browser save data.
- Verified bulk purchase pricing, stats and selection persistence after reload, discount progression and level-cap behavior, and a narrow mobile viewport.

### Update 2 — Research Tree

**Status:** Complete  
**Date:** 2026-10-24

- Added a permanent research tree with branch-based upgrades and prerequisite locks.
- Earned research points from lifetime energy generation; points persist in browser saves.
- Applied research bonuses to click output, passive generation, upgrade costs, and prestige scaling.
- Added a dedicated research panel with unlock states, branch labels, and point tracking.

### Update 3 — Resource Crafting

**Status:** Complete  
**Date:** 2026-10-24

- Added crystal refinement and three craftable specialty upgrades.
- Resource crafting grants permanent bonuses to click power, passive generation, and upgrade costs.
- Saved crystal totals and crafted-upgrade levels with the browser save data.

## Current game features

- Click-to-generate energy and passive production.
- Five upgrade types, including click-power and cost-reduction upgrades.
- Research tree with permanent branch upgrades and prerequisite locks.
- Resource crafting with crystals and specialized upgrades.
- Missions, achievements, and prestige.
- Automatic local saves and capped offline production.
- Optional sound, motion, and break-reminder settings, plus pause/resume.
- Bulk upgrade purchases, lifetime statistics, research progression, and crafting.

## Development notes

- The game currently runs as a standalone `index.html` file; saves use browser `localStorage`.
- Keep the game playable without a server. Cloud saves would require adding and documenting a backend.
- For each major update, record the date, key changes, and relevant verification in the update log above.
