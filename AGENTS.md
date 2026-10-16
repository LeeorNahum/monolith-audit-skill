# Maintenance contract: monolith-audit

Rules for editing this skill. User-facing guidance lives in `SKILL.md`. `README.md` is the human skim layer.

## File roles

| File | Role |
| --- | --- |
| `SKILL.md` | The auditing methodology: grounding, thinking wider, pushing back, asking, hunting problems, outside judgment, and the closing brief |
| `README.md` | Short human summary |

## Editing

- Keep it manual-only. There is no frontmatter flag for this: manual-only behavior must live entirely in the `description` text (it already states the skill is strictly manual and must only be invoked by name). Never add a frontmatter key outside the six the specification defines to try to enforce this.
- The skill thinks, examines, pushes back, and agrees a brief. Carrying a stated job through to a finished deliverable belongs to the monolith-implement skill. Keep that boundary in these words: the skill does not carry out what needs implementing. Never call it read-only, because it may run and write whatever settles a question, such as a prototype, a sandbox, or a trial of wordings.
- It is an optional step. Nothing in it may read as required before implementing, and it must work with no direction at all, examining the work and finding what deserves attention.
- It has opinions. Never soften a line into neutral facilitation, and never let it become a critic that objects for its own sake: every objection needs a stated failure, and a preference is labeled or dropped.
- The closing brief stays short. Never grow it into a step list or a specification, since the implementer works those out with the work in front of them.
- Keep it usable for any deliverable. Software is one case, named only where a line needs it. When a new line would only make sense for code, generalize it.
- Keep it generic and placeholder-only. No real repo, vendor, provider, protocol, product, or project names belong in `SKILL.md`. Anchors for one piece of work live in the prompt that invokes the skill.
- The skill works with nothing else loaded. It states its own minimum for asking (one question at a time, with a recommendation) and for outside judgment (the partner, the panel, and how their answers are combined). Three sibling skills are named and linked by their public share addresses as the fuller method where they are available, never as a requirement: ask-questions, subagent-spawn-book, and anti-backrooms. Name no other sibling skill or product in `SKILL.md`.
- The steps are in the order a full audit runs: ground, think wider, hunt, outside judgment, push back and ask, end. Asking comes after the hunt and the outside judgment because their results are what the questions are about.
- A finding is kept for its consequence and evidence, never dropped for how it was found or because its fix is a change of wording. For an agreement, an instruction set, or a skill, wording is where the defects are.
- Keep `SKILL.md` direct and short. This is a high-altitude methodology, not a tutorial. Prefer deleting a line over softening it.
- Bump `metadata.version` by the release-versioning skill's rules for skills. The version continues from the skill that carried this name before it, which is now monolith-implement.
- Quote every frontmatter string value. Keys stay unquoted.
- No em dashes, and no semicolons used to join what should be separate sentences. Use commas, periods, parentheses, or "to".
- Capitalized bullets, parallel phrasing.

## Before finishing

- No real repo, vendor, or project names snuck into `SKILL.md` or `README.md`.
- Manual-only stance still lives only in the `description` text, never as a frontmatter key.
- `metadata.version` bumped as the release-versioning skill requires.
- `README.md` matches the actual file layout.
