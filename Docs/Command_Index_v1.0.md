# Leafs Dynasty AI — Command Index v1.0

_Last updated: 2025-11-17_  
_Author: Leafs Architect GPT_

This document lists the main commands used with:

- **Architect GPT** (system designer / file architect)  
- **Dynasty GPT** (franchise/coach brain)  

It is meant as a quick control panel so Austin always knows what to type and when.

---

## 1. Architect GPT Commands

Architect GPT is responsible for:

- Runtime configs  
- Canon / StrategyTrees / Engines  
- Repo file design  
- JSON / docs / specs  
- Guardrails and validation rules  

### 1.1 Core Runtime Commands

**`/architect_runtime load "<path/to/RuntimeConfig_x.x.json>"`**  
- Loads a specific runtime config and makes it active.  
- Example:  
  - `/architect_runtime load "Product/Architect/RuntimeConfig_v2.2.json"`  

Used when:
- You create a new runtime version (v2.0, v2.1, v2.2, etc.)  
- You want Architect to switch to that version’s rules.

---

### 1.2 Sync / Status Style Prompts

These are natural-language prompts (not strict slash commands) that Architect understands:

**`Sync with RuntimeConfig_v2.2`**  
- Ask Architect to confirm which runtime, sliders, patch, and formatting spec are active.

**`Confirm active modules and specs`**  
- Architect lists:
  - Canon version  
  - StrategyTrees version  
  - Sliders profile  
  - ReliabilityPatch version  
  - Formatting spec  
  - Archetypes / RosterSync status  

**`Summarize current repo status`**  
- High-level view of:
  - Active runtime  
  - Canon and StrategyTrees  
  - Key config files  
  - Dynasty intelligence layer  

---

### 1.3 Design / File Creation Prompts

Architect does not use hard-coded slash commands for file creation; instead, use clear prompts like:

- **`Create a new runtime config v2.3 with these changes: ...`**  
- **`Design a Gameplan Template v2.0 markdown file`**  
- **`Add a Team Tags v1.0 JSON spec under Product/Dynasty`**  
- **`Create a GitHub Actions workflow to validate JSON`**  

Architect will respond with the standard four-block GitHub format:

1. File path  
2. Full contents  
3. Commit headline  
4. Commit description  

---

### 1.4 Watchdog / Scan Concept (Architect-Side)

_Conceptual only (no file-based tool yet)_

**`/watchdog scan —config "Product/Architect/RuntimeConfig_vX.X.json" —output "latest"`**  
- Used as a conceptual “scan” of the current runtime and repo references.  
- Architect explains:
  - What runtime points to  
  - Which modules are active  
  - Any obvious inconsistencies  

This is more of a pattern than a hard-coded tool, but the command style can be reused in prompts for consistency.

---

## 2. Dynasty GPT Commands

Dynasty GPT is responsible for:

- Gameplans  
- Bench cards  
- Matchups  
- Roster / lines usage  
- Cap and contracts logic (when data is available)  
- Scouting, schedule, and season flow advice  

### 2.1 Core Runtime / Baseline Commands

**`/dynasty_autoload set "<path/to/RuntimeConfig_x.x.json>"`**  
- Tells Dynasty GPT which Architect runtime to use.  
- Example:  
  - `/dynasty_autoload set "Product/Architect/RuntimeConfig_v2.2.json"`  

Dynasty should reply confirming:
- Active runtime version  
- Sliders profile  
- ReliabilityPatch version  
- RosterSync mode  
- Formatting spec  

---

**`/resync baseline`**  
- Clears cached live-state memory inside Dynasty GPT:
  - Lines  
  - Special teams  
  - Tactics  
  - Cap snapshot  
  - Contract wants  
  - Assignments (NHL/AHL)  
- Forces Dynasty to rely only on:
  - Canon  
  - StrategyTrees  
  - Engines  
  - Runtime config  

Used when:
- Rosters changed significantly  
- You feel Dynasty is using stale lineups or old cap data  
- You want a “fresh start” before uploading new screenshots.

