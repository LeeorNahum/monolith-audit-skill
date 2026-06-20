---
name: "monolith-audit"
description: "Perform a rigorous, full-repo audit grounded in present-day intentionality: eliminate every broken, obsolete, duplicated, incoherent, or worked-around piece of code, and verify all external assumptions directly at the source. This skill is strictly manual. Invoke only by name for deep, whole-product correctness, cleanliness, and coherence reviews across backend, data, APIs, protocols, frontend, UI, UX, copy, configuration, environment contracts, integration points, and product flows, or for self-critical rewrites validated against up-to-date, authoritative references."
metadata:
  author: "Leeor Nahum"
  version: "1.0.0"
---

# Monolith Audit

Treat this audit as if you’re accountable for every line in the repository. Your benchmark is *current intentionality*: what the product is meant to be right now, directly reflected in the committed code and contracts, not in historical plans or past intent. Remove all code and artifacts that are broken, outdated, assumed-but-wrong, duplicated, unnecessary, or surviving as leftover workarounds. When done, every layer should be accurate, essential, and clearly connected to the live contract.

This is an intensive manual review. No corner is skipped, no layer is assumed clean, no finding is left unresolved:

- Read widely and deeply across the repo, references, and branches.
- Verify every detail from first principles, not memory.
- Spawn subagents and specialist checkers for parallelism, context isolation, or niche domains. Do not rely on a single context window for a full monolith sweep.
- Anticipate downstream effects: fix root causes, not just symptoms.

## Step 1: Fully Ground Your Audit

Align your review baseline with the true, live, running system and the rules you’ll apply:

- Sync your environment: refresh the agent-skills bridge for your coding tool, then regenerate it to guarantee all skills and rules are loaded.
- Update: pull all installed skills/submodules to their latest versions.
- Bring all branches current and promote deployments/runtimes for each stage: ensure what you audit matches what's actually deployed. Follow all approval processes before making any production-impacting moves.
- Ignore planning, wishlists, or design history. Your reference is only today’s code and the contracts explicitly written in the repo. If reality disagrees between code, contract, or deployment, the intended contract in the code wins.

## Step 2: Verify with First-Party Sources

Audit every assumption, convention, and framework usage by consulting direct, authoritative documentation:

- For each external API, library, provider, platform, or protocol in use, open the current, official first-party docs, not third-party summaries.
- Seek working example code and reference implementations for ambiguous or critical behaviors. Prose docs often leave key details unstated.
- Treat as a defect any interface, shape, or contract the code assumes that is not fully supported by the canonical documentation or examples.

## Step 3: Apply All Installed Skills

- Read every installed skill file, system-wide and in any nested directory tree, from top to bottom.
- Execute all rules, especially design, naming, and maintenance skills that touch the layers you’re auditing.
- Apply user-facing/design-coherence audits to all text, user journeys, UI, and UX components, walking a real end-to-end user scenario.

## Step 4: Confirm Findings with Subagents

- Recursively assign subagents to independently verify complex, cross-cutting, or niche findings.
- Separate the audit surface among agents to ensure parallel, unbiased evaluation. No single context is comprehensive enough for a true monolith review.
- Only claim a finding if you have direct evidence: a file, a first-party doc, or a reproduced interaction.

## Step 5: Audit Every Layer in Depth

Vigilantly search for code that is broken, obsolete, unverified, dead, duplicative, patched, or otherwise unsound across:

- Backend logic and contracts
- Data models and schema (look for drift between schema and usage)
- HTTP APIs and their actual/published contracts
- Protocol servers, transports, and handshakes
- Authentication, identity, and capability checks
- Environment contracts and stage isolation
- Background work, failure modes, and retries

For each possible change, map all upstream and downstream callers, possible failures, and what future maintenance will assume about this behavior.

## Step 6: Clean Up to the Present Standard

- For each defect or gap, rewrite towards the current intended contract, not a workaround or compatible shim.
- Tear out every workaround whose original reason no longer exists. Leave no orphaned workaround that might mislead future readers.

## Step 7: Reconfirm After Edits

After applying fixes, do not move on. Re-read every changed file and its callers:

- Confirm the edit matches the intended contract, introduces no new smell, and aligns with installed skill rules and first-party documentation.
- Spawn a fresh subagent or checker pass over the edited areas if the change was non-trivial.
- Catch regressions, partial fixes, and newly exposed issues before declaring a layer clean.

## Step 8: Wrap Up

- Make zero commits. Leave all work, diffs, and notes uncommitted for the user’s explicit review and discretion.
- Output a succinct, readable summary of recommended changes, with issue types and rationales.
- Finish with an unambiguous, plain list of files to review.

Execute this process thoroughly. A partial or non-critical audit risks institutionalizing accidental complexity.

- Never make any commit or irreversible change. All results, notes, and recommended diffs are left to the user's determination and review.
- Produce a terse, unambiguous summary of each proposed change or finding, its rationale, and affected files.
- Finish with a clear checklist and reading guide for user review. Nothing is done until the user has explicitly confirmed or discarded each change.

Run this process with absolute thoroughness and no tolerance for partial, incremental, or low-impact audits: your job is to exterminate accidental complexity, legacy deadweight, and every violation of present best practices, reconfirming the result at every stage until the whole product is truly clean.
