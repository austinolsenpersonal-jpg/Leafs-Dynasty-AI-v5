# Leafs-Dynasty-AI-v5 — Repo Status v1.0

_Last updated: 2025-11-17_  
_Author: Leafs Architect GPT_

---

## 1. Overview

This repository (`Leafs-Dynasty-AI-v5`) is the **active, canonical home** for all Leafs Dynasty AI v5 assets:

- Architect runtime configs  
- Canon strategy files  
- StrategyTrees  
- Engines  
- Dynasty intelligence (archetypes, roster sync, etc.)  
- Docs and workflows for gameplans, reports, and formatting  

All **new work** must be done here going forward.

---

## 2. Active vs Archived Repos

### Active Repo (this one)

- **Name:** `Leafs-Dynasty-AI-v5`  
- **Role:** Single source of truth for Architect + Dynasty GPT.  
- **Runtime:** `Product/Architect/RuntimeConfig_v2.2.json` (current)  

This is what Architect GPT and Dynasty GPT should always reference.

### Archived Repo (old)

- **Name:** `Leafs-Dynasty-AI`  
- **Role:** Historical archive and backup only.  
- **Status:** Do **not** use for active development or new files.  
- May contain early experiments, legacy workflows, and older Canon versions.

---

## 3. Current Runtime & Key Configs

**Active runtime (Architect & Dynasty):**

- `Product/Architect/RuntimeConfig_v2.2.json`

This runtime:

- Links to Canon v5.0  
- Links to StrategyTrees v1.0  
- Enables **RosterSync_Integrity v1.0** (strict mode)  
- Enables **Formatting_Spec v1.0** (global formatting rules)  
- Uses **Sliders_v2.0_AllStar_Austin** by default  
- Activates **Dynasty_ReliabilityPatch v5.2**  
- Connects to the **OpponentArchetypes v1.0** spec  

**Key config files:**

- `Product/Config/Sliders_v2.0_AllStar_Austin.json`  
- `Product/Config/Dynasty_ReliabilityPatch_v5.2.json`  

---

## 4. Canon & Strategy Assets

**Canon (NHL 25 systems – v5.0):**

- `Product/Canon/Canon_Manifest_v5.0.json`  
- `Product/Canon/Forecheck_v5.0.json`  
- `Product/Canon/NeutralZone_v5.0.json`  
- `Product/Canon/DefensiveStrategy_v5.0.json`  
- `Product/Canon/DefensivePressure_v5.0.json`  
- `Product/Canon/OffensiveStrategy_v5.0.json`  
- `Product/Canon/ControlBreakout_v5.0.json`  
- `Product/Canon/QuickBreakout_v5.0.json`  
- `Product/Canon/StrategyMaps_v5.0.json`  

**StrategyTrees & Engines:**

- `Product/StrategyTrees/FiveOnFive_v1.0.json`  
- `Product/Engines/GameplanEngine_v1.0.json`  

These define how Canon options are combined into in-game strategies and gameplans.

---

## 5. Dynasty Intelligence Layer

**Opponent archetypes:**

- `Product/Dynasty/OpponentArchetypes_v1.0.json`  
  - Classifies teams (chaos forecheck, rush offense, heavy cycle, trap, balanced hybrid)  
  - Gameplans use this to choose counters.

**Roster integrity:**

- `Product/Dynasty/RosterSync_Integrity_v1.0.json`  
  - Enforces strict roster sync:
    - No guessed lineups  
    - No invented players  
    - No default NHL rosters  
    - Only user-uploaded screens are allowed  

**Dynasty structure folders:**

- `Product/Dynasty/Matchups/` — per-opponent matchup/gameplan files (future use)  
- `Product/Dynasty/Snapshots/` — franchise state snapshots (future use)  

---

## 6. Docs & Formatting

**Formatting rules (global):**

- `Docs/Formatting_Spec_v1.0.md`  
  - Defines:
    - Heading levels  
    - Bullet styles  
    - Dividers  
    - Mobile-friendly spacing  
    - GitHub/Markdown-safe layout  

**Reports workflow:**

- `Docs/Reports_Workflow_v1.0.md`  
  - Defines how gameplans and postgame reports are structured and where they are stored (e.g., `Reports/Gameplans/`, `Reports/Postgames/`).

**Modules spec:**

- `Docs/Dynasty_Modules_v5.2_Spec.md`  
  - Describes the active Dynasty module set and reliability rules.

---

## 7. How Architect & Dynasty Should Use This Repo

**Architect GPT:**

- Loads: `Product/Architect/RuntimeConfig_v2.2.json`  
- Reads/writes:
  - Canon files  
  - StrategyTrees  
  - Engines  
  - Docs  
  - New config/spec JSONs  
- Outputs files in **four-block GitHub format**:
  1. File path  
  2. Full contents  
  3. Commit headline (`create ...`)  
  4. Commit description  

**Dynasty GPT:**

- Uses the same runtime config via autoload:  
  - `/dynasty_autoload set "Product/Architect/RuntimeConfig_v2.2.json"`  
- Reads:
  - Canon  
  - StrategyTrees  
  - Archetypes  
  - RosterSync integrity  
  - Sliders  
  - Reliability patch  
- Generates:
  - Gameplans  
  - Bench cards  
  - Matchup reports  
  - Diagnostics (future)  

All **new JSON specs, gameplans, and reports** should be created in this repo using the Architect formatting rules.

---

## 8. Version Notes

- **Runtime v2.0:** Initial Architect runtime refactor.  
- **Runtime v2.1:** Linked Formatting_Spec and Sliders v2.0.  
- **Runtime v2.2:** Activated RosterSync_Integrity v1.0 and OpponentArchetypes v1.0; enabled strict roster sync and global formatting.

Future versions (v2.3+) will extend:

- Strategy tuning rules  
- Gameplan templates v2.0  
- Bench card templates  
- Live coaching engine  
- Additional Dynasty intelligence features.

---

_End of Repo Status v1.0_