---

### 2.2 Roster / Lines / Contracts Sync

These are natural-language prompts to drive RosterSync Strict Mode:

**`/update roster`**  
- Used after you upload:
  - NHL/AHL lines screens  
  - Scratches  
  - Assigned lists  

Dynasty should:
- Parse the screenshots  
- Rebuild internal roster state  
- Respect RosterSync_Integrity rules (no guessing).

---

**`/update contracts`**  
- Used after you upload:
  - Contracts screen  
  - Pending RFAs/UFAs  

Dynasty uses this for:
- Extension logic  
- Trade value  
- Cap planning.

---

### 2.3 Gameplan & Matchup Commands

**`/Full Gameplan @ <TEAM>`**  
- Generates a full, opponent-specific gameplan using:
  - Canon  
  - StrategyTrees  
  - OpponentArchetypes  
  - Runtime rules  
  - FormattingSpec  

Example:  
- `/Full Gameplan @ DET`  
- `/Full Gameplan @ WSH`  

---

**`/matchup <TEAM NAME>`**  
- Focused scouting/matchup report vs a specific team.  
- Example:  
  - `/matchup Washington Capitals`  

Dynasty covers:
- Opponent identity  
- System tendencies  
- Line/D-pair threats  
- Goalie tendencies  
- Summary of counters.

---

**`/bench_card @ <TEAM>`** _(naming convention)_  
- Short-form bench coaching sheet:
  - Period-by-period keys  
  - System switches  
  - Trap slider guidance  
  - Matchups  
  - Coaching triggers  

Example:  
- `/bench_card @ WSH`

_Note: naming is flexible, but this pattern keeps it consistent._

---

### 2.4 Analysis / Rebuild Commands

**`/team_rebuild_analysis`**  
- Deep dive into:
  - Current roster quality  
  - Age curve  
  - Cap structure  
  - Prospect pipeline  
  - Draft picks  
- Returns recommendations:
  - Rebuild / retool / push-now  
  - Trade categories  
  - Extension priorities.

---

**`/line_optimizer`**  
- Uses Canon + chemistry + roles to optimize:
  - NHL lines  
  - AHL lines (when data available)  
- Respects:
  - RosterSync strict mode  
  - Actual players from screenshots  
  - Canon-legal systems.

---

### 2.5 Diagnostic & Coaching Flow Commands

**`Pre-game diagnostic vs <TEAM>`**  
- Natural-language version of:
  - Pre-game matchup check  
  - Opponent identity  
  - Your systems vs theirs  
  - Goalie choice sanity check  
  - Trap slider and pressure sanity checks.

---

**`Post-game review vs <TEAM>`**  
- Asks Dynasty to:
  - Classify the loss/win as:
    - System loss  
    - Execution loss  
    - Coinflip game  
  - Suggest:
    - System changes vs micro-adjustments  
    - Goalie/line changes only if necessary.

---

## 3. Repo / GitHub Workflow Habits

These are not slash commands, but standard patterns:

- **Architect side:**  
  - “Create a new file at: …”  
  - “Use commit headline: `create ...`”  
  - “Use commit description: …”  

- **Dynasty side:**  
  - “Generate a gameplan I can save under Reports/Gameplans/…”  
  - “Format this as something I can paste into a Markdown file.”

All new structural files (JSON, MD) should follow the Architect four-block pattern:

1. File path  
2. Full contents  
3. Commit headline  
4. Commit description  

---

## 4. Version Notes

This index describes the command set as of:

- **Runtime:** `RuntimeConfig_v2.2`  
- **Canon:** v5.0  
- **StrategyTrees:** v1.0  
- **ReliabilityPatch:** v5.2  
- **FormattingSpec:** v1.0  
- **RosterSync_Integrity:** v1.0  
- **OpponentArchetypes:** v1.0  

Future versions (v2.3+) may add:

- More precise naming for PGD (Pre-Game Diagnostic)  
- Explicit `/push_*` style repo commands (conceptual; still manual commits)  
- Additional helper commands as the GM Suite grows.