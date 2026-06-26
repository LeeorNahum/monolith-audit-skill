# Monolith Audit

Manual-only skill for running a brutal, whole-codebase audit to enforce present-day correctness, whether building or reviewing. Ground in the live code, verify every external assumption against first-party docs and real example code, and remove or never introduce anything broken, obsolete, assumed, duplicated, or worked-around.

Invoke it explicitly by name. It runs whole-repo when bare, or appended to a named task or focus, where it holds that task and its blast radius to the same uncompromising standard so the work lands right in one pass. The audit grounds itself, cross-checks externally, spawns subagents, covers every layer, builds or fixes to a clean state, and reconfirms every edit against the intended contract. In a pure review it lists the changes and files to review without committing; appended to a build task it follows the delivery that task defines.

Files:

- `SKILL.md` is the methodology.
- `AGENTS.md` is the maintenance contract.
