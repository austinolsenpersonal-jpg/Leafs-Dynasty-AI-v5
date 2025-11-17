# Leafs Dynasty AI – Modules Upgrade Pack v5.2

Author: Leafs Architect GPT  
Date: 2024-12-27  
Scope: Dynasty GPT behavioural, matchup, and gameplay systems upgrade  
Status: Approved by Architect

This document defines the official v5.2 upgrade for Leafs Dynasty AI modules. It extends the existing v5.0.1 Reliability Patch and NHL 25 Knowledge Pack v1.0 without breaking Canon or NHL 25 legality.

---

## 1. Goal of v5.2

- Improve post-patch NHL 25 behaviour modelling.
- Tighten matchup-specific tactical advice (e.g., Detroit chaos style).
- Add timing-aware system switching (when to change forecheck, breakout, pressure).
- Align sliders philosophy with the user’s real-world play style.
- Reduce false QA/validation flags when using matchup-specific overrides.
- Tailor advice to the user’s actual platform (cloud Series version on Xbox One S).

v5.2 is an additive layer. It does not replace Canon or core StrategyTrees.

---

## 2. Modules Touched in v5.2

- M81 – Controls & Inputs
- M82 – Settings & Sliders Map
- M84 – Patch-Aware Behavior
- M86 – Tactics Translator
- M88 – QA & Menu Mapper
- M89 – Platform Check
- Reliability Patch – upgraded from v5.0.1 to v5.2
- Sliders Package – Sliders_v2.0 profile
- Opponent Packs – new archetype extensions (DET and others)

---

## 3. M81 – Controls & Inputs (Upgrade)

**Intent:** Align controller advice with post-patch skating, cutbacks, and cycle-heavy offense.

### v5.2 Extensions

- Emphasize:
  - Lateral cutbacks at offensive blue line.
  - Half-wall delay moves and curl-backs.
  - Weak-side curls to open cross-ice seams.
  - Short give-and-go sequences at the dots.
- Entry logic:
  - Prefer controlled entries with delay → trailer support over straight-line rushes.
  - Teach Dynasty GPT to recommend “cutback + middle drive” instead of high-risk wide rushes.
- Output behaviour:
  - When giving gameplay advice, reference cutbacks, curl-backs, and delay plays as primary tools for Lines 1 and 2.

No change to button mapping; this is behavioural guidance only.

---

## 4. M82 – Settings & Sliders Map (Upgrade)

**Intent:** Introduce Sliders_v2.0 tuned for the user’s style and current AI behaviour.

### v5.2 Extensions

- Add a new named slider profile: `Sliders_v2.0_AllStar_Austin`.
- Philosophy:
  - Slightly increase pass accuracy (to support clean breakouts under pressure).
  - Slightly reduce CPU aggression and CPU forecheck pressure (to keep chaos manageable).
  - Ensure realistic but not overpowered rebounds and puck pickups.
- Dynasty GPT guidance:
  - When the user asks about sliders, default to recommending `Sliders_v2.0_AllStar_Austin`.
  - Mark previous slider suggestions as “legacy” when conflicting.

Exact numeric values to be defined in a future JSON file (`Product/Config/Sliders_v2.0_AllStar_Austin.json`).

---

## 5. M84 – Patch-Aware Behavior (Upgrade)

**Intent:** Update internal assumptions to match post-patch NHL 25 behaviour.

### v5.2 Extensions

- Recognize:
  - Adjusted forecheck and neutral-zone AI behaviour.
  - Updated PK diamond rotations and point-lane coverage.
  - Tweaked puck pickup responsiveness and battle outcomes.
  - Goalie rebound logic changes (fewer “free” rebounds in some spots, more in others).
- Dynasty GPT must:
  - Reference patch-adjusted tendencies when giving PK, forecheck, and breakout advice.
  - Avoid suggesting old tactics that relied on pre-patch AI weaknesses.

---

## 6. M86 – Tactics Translator (Upgrade + Archetypes)

**Intent:** Add opponent archetype-specific logic so matchup gameplans are more accurate.

### v5.2 Extensions

Add archetype definitions (examples):

- DET – Chaos Forecheck / Weak Side Lock:
  - High forecheck, high pressure, weak-side lock, heavy collapse.
  - Best counters: 1–2–2 Passive → early 2–3 forecheck, Strong Side Slant + Close Support, trap slider timing.
- WSH – Ovechkin Shooting / Left-Side Threat:
  - Diamond PP with left-circle one-timer bias.
  - Best counters: tighter PK box, lane denial, specific weak-side coverage.
- BOS – Heavy Point Cycle:
  - D-to-D cycles, point shots through traffic.
  - Counters: Staggered, Protect Net triggers, shot lane blocking.
- FLA / CAR – Relentless Forecheck:
  - Two-man pressure, deep cycle.
  - Counters: Close Support, Leave Zone Early situational use, earlier NZ switches.

Future modules may add more teams; v5.2 establishes the framework and at least a DET-focused archetype.

---

## 7. M88 – QA & Menu Mapper (Upgrade)

**Intent:** Reduce false validation flags when the user uses matchup-specific overrides.

### v5.2 Extensions

- Add awareness of:
  - Matchup gameplans stored under `Product/Dynasty/Matchups/`.
  - Game-specific overrides (e.g., trap slider, forecheck, breakout type).
- New rule:
  - If a setting matches a currently active matchup gameplan, do NOT flag it as a Canon violation.
- Confidence logic:
  - Distinguish between “Canon mismatch” and “Matchup override”.
  - Only warn if a setting is neither Canon nor defined in the active matchup file.

---

## 8. M89 – Platform Check (Upgrade)

**Intent:** Tailor timing and control advice to cloud-streamed Series version on Xbox One S.

### v5.2 Extensions

- Assume:
  - Slight input latency.
  - Minor visual delay in fast transitions.
- Dynasty GPT must:
  - Recommend simpler outlet options under heavy pressure.
  - Allow slightly earlier input timing for passes, shots, and poke checks in descriptive advice.
  - Avoid tactics that rely on frame-perfect dekes or hyper-precise timing.

This is a soft behavioural adjustment only; no Canon changes.

---

## 9. Reliability Patch – v5.2 Extension

**Base:** Leafs Dynasty Reliability Patch v5.0.1.

### New v5.2 Features

- Timing-Gated System Switching:
  - Add rules like “Suggest 2–3 forecheck earlier vs high-pressure chaos teams” and “Protect Net for 2–3 shifts when pinned.”
- Trap Slider Logic:
  - Add explicit guidance for when to increase/decrease the trap slider based on score, momentum, and opponent archetype.
- Breakout Switching:
  - Encode rules for when to swap between Stay Wide, Close Support, and Leave Zone Early.
- NZ Switching:
  - Introduce triggers for 1–3–1 vs rush-heavy teams and 1–2–2 Red vs traditional attacks.

All new rules must remain consistent with Canon strategies and available NHL 25 options.

---

## 10. Sliders_v2.0 Package (Definition Stub)

This spec authorizes a future config file:

- Path (proposed): `Product/Config/Sliders_v2.0_AllStar_Austin.json`
- Purpose:
  - Hold all gameplay slider values for the user’s preferred difficulty and style.
  - Used by Dynasty GPT as the default recommendation.

v5.2 does not define the numeric values here; it defines the intent and reference.

---

## 11. Opponent Matchup Packs

This spec formally recognizes Matchups folder usage:

- Folder: `Product/Dynasty/Matchups/`
- Each matchup file (e.g., `2024-12-27_vs_DET_Gameplan.md`) is considered an authoritative source for:
  - Per-game system overrides.
  - Slider deviations.
  - Matchup targeting rules.
- v5.2 behaviour:
  - Dynasty GPT should read matchup files as valid context and not treat their overrides as Canon violations.

---

## 12. Implementation Notes

- v5.2 is additive and backward compatible with:
  - Canon files under `Product/Canon/`
  - StrategyTrees under `Product/StrategyTrees/`
  - Engines under `Product/Engines/`
  - Existing RuntimeConfig files
- Future work:
  - Add JSON-level configs for sliders and modules if required.
  - Add more opponent archetypes as the season progresses.

End of v5.2 Modules Spec.