# Energy Clicker — Plan and Update Log

## Project overview

Energy Clicker is a browser based incremental game. Players generate energy by clicking, spend it on upgrades, complete missions, earn achievements, and reset through prestige for permanent bonuses. Progress is saved in the browser.

This document tracks the planned major updates and records what has been completed.

## Major update roadmap

| # | Major update | Scope | Status |
|---|---|---|---|
| 1 | Lab Management | Bulk buy upgrades and track lifetime statistics. | **Done** |
| 2 | Research Tree | Add unlockable research branches with choices that shape a play style. | **Done** |
| 3 | Resource Crafting | Introduce another resource and recipes for specialized upgrades. | **Done** |
| 4 | Factory Builder | Let players arrange production modules and connect automation chains. | **Done** |
| 5 | Exploration Map | Unlock locations with distinct production bonuses and visual themes. | **Done** |
| 6 | Challenge Runs | Add optional scenarios with unique rules and rewards. | **Done** |
| 7 | Artifact Collection | Add passive artifacts that players can collect and equip. | **Done** |
| 8 | Story Campaign | Build a progression based sequence of chapters, characters, and goals. | Planned |
| 9 | Accessibility & Localization | Expand language support and input, display, and assistive options. | Planned |
| 10 | Portable Saves | Support save file export and import; consider cloud sync if a backend is added. | Planned |

The roadmap is a guide, not a fixed release schedule. Scope and order may change as the game evolves.

## Update log

### Update 1 — Lab Management

**Status:** Complete  
**Date:** 2026-10-23

- Added a shop quantity selector for buying 1, 10, or 100 upgrades at a time.
- Showed the total bundle price, recalculated sequential Efficient Circuits discounts, and handled its level cap during bulk purchases.
- Added lifetime counters for energy generated, clicks, upgrades purchased, and prestige cores.
- Saved the selected purchase quantity with existing browser save data.
- Verified bulk purchase pricing, stats and selection persistence after reload, discount progression and level cap behavior, and a narrow mobile viewport.

### Update 2 — Research Tree

**Status:** Complete  
**Date:** 2026-10-24

- Added a permanent research tree with branch based upgrades and prerequisite locks.
- Earned research points from lifetime energy generation; points persist in browser saves.
- Applied research bonuses to click output, passive generation, upgrade costs, and prestige scaling.
- Added a dedicated research panel with unlock states, branch labels, and point tracking.

### Update 3 — Resource Crafting

**Status:** Complete  
**Date:** 2026-10-24

- Added crystal refinement and three craftable specialty upgrades.
- Resource crafting grants permanent bonuses to click power, passive generation, and upgrade costs.
- Saved crystal totals and crafted upgrade levels with the browser save data.

### Update 4 — Factory Builder

**Status:** Complete  
**Date:** 2026-10-25

- Added a factory module system for drilling, smelting, and assembly line scaling.
- Built module costs and purchase logic into the economy, with persistent counts in save data.
- Integrated module perks into passive production and global output efficiency.

### Update 5 — Exploration Map

**Status:** Complete  
**Date:** 2026-10-25

- Added an exploration map with unlockable sectors and permanent region bonuses.
- Region payouts boost overall production, click power, and prestige scaling.
- Saved each unlocked sector with the game progress.

### Update 6 — Challenge Runs

**Status:** Complete  
**Date:** 2026-10-25

- Added three timed challenges for clicking, energy generation, and upgrade purchases.
- Awarded one-time crystal rewards for completing each challenge.
- Made challenge timers pause with the game; failed attempts can be retried.
- Persisted completed challenge rewards while keeping active attempts out of saves.

### Update 7 — Artifact Collection and Progress Views

**Status:** Complete  
**Date:** 2026-10-25

- Added four collectible artifacts with permanent bonuses to clicking, energy production, crystal production, or upgrade costs.
- Added crystal purchases, equip and unequip controls, and a two-artifact equipment limit.
- Saved collected and equipped artifacts, validating saved IDs and enforcing the equipment limit during load.
- Organized progression panels into Overview, Build, and Records views with accessible section controls.
- Verified artifact purchasing, slot limits, equipping, bonus calculations, and pause behavior.

## Latest devlog — The Lab Overhaul

This update was the big combined push: instead of spreading improvements across multiple tiny waves, everything landed together in one stronger release. The game now feels more complete, more addictive, and far easier to understand at a glance.

We rebuilt the progression loop around a cleaner structure: the player still clicks to generate energy, but now that energy fuels a broader lab system that includes upgrades, research, crafting, modules, sectors, missions, achievements, challenge runs, and prestige. The core loop is faster to understand, while the deeper systems reward long-term planning.

### What changed

- Added a stronger clicker foundation with manual energy gains, passive production, and a click-speed readout in the main HUD.
- Expanded the upgrade system with buy quantity controls, cost scaling, and better bulk purchase feedback.
- Added a research tree with permanent branch upgrades and requirement locks, so progression feels deliberate instead of repetitive.
- Introduced crystal crafting and specialty upgrades that improve click power, passive generation, and economy efficiency.
- Added factory modules for scaling automation and deeper production chains.
- Added exploration sectors with permanent region bonuses and bigger strategic payoff.
- Introduced timed challenge runs with crystal rewards and pause-safe gameplay.
- Added collectible artifacts with permanent bonuses and a two-slot equipment limit.
- Organized the interface into Overview, Build, and Records views to make the game feel cleaner and more readable.
- Added missions, prestige, lifetime statistics, and unlockable achievements to extend the progression arc.
- Improved save reliability and offline production logic so larger runs remain stable.
- Added optional sound, motion, and break reminder controls for a more polished experience.

### Why this feels better

The main goal was to make the game feel more alive without making it confusing. The old version was functional, but it felt like pieces spread across separate systems. This version unifies those pieces into one lab identity: you are building a power engine, not just clicking a number.

The progression is now smoother because each system feeds into the next. Upgrades strengthen output, research refines the economy, crafting adds specialization, factory modules scale automation, sectors expand scale, and prestige resets the board for long-term growth. The UI is clearer, the loop is stronger, and the game reads as an actual incremental game rather than a loose prototype.

### Final state

The project now sits in a strong middle ground between simple arcade gameplay and deeper strategy progression. It is still lightweight and browser-first, but it has enough systems to feel rewarding and replayable. The next logical steps are story content, accessibility support, and portable save/import tools, but the current build is a major, polished release in its own right.

## Current game features

- Click to generate energy and passive production.
- Five upgrade types, including click power and cost reduction upgrades.
- Research tree with permanent branch upgrades and prerequisite locks.
- Resource crafting with crystals and specialized upgrades.
- Factory building modules and exploration sectors for large scale progression.
- Timed challenge runs with one time crystal rewards.
- Collectible artifacts with two equipment slots and permanent bonuses.
- Organized progression panels with Overview, Build, and Records views.
- Missions, achievements, and prestige.
- Automatic local saves and capped offline production.
- Optional sound, motion, and break reminder settings, plus pause/resume.
- Bulk upgrade purchases, lifetime statistics, research progression, crafting, factory modules, and exploration.

## Development notes

- The game currently runs as a standalone `index.html` file; saves use browser `localStorage`.
- Keep the game playable without a server. Cloud saves would require adding and documenting a backend.
- For each major update, record the date, key changes, and relevant verification in the update log above.
