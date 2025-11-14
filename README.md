# NHL 25 – Leafs Architect & Dynasty AI (Clean Rebuild)

Clean rebuilt environment for Austin Olsen’s NHL 25 Toronto Maple Leafs franchise.

This repo is the **single source of truth** for:
- Strategy canon (Canon v5 – NHL 25–accurate)
- Architect configuration (builder / JSON / schemas)
- Leafs Dynasty Suite AI configuration (GM + gameplay)
- Matchup and gameplan templates
- Slider and tactics maps that match the *actual* NHL 25 menus
- Export files used by custom GPTs

---

## 1. Project Goals

- Fix all old canon mistakes (wrong slider directions, non-existent tactics, etc.).
- Keep the structure **simple, readable, and recoverable**.
- Separate:
  - **Architect GPT** → files, JSONs, schemas, exports.
  - **Leafs Dynasty GPT** → gameplay help, GM advice, in-game tactics.
- Make it easy to:
  - Start a brand-new Dynasty chat.
  - Rebuild everything from this repo without relying on old conversations.
  - Add new opponents, gameplans, or canon versions safely.

---

## 2. Planned Folder Layout

These folders will be created gradually in future commits:

- `Architect/`
  - Core config files, strategy canon, schemas, and module settings.
- `Canon/`
  - Canon v5 strategy maps (forecheck, NZ, DZ, pressure, breakout, PP/PK).
- `Matchups/`
  - Per-opponent gameplans and matchup cards.
- `Sliders/`
  - NHL 25 slider maps (offensive and defensive line sliders, trap scale, etc.).
- `Exports/`
  - Full export files for loading into custom GPTs (e.g., `LeafsDynasty_FullExport_vX.json`).
- `Docs/`
  - Human-readable notes, how-to guides, and change logs.

The actual folders will be created as files are added in later steps.

---

## 3. Custom GPT Integration

This repo is designed to work with two custom GPTs:

1. **Architect GPT (Builder / File Brain)**
   - Reads and writes JSON, schemas, and config files in this repo.
   - Maintains Canon v5 strategy maps.
   - Validates sliders, tactics, and matchup files.
   - Produces GitHub-ready output (file path, contents, commit title, description).

2. **Leafs Dynasty Suite AI (GM + Gameplay)**
   - Uses the exports from this repo as read-only input.
   - Helps with:
     - Roster and lines
     - Trades and contracts
     - Gameplans, matchups, and in-game adjustments
   - Does **not** edit JSON directly; it asks Architect GPT (or you) to update files here.

---

## 4. NHL 25 Systems Scope (Canon v5)

Canon v5 will only use **real NHL 25 options**, including:

- **Forecheck:**  
  `1-2-2 Passive`, `1-2-2 Aggressive`, `2-3`, `Weak Side Lock`
- **Neutral Zone:**  
  `1-2-2 Red`, `1-2-2 Blue`, `1-3-1`, `1-4`
- **Trap Forecheck Slider (0–6):**  
  `0 = full trap`, `6 = full forecheck pressure`
- **Defensive Pressure:**  
  `Protect Net`, `Contain Puck`, `Normal`, `Puck Side Attack`, `High Pressure`
- **Defensive Strategies:**  
  `Collapsing`, `Staggered`, `Tight Point`
- **Offensive Strategy:**  
  `Defend Lead`, `Conservative`, `Standard`, `Aggressive`, `Full Attack`
- **Control Breakout:**  
  `Strong Side Slant`, `Blue-to-Blue`, `Three High`
- **Quick Breakout:**  
  `Stay Wide`, `Leave Zone Early`, `Close Support`
- **Offensive Line Sliders (0–10):**  
  `Carry/Dump`, `Cycle/Shoot`, `Efficiency/Energy`, `Don’t Block/Block`
- **Defensive Pair Sliders (0–10):**  
  `Hold Line/Pinch`, `Cycle/Shoot`

Future JSON files in this repo will map those options and sliders **exactly** to how they appear in-game.

---

## 5. Usage Pattern (High Level)

1. Architect GPT:
   - Creates or updates JSON/config files in this repo.
   - Always outputs:
     - File path
     - Full file contents
     - Commit headline (starting with `create`)
     - Commit description

2. Leafs Dynasty GPT:
   - Loads exports from `Exports/`.
   - Helps you with:
     - Full matchup cards (e.g., `/full gameplan @DET`)
     - In-game adjustment rules
     - GM decisions (trades, contracts, development).
   - When changes are needed to canon or configs, it will tell you:
     - “Ask Architect GPT to create/update `<file>` with these changes.”

---

## 6. Version Tags

- **Canon:** v5.0 (NHL 25–accurate tactics and sliders)
- **Architect Config:** v1.0 (Clean Rebuild)
- **Leafs Dynasty Export Format:** v1.0 (to be defined in `Exports/`)

A simple change log will be added later under `Docs/`.

---

## 7. Austin’s Preferences (Embedded Rules)

- Use **Canadian context** and Leafs franchise focus.
- Git commit headlines must start with `create`.
- All AI-generated file instructions must be:
  - iPhone-friendly (good on iPhone 14 Pro Max).
  - Presented as:
    1. File path (in its own copy-paste box)
    2. Full contents (copy-paste box)
    3. Commit headline (copy-paste box)
    4. Commit description (copy-paste box)

This README is the anchor for the clean rebuild. All future files, canon maps, and exports will build on top of this.