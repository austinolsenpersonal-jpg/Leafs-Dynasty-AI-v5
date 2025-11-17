# /FULL GAMEPLAN @ {{OPPONENT}} — TEMPLATE v2.0

_Date: {{GAME_DATE}}_  
_Starter: {{GOALIE_NAME}}_  
_Runtime: v2.3 • Canon v5.0 • Sliders v2.0 • Patch v5.2_

> NOTE: Replace all `{{PLACEHOLDER}}` tokens before saving as a report under `Reports/Gameplans/`.

---

## 0. SCOUTING SNAPSHOT

**Opponent:** {{OPPONENT}}  
**Archetype:** {{OPPONENT_ARCHETYPE}} (e.g., chaos forecheck, heavy cycle, rush, trap)  
**Record:** {{OPP_RECORD}} (L10: {{OPP_LAST10}})  
**Key Traits:**
- Forecheck: {{OPP_FC_TYPE}}  
- Neutral Zone: {{OPP_NZ_TYPE}}  
- DZ Strategy: {{OPP_DZ_TYPE}}  
- PP: {{OPP_PP_TYPE}}  
- PK: {{OPP_PK_TYPE}}  
- Goalie: {{OPP_G_GSTYLE}} (rebound-prone / positional / athletic)

**Toronto Focus Tonight:**
- Theme: {{GAME_THEME}} (e.g., “Control chaos”, “Exploit slow D”, “Own the neutral zone”)
- Win Condition: {{WIN_CONDITION}} (1–2 clear sentences)

---

## 1. TORONTO SYSTEMS (IN NHL 25 MENU ORDER)

### 1.1 Forecheck

**Start:** {{FORECHECK_START}}  
**Adjustments:**
- If opponent exits clean too easily → {{FORECHECK_ADJ1}}
- If trailing in 3rd → {{FORECHECK_ADJ2}}
- If protecting lead → {{FORECHECK_LEAD_MODE}}

Short note: {{FORECHECK_NOTES}}

---

### 1.2 Neutral Zone

**Start:** {{NZ_START}}  

**Why:**  
- {{NZ_REASON_1}}  
- {{NZ_REASON_2}}  

**Switch To:** {{NZ_SWITCH_MODE}} if:
- {{NZ_SWITCH_TRIGGER_1}}  
- {{NZ_SWITCH_TRIGGER_2}}  

---

### 1.3 Trap / Forecheck Slider (0–6)

**Slider Start:** {{TRAP_START}}  
- vs chaos teams: usually 2–3  
- vs slow/trap teams: usually 3–4  

**Adjustment Rules:**
- If getting pinned in DZ → **lower to** {{TRAP_LOWER}}  
- If stuck in NZ trap → **raise to** {{TRAP_RAISE}}  
- If protecting lead late → **set to** {{TRAP_LEAD}}  

Short note: {{TRAP_NOTES}}

---

### 1.4 Defensive Pressure

**Start:** {{D_PRESSURE_START}}  

**Curl-Shooter Patch:**
- If repeated curl-and-shoot from circles:
  - TEMP: set **Defensive Pressure → High Pressure** for 2 shifts  
  - Then revert to **Contain Puck**  

Short note: {{D_PRESSURE_NOTES}}

---

### 1.5 Defensive Strategy

**Start:** {{D_STRAT_START}}  

**Why:**  
- {{D_STRAT_REASON_1}}  
- {{D_STRAT_REASON_2}}  

**If hemmed in repeatedly:**
- Consider temporary switch to: {{D_STRAT_SWITCH}}  

---

### 1.6 Offensive Pressure

**Start:** {{O_PRESSURE_START}}  

**Rules:**
- Stay on Standard until:
  - You fully read opponent’s DN-zone coverage  
- Switch to Aggressive when:
  - You need sustained O-zone pressure  
- Drop to Conservative when:
  - Protecting a one-goal lead late  

Short note: {{O_PRESSURE_NOTES}}

---

### 1.7 Control Breakout

**Start:** {{CONTROL_BO_START}}  

**Usage:**
- Best vs: {{CONTROL_BO_VS}}  
- Avoid when: {{CONTROL_BO_AVOID}}  

Short note: {{CONTROL_BO_NOTES}}

---

### 1.8 Quick Breakout

**Start:** {{QUICK_BO_START}}  

**Triggers:**
- If opponent runs Puck Side Attack:
  - Prefer **Stay Wide**  
