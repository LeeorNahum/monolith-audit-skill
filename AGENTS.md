# Maintenance contract: monolith-audit

Rules for editing this skill. User-facing guidance lives in `SKILL.md`. `README.md` is the human skim layer.

## File roles

| File | Role |
| --- | --- |
| `SKILL.md` | The build-or-audit methodology: scope, grounding, cross-checking, subagent confirmation, layer coverage, and close-out |
| `README.md` | Short human summary |

## Editing

- Keep it manual-only. There is no frontmatter flag for this: manual-only behavior must live entirely in the `description` text (it already states the skill is strictly manual and must only be invoked by name). Never add a frontmatter key outside the six the specification defines to try to enforce this.
- Keep it generic and placeholder-only. No real repo, vendor, provider, protocol, or project names belong in `SKILL.md`. Project-specific anchors (a docs URL, a directory to focus, a stack) live in the prompt that invokes the skill, never here.
- Describe the function of any supporting tool generically: an agent-skills bridge generator, a skill sync, a design-coherence pass. Never name a specific sibling skill or product.
- Keep `SKILL.md` direct and short. This is a high-altitude methodology, not a tutorial. Prefer deleting a line over softening it.
- Bump `metadata.version` with semver whenever behavior changes.
- Quote every frontmatter string value. Keys stay unquoted.
- No em dashes, and no semicolons used to join what should be separate sentences. Use commas, periods, parentheses, or "to".
- Capitalized bullets, parallel phrasing.

## Before finishing

- No real repo, vendor, or project names snuck into `SKILL.md` or `README.md`.
- Manual-only stance still lives only in the `description` text, never as a frontmatter key.
- `metadata.version` bumped if and only if behavior changed.
- `README.md` matches the actual file layout.
