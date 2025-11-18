# Leafs Dynasty AI – V5 Repository
A fully structured, modular, runtime-driven NHL 25 Franchise Mode assistant system featuring:

- Architect GPT (builder, code, runtime generation)
- Dynasty GPT (roster, lines, gameplans, matchups, reports)
- Canon Strategy System (v4.x+)
- RuntimeConfig Engine (v2.x+)
- Export Pipeline (gameplans, matchups, reports, runtimes, packaging)

Built and maintained by **Austin Olsen**.

---

## 📁 Repository Structure

```
Leafs-Dynasty-AI-v5/
│
├── Canon/                 # Strategy canon, enums, maps, 5v5 logic, breakout maps
│
├── Product/
│   ├── Architect/         # Architect runtimes + system builders
│   └── Dynasty/           # Dynasty game engines, matchups, lines, logic modules
│
├── Exports/
│   ├── Gameplans/         # Exported opponent-specific gameplans (JSON)
│   ├── Matchups/          # Opponent scouting & matchup exports (JSON)
│   ├── GameReports/       # Post-game reports / system evaluations
│   ├── Runtimes/          # Runtime snapshots (version history of gameplan/report runs)
│   └── Packaging/         # Release notes & packaged runtime bundles
│
└── README.md              # You are reading this
```

---

## 🧠 System Overview

### Architect GPT (Builder Mode)
Responsible for:
- Creating & updating RuntimeConfig files  
- Building Canon Strategy files  
- Generating templates and folder structures  
- Managing repo consistency and upgrades  
- Export system research & development  

Architect = **the coder, engineer, and systems person**.

---

### Dynasty GPT (Assistant GM / Coaching Mode)
Responsible for:
- Reading screenshots (lines, contracts, cap, tactics)  
- Suggesting optimized lines & chemistry  
- Building custom gameplans per opponent  
- Running matchup analysis  
- Live coaching during games  
- Post-game reporting & adjustments  
- Runtime-driven strategy logic  

Dynasty = **the GM, coach, strategist**.

---

## 📤 Exports Pipeline (New in v5)
All exports now live in the `Exports/` directory.

### 1. Gameplans
Opponent-specific full NHL 25 gameplans including:
- Systems  
- Sliders  
- Triggers  
- Matchups  
- Period plans  
- Goalie decisions  

Template:  
`Exports/Gameplans/BaseGameplanTemplate.json`

---

### 2. Matchups
Opponent scouting reports:
- System tendencies  
- Threats  
- Weak defense pairs  
- Goalie tendencies  
- Line matching  

Template:  
`Exports/Matchups/BaseMatchupTemplate.json`

---

### 3. Game Reports
Post-game summaries:
- Systems performance  
- What worked / failed  
- Next-game adjustments  
- Runtime insight  

Template:  
`Exports/GameReports/GameReportTemplate.json`

---

### 4. Runtime Snapshots
Records which runtimes/system versions generated each export:
- RuntimeConfig version  
- Architect version  
- Canon version  
- StrategyMap version  

Template:  
`Exports/Runtimes/RuntimeSnapshotTemplate.json`

---

### 5. Packaging (Release Notes)
Used for runtime, canon, or export bundle releases.

Template:  
`Exports/Packaging/ReleaseNotesTemplate.md`

---

## 🔧 How to Add Files (iPhone Friendly)

On GitHub mobile:
1. Open folder  
2. Tap **Add file → Create new file**  
3. Paste filename (including folders)  
4. Paste contents  
5. Commit using:

**Commit headline**
```
create <FileName>
```

**Commit description**
```
Description of what the file does and why it exists.
```

---

## 🚀 Current Runtime
Active runtime used by Architect & Dynasty:

```
Product/Architect/RuntimeConfig_v2.2.json
```

(Updated automatically when you run `/architect_runtime load`)

---

## 🏒 What This Repo Enables
- Coaching-grade NHL 25 gameplans  
- Opponent scouting & matchup prep  
- Dynamic strategies based on Detroit/WSH-style team tags  
- Runtime versioning & export logging  
- Long-term franchise memory  
- Data-driven season improvements  
- Full synergy between Architect & Dynasty chats  

---

## 📌 Next Recommended Additions
- Export automation  
- Season summary exporters  
- Canon v5.0 rewrite  
- Architect runtime auto-validator  
- Dynasty Line Optimizer v3 module  

---

# End of README