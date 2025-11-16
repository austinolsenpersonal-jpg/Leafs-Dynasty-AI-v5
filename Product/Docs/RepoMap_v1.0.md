# Repo Map — Leafs-Dynasty-AI-v5 (v1.0)

A clean, readable overview of the full repo structure for both Architect GPT and Dynasty GPT.

---

## TOP LEVEL
```
/
├── Architect/
├── Docs/
├── Product/
├── Project_Bootstrap_v1.0.json
└── README.md
```

---

## PRODUCT ROOT
```
Product/
├── Architect/
├── Canon/
├── Coaching/
├── Config/
├── DailyOps/
├── Dynasty/
├── Engines/
├── Exports/
├── Roster/
├── StrategyTrees/
├── Templates/
└── README.md
```

---

## CANON (NHL 25 Legal Strategy)
```
Product/Canon/
├── Forecheck.json
├── NeutralZone.json
├── OffensiveStrategy.json
├── DefensivePressure.json
├── DefensiveStrategy.json
├── ControlBreakout.json
└── QuickBreakout.json
```

These define ONLY the real NHL 25 options:
- Forecheck: 1-2-2 Passive / Aggressive, 2-3, Weak-Side Lock  
- Neutral Zone: 1-2-2 Red / Blue, 1-3-1, 1-4  
- Pressure: Protect Net, Contain Puck, Normal, Puck-Side Attack, High Pressure  
- Defensive Strategies: Collapsing, Staggered, Tight Point  
- Breakouts: Strong Side Slant, Blue-to-Blue, 3-High  
- Quick Breakout: Stay Wide, Leave Zone Early, Close Support  

Architect GPT **owns** Canon.  
Dynasty GPT **uses** Canon (cannot modify it).

---

## STRATEGY TREES
```
Product/StrategyTrees/
├── FiveOnFive_v1.0.json
└── SpecialTeams_v1.0.json
```

Trees = decision logic → matchups, gameplans, adjustments.

---

## ENGINES
```
Product/Engines/
├── MatchupEngine_v1.0.json
└── GameplanEngine_v1.0.json
```

- MatchupEngine → opponent analysis  
- GameplanEngine → full gameplans auto-built from Canon

---

## TEMPLATES
```
Product/Templates/
└── MatchupCard_v1.0.json
```

Formatting blueprints (cards, reports).

---

## CONFIG
```
Product/Config/
└── LeafsDynasty_MasterBootstrap_v2.0.json
```

The master brain loader.  
Everything points back to this.

---

## DYNASTY (Runtime)
```
Product/Dynasty/
└── RuntimeConfig_v1.0.json
```

Tells **Dynasty GPT**:
- which files to load  
- which modes exist (hybrid/gm/gameplay)  
- to enforce NHL 25 legal options only  
- to sync with Architect  

---

## ARCHITECT (Runtime)
```
Product/Architect/
└── RuntimeConfig_v1.0.json
```

Tells **Architect GPT**:
- you are the builder  
- you validate Canon, Trees, Engines  
- you enforce NHL 25 legality  
- you output iPhone-friendly commit instructions  

---

## ROLE SUMMARY
Architect GPT:
- Designs Canon, Trees, Engines
- Validates all strategy files
- Controls repo creation rules

Dynasty GPT:
- Generates gameplans
- Generates matchups
- Runs GM Mode decisions
- Uses Canon but cannot modify it

---

## VERSION
RepoMap_v1.0  
Generated for Leafs-Dynasty-AI-v5