- If hemmed in:
  - TEMP: **Close Support**  
- If chasing game and opponent pinches:
  - **Leave Zone Early**  

Short note: {{QUICK_BO_NOTES}}

---

## 2. LINE STRATEGIES (0–10 SLIDERS)

> Scale: 0 = Carry / Cycle / Energy / No Block  
> 10 = Dump / Shoot / Energy Spend / Full Block

### 2.1 Line 1 — {{L1_NAME}}

**Strategy:** {{L1_STRAT}}  
- Carry/Dump: {{L1_CARRY_DUMP}}  
- Cycle/Shoot: {{L1_CYCLE_SHOOT}}  
- Efficiency/Energy: {{L1_EFF_ENERGY}}  
- Block: {{L1_BLOCK}}  

**Purpose:**  
- {{L1_PURPOSE_1}}  
- {{L1_PURPOSE_2}}  

---

### 2.2 Line 2 — {{L2_NAME}}

**Strategy:** {{L2_STRAT}}  
- Carry/Dump: {{L2_CARRY_DUMP}}  
- Cycle/Shoot: {{L2_CYCLE_SHOOT}}  
- Efficiency/Energy: {{L2_EFF_ENERGY}}  
- Block: {{L2_BLOCK}}  

**Purpose:**  
- {{L2_PURPOSE_1}}  
- {{L2_PURPOSE_2}}  

---

### 2.3 Line 3 — {{L3_NAME}}

**Strategy:** {{L3_STRAT}}  
- Carry/Dump: {{L3_CARRY_DUMP}}  
- Cycle/Shoot: {{L3_CYCLE_SHOOT}}  
- Efficiency/Energy: {{L3_EFF_ENERGY}}  
- Block: {{L3_BLOCK}}  

**Purpose:**  
- {{L3_PURPOSE_1}}  
- {{L3_PURPOSE_2}}  

---

### 2.4 Line 4 — {{L4_NAME}}

**Strategy:** {{L4_STRAT}}  
- Carry/Dump: {{L4_CARRY_DUMP}}  
- Cycle/Shoot: {{L4_CYCLE_SHOOT}}  
- Efficiency/Energy: {{L4_EFF_ENERGY}}  
- Block: {{L4_BLOCK}}  

**Purpose:**  
- {{L4_PURPOSE_1}}  
- {{L4_PURPOSE_2}}  

---

## 3. DEFENSIVE PAIRS (PINCH / SHOOT)

### 3.1 Pair 1 — {{D1_PAIR_NAME}}

**Strategy:** {{D1_STRAT}}  
- Pinch: {{D1_PINCH}}  
- Shoot: {{D1_SHOOT}}  

Role: {{D1_ROLE_NOTE}}

---

### 3.2 Pair 2 — {{D2_PAIR_NAME}}

**Strategy:** {{D2_STRAT}}  
- Pinch: {{D2_PINCH}}  
- Shoot: {{D2_SHOOT}}  

Role: {{D2_ROLE_NOTE}}

---

### 3.3 Pair 3 — {{D3_PAIR_NAME}}

**Strategy:** {{D3_STRAT}}  
- Pinch: {{D3_PINCH}}  
- Shoot: {{D3_SHOOT}}  

Role: {{D3_ROLE_NOTE}}

---

## 4. PERIOD-BY-PERIOD GAMEPLAN

### 4.1 1st Period — {{P1_THEME}}

**Keys:**
- {{P1_KEY_1}}
- {{P1_KEY_2}}
- {{P1_KEY_3}}

**No-go rules:**
- {{P1_NO_GO_1}}
- {{P1_NO_GO_2}}

---

### 4.2 2nd Period — {{P2_THEME}}

**Keys:**
- {{P2_KEY_1}}
- {{P2_KEY_2}}
- {{P2_KEY_3}}

**Target matchups:**
- {{P2_MATCHUP_1}}
- {{P2_MATCHUP_2}}

---

### 4.3 3rd Period — Situational Plan

**If tied:**  
- {{P3_TIED_PLAN}}

**If leading:**  
- NZ: {{P3_LEAD_NZ}}  
- DZ: {{P3_LEAD_DZ}}  
- Trap slider: {{P3_LEAD_TRAP}}  
- Pressure: {{P3_LEAD_PRESSURE}}  

**If trailing:**  
- NZ: {{P3_TRAIL_NZ}}  
- Forecheck: {{P3_TRAIL_FC}}  
- Trap slider: {{P3_TRAIL_TRAP}}  
- Double-shift line: {{P3_TRAIL_DOUBLE_SHIFT}}  

---

## 5. MATCHUPS & TARGETING

### 5.1 Opponent Forward Lines

**Line 1 — {{OPP_L1}}**  
- Threats: {{OPP_L1_THREATS}}  
- Counter: {{TOR_COUNTER_L1}}  

**Line 2 — {{OPP_L2}}**  
- Threats: {{OPP_L2_THREATS}}  
- Counter: {{TOR_COUNTER_L2}}  

**Line 3 — {{OPP_L3}}**  
- Threats: {{OPP_L3_THREATS}}  
- Counter: {{TOR_COUNTER_L3}}  

**Line 4 — {{OPP_L4}}**  
- Threats: {{OPP_L4_THREATS}}  
- Counter: {{TOR_COUNTER_L4}}  

---

### 5.2 Opponent Defense Pairs

**Pair 1 — {{OPP_D1}}**  
- Strengths: {{OPP_D1_STR}}  
- How to attack: {{OPP_D1_ATTACK}}  

**Pair 2 — {{OPP_D2}}**  
- Strengths: {{OPP_D2_STR}}  
- How to attack: {{OPP_D2_ATTACK}}  

**Pair 3 — {{OPP_D3}}**  
- Strengths: {{OPP_D3_STR}}  
- How to attack: {{OPP_D3_ATTACK}}  

---

## 6. SPECIAL TEAMS

### 6.1 Toronto PP vs {{OPPONENT}} PK

**Opponent PK Type:** {{OPP_PK_TYPE}} (e.g., Diamond, Passive Box)  

**Keys:**
- {{PP_KEY_1}}
- {{PP_KEY_2}}
- {{PP_KEY_3}}

**Primary play:** {{PP_PRIMARY_PLAY}}  
**Secondary option:** {{PP_SECONDARY_PLAY}}  

---

### 6.2 Toronto PK vs {{OPPONENT}} PP

**Opponent PP Type:** {{OPP_PP_TYPE}} (Shooting PP / Umbrella / 1-3-1)  

**Template Use:**  
- If Shooting PP → **use Shooting PP PK template**  
- If Umbrella → **use Umbrella PK template**  

**Keys:**
- {{PK_KEY_1}}
- {{PK_KEY_2}}
- {{PK_KEY_3}}

---

## 7. GOALIE GAMEPLAN — {{GOALIE_NAME}}

**Opponent goalie:** {{OPP_GOALIE_NAME}} — {{OPP_G_GSTYLE}}  

**Our Goalie:** {{GOALIE_NAME}}  

**Shot Profile vs Opponent Goalie:**
- Location focus: {{G_SHOT_LOC}}  
- Height: {{G_SHOT_HEIGHT}}  
- Rebounds: {{G_REBOUND_STRATEGY}}  

**For Our Goalie ({{GOALIE_NAME}}):**
- Track: {{G_TRACK_NOTES}}  
- Rebound control: {{G_OUR_REBOUND}}  
- Puck freezes: {{G_FREEZE_NOTES}}  

---

## 8. COACHING TRIGGERS (FAST SWITCHES)

**If hemmed in repeatedly:**
- Quick Breakout → {{TRIGGER_HEMMED_QB}}  
- D Strategy → {{TRIGGER_HEMMED_DSTRAT}}  

**If NZ trap is killing entries:**
- Trap slider → {{TRIGGER_NZ_TRAP_SLIDER}}  
- NZ strategy → {{TRIGGER_NZ_TRAP_STRAT}}  

**If offense stalls:**
- Offensive Pressure → {{TRIGGER_OFFENSE_PRESSURE}}  
- Forecheck → {{TRIGGER_OFFENSE_FC}}  

**If protecting a one-goal lead:**
- NZ → {{TRIGGER_LEAD_NZ}}  
- D Pressure → {{TRIGGER_LEAD_DPRESSURE}}  
- Trap slider → {{TRIGGER_LEAD_TRAP}}  

---

## 9. LIVE COACHING SAFETY RAILS (REMINDER)

- Do **not** change full 5v5 systems because of a single PP goal.  
- Avoid stacking High Pressure + 1–2–2 Aggressive + trap slider > 4 except in last 3 minutes (RED MODE).  
- Any extreme settings → **RED MODE**, max 2–3 shifts, then revert.  

---

_End of Gameplan Template v2.0_