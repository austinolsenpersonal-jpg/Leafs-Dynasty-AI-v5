Leafs Dynasty – Repo Structure Plan (v1.0)

This repository is designed for two GPTs:
1. Architect GPT – handles schemas, canon, exports, strategy trees.
2. Dynasty GPT – handles gameplans, GM logic, matchups, coaching.

Both GPTs share the same Canon and systems, but each uses its own folder so they never overwrite each other.

------------------------------------------------------------
TOP-LEVEL FOLDERS
------------------------------------------------------------

ArchitectAI/
- Workspace for Architect GPT only.
- Stores: strategy trees, canon versions, JSON schemas, templates, config files.
- Dynasty GPT never writes here.

DynastyAI/
- Workspace for Dynasty GPT only.
- Stores: gameplans, matchups, sliders, GM planning, coaching logic.
- Architect GPT never writes here.

Shared/
- The “Source of Truth” used by BOTH GPTs.
- Stores: Canon, systems, forecheck/NZ/DZ files, PP/PK, slider maps.
- Dynasty GPT reads these but never modifies Canon.
- Architect GPT is the only one allowed to update Canon.

Exports/
- Used for handoff between GPTs.
- Architect writes exports.
- Dynasty loads exports.
- Holds: full exports, gameplans, snapshots.

Docs/
- Human-readable guides, notes, explanations.
- Has no effect on the AI engines.

------------------------------------------------------------
RESPONSIBILITY SPLIT
------------------------------------------------------------

Architect GPT:
- Writes: ArchitectAI/, Shared/, Exports/, Docs/
- Reads everything.
- Controls Canon.
- Does NOT write into DynastyAI.

Dynasty GPT:
- Writes: DynastyAI/, Exports/
- Reads: Shared/, Exports/
- Does NOT modify Canon.
- Does NOT write into ArchitectAI.

------------------------------------------------------------
SETUP ORDER FOR NEW REPO
------------------------------------------------------------

1. Create these folders:
   ArchitectAI/
   DynastyAI/
   Shared/
   Exports/
   Docs/

2. Add small README files into ArchitectAI/ and DynastyAI/.

3. Place your full export JSON (FullExport_v1.0.json or newer) inside:
   Exports/FullExports/

4. In Architect GPT:
   Tell it: Canon lives in Shared/, Architect works in ArchitectAI/, exports go to Exports/.

5. In Dynasty GPT:
   Tell it: Read Canon from Shared/, work only in DynastyAI/, load exports from Exports/.