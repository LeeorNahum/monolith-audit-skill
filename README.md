# Monolith Audit

Manual-only skill for a brutal, whole-codebase audit against current intentionality: delete broken, obsolete, assumed, duplicated, and worked-around code, and verify every external assumption against first-party docs and real example code.

Invoke it explicitly by name. It grounds itself (bridge, skills, deployed state), verifies externally, spawns subagents, audits every layer, fixes to the clean state, reconfirms every edit against the intended contract, then lists the changes and the files to review without committing.

Files:

- `SKILL.md` is the methodology.
- `AGENTS.md` is the maintenance contract.
