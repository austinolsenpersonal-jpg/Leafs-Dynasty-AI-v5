# Product/Exports

This folder will store all generated export bundles created by either
Architect GPT or Leafs Dynasty GPT.

Exports are “snapshots” of the system at a point in time, including:

## Typical contents
- FullExport_v1.x.json (master state bundles)
- Gameplan exports
- Matchup packages
- Strategy baselines
- Canon snapshots
- Any combined JSON/MD packs needed for easy autoload

## Purpose
Exports are designed so:
- Dynasty GPT can autoload your full environment in new chats.
- Architect GPT can rebuild or validate the entire system via a single file.
- You can restore your project even if a chat fills up.

## Current status
- Placeholder only.
- Safe to regenerate.
- No active exports yet.