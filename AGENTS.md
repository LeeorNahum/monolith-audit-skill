# Maintenance contract: monolith-audit

Rules for editing this skill.

- Keep it manual-only. `disable-model-invocation: true` must stay; this skill is heavy and must never auto-load.
- Keep it generic and placeholder-only. No real repo, vendor, provider, protocol, or project names belong in `SKILL.md`. Project-specific anchors (a docs URL, a directory to focus, a stack) live in the prompt that invokes the skill, never here.
- Describe the function of any supporting tool generically: an agent-skills bridge generator, a skill sync, a design-coherence pass. Never name a specific sibling skill or product.
- Keep `SKILL.md` direct and short. This is a high-altitude methodology, not a tutorial. Prefer deleting a line over softening it.
- Bump `metadata.version` with semver whenever behavior changes.
- Capitalized bullets, no em dashes.
