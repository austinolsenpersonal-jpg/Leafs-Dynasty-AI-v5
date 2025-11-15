# Leafs Dynasty Systems

This repository contains the complete two-GPT ecosystem built by Austin Olsen for NHL 25 Franchise Mode:
- **Architect GPT** (systems builder, validator, Canon enforcer)
- **Dynasty GPT** (gameplay + GM assistant with matchup engine)

The repo is designed so BOTH GPTs stay synced, stable, and drift-free using one shared Canon foundation.

---

## 📁 Repository Structure

- **ArchitectAI/**  
  Core systems, validations, templates, strategy format rules.

- **DynastyAI/**  
  Gameplay engine, GM tools, matchup generator, coaching cards, daily ops.

- **Shared/**  
  Canon files, configuration indexes, rule maps, synced datasets.

- **Exports/**  
  Full export packages, bootstrap files, snapshots.

- **Docs/**  
  Guides, instructions, specifications for both GPTs.

---

## 🎯 Purpose

This repo is the **single source of truth** for:
- Strategy logic  
- Matchup generation  
- Canon v1.0+ rules  
- Lines and slider templates  
- Gameplan engine specifications  
- GPT instruction frameworks  
- Export/Import consistency  

All Dynasty and Architect GPT sessions pull from this repo to ensure:
- No drift  
- No mismatched tactics  
- Canon always matches real NHL 25 options  
- Stable gameplay + accurate gameplanning  

---

## 🚀 Usage

1. Architect GPT:  
   Reads/writes inside `/ArchitectAI`, `/Shared`, and `/Docs`.

2. Dynasty GPT:  
   Reads/writes inside `/DynastyAI`, `/Shared`, and `/Exports`.

3. Both GPTs load Canon from `/Shared/Canon_Index_v1.0.md`.

---

## 🔒 Canon

All strategy, tactic, and slider files in this repo follow:
- **NHL 25–accurate options only**  
- Trap scale (0–6)  
- Offensive/Defensive sliders (0–10)  
- Forecheck, NZ, DZ, Pressure, Breakout options that exist in the game  
- Zero legacy items from older NHL entries  

---

## 📌 Status

Repo initialized cleanly.  
Ready for Architect v7.0 and Dynasty v3.0 bootstrap files.