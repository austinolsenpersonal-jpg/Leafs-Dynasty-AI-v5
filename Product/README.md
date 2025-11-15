# Leafs Dynasty Canon — Project Structure (Product Directory)

This directory contains **all system files** that power Architect GPT and Leafs Dynasty GPT for Austin Olsen’s NHL 25 Franchise Mode.

The structure follows a clean separation of responsibility:

---

## 🔵 1. Architect GPT (Rules & Enforcement Layer)

**Folder:** `Product/Architect/`  
**Purpose:** Architect defines the *laws* of the universe.

Architect owns the following:

- **Canon system definitions**  
  (`Product/Canon/SystemsMap_v1.0.json`)

- **Slider engine rules**  
  (`Product/Config/SliderEngine_v5.0.json`)

- **Repo synchronization map**  
  (`Product/Config/RepoSync_v1.0.json`)

- **Template enforcement**  
  (matchup templates, coaching templates)

Architect **never** creates or manages trades, lines, gameplans, or gameplay decisions.  
It only sets rules, validates structure, and prevents illegal tactics or slider drift.

---

## 🟢 2. Leafs Dynasty GPT (GM + Coaching Layer)

**Folder:** `Product/Dynasty/`  
**Purpose:** Dynasty handles *all decision-making*, including:

- Full gameplans (`full_gameplan @DET`)
- Coaching cards
- In-game adjustments
- Roster management (NHL & AHL)
- Goalie plan
- Trades & contract logic
- Draft, scouting, development planning
- AHL readiness & call-up logic
- Matchup prep & pre-scouts

Dynasty **reads** Architect’s Canon but does **not modify** it.

---

## 🔶 3. Canon (Shared Source-of-Truth Files)

**Folder:** `Product/Canon/`

Contains rules that **both GPTs must follow**, including:

- `SystemsMap_v1.0.json`  
  (All legal NHL 25 strategies, forecheck/NZ/DZ options, breakouts, pressure, trap, etc.)

- Future canon files (v1.1, v1.2, etc.)  
  Will be added here by Architect GPT only.

Dynasty GPT may **read** but not alter these files.

---

## 📁 4. Config (Shared Configuration)

**Folder:** `Product/Config/`

Contains high-level engines and sync files:

- `RepoSync_v1.0.json`
- `SliderEngine_v5.0.json`

Architect controls these.  
Dynasty reads them.

---

## 📗 5. Instructions

### Architect instructions:
`Product/Architect/Architect_Instructions_v1.0.md`

### Dynasty instructions:
`Product/Dynasty/LeafsDynasty_Instructions_v1.0.md`

---

## 📦 6. Expected Growth

This repo will grow in clean sections:

- `Product/Dynasty/Gameplans/`
- `Product/Dynasty/Reports/`
- `Product/Canon/SystemsMap_v1.1.json` (future versions)
- `Product/Architect/Templates/`
- `Product/Config/…` new shared engines as needed

Both GPTs know how to expand their own folders without interfering with each other.

---

## Version Tag

Leafs Dynasty Canon (Repo Structure) — v1.0  
Architect Rules v1.0  
Dynasty Instructions v1.0  
RepoSync v1.0  
SliderEngine v5.0  
SystemsMap v1.0

---

This file ties the whole architecture together so both GPTs always know exactly where to read from, write to, and validate against.