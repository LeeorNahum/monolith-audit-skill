---
name: "monolith-audit"
description: "Build or audit a body of work to rigorous, present-day correctness: ground in the live code, verify every external assumption at the source, and eliminate or never introduce anything broken, obsolete, duplicated, incoherent, or worked-around. Runs whole-repo when invoked bare, or appended to a specific task or focus (a feature, fix, subsystem, surface, or file set), where it holds that task and everything in its blast radius to the same standard so the work is done right in one pass rather than patched and audited later. This skill is strictly manual and must only be invoked by name. When invoked, load this skill and follow it for deep, whole-product correctness, cleanliness, and coherence work across backend, data, APIs, protocols, frontend, UI, UX, copy, configuration, environment contracts, integration points, and product flows, or for self-critical building and rewrites validated against up-to-date, authoritative references."
metadata:
  author: "Leeor Nahum"
  version: "1.2.0"
---

# Monolith Audit

Treat this work as if you are accountable for every line in the repository, whether you are building something new or reviewing what already exists. Your benchmark is *current intentionality*: what the product is meant to be right now, read directly from the present code and contracts on the working branch, not from memory, plans, or past intent. Remove, and never introduce, code that is broken, outdated, assumed-but-wrong, duplicated, unnecessary, or surviving as a leftover workaround. When done, every layer you touched is accurate, essential, and clearly connected to the live contract.

This is intensive and uncompromising in both modes. No corner is skipped, no layer is assumed clean, no finding is left unresolved:

- Read widely and deeply across the present code, every reference it points to, and the branches.
- Verify every detail from first principles and at the source, never from memory.
- Spawn subagents and specialist checkers for parallelism, context isolation, or niche domains. Do not rely on a single context window.
- Anticipate downstream effects: build and fix root causes, not symptoms.

## Scope: Build Or Audit, Whole Repo Or A Named Focus

This skill runs in two modes with the same uncompromising rigor in both.

- No focus: audit the entire repository, every layer, end to end.
- A named focus, the task appended to the invocation (a feature, fix, subsystem, surface, or file set): apply this same rigor to that focus and everything in its blast radius, the callers it touches and the contracts it depends on, still judged against the whole product’s current intentionality. Ground and verify before you build, hold every new line to the same standard as the code it joins, and audit as you go rather than patching first and cleaning up later. Doing the task this way means doing it right in one pass.

Scale Step 1 grounding to the mode. A whole-repo run grounds the entire system; a focused run grounds only what its task depends on and deploys, and skips stage-wide promotion the task does not need. Every other step applies in full at the focus’s scope: verify at the source, confirm with subagents, build or fix to the contract, and reconfirm after editing.

## Step 1: Fully Ground Your Work

Align your baseline with the true, live, running system and the rules you will apply:

- Ensure your environment matches the current state of the repository and is in sync with the actual codebase and tools in use. Do not proceed based on outdated files or stale assumptions
- Review documentation and environment details to confirm you are working with current and reliable information. Avoid acting on information you have not directly checked
- Pay close attention to the deployment environments and runtimes in use so your audit or build reflects what is truly active in production, staging, and development. Never assume local code matches what is deployed
- Read the real and present code. Ignore planning, wishlists, and design history. Your reference is only today’s code and the contracts explicitly written in the repo. Where code, contract, or deployment disagree, the intended contract in the code wins and you surface the discrepancy

## Step 2: Cross-Check Against First-Party Sources

Verify the present code against authoritative documentation for every service it touches, and correct what has drifted:

- For each external API, library, provider, platform, or protocol in use, open the current official first-party docs, never memory and never third-party summaries, and check the code against them.
- Confirm the interfaces, shapes, and contracts the code assumes still exist and behave as used. Flag and correct anything deprecated, removed, renamed, or misused.
- Seek working example code and reference implementations for ambiguous or critical behaviors, because prose docs often leave key details unstated.
- Treat as a defect any assumption the canonical docs or examples do not fully support.

## Step 3: Apply All Installed Skills

- Read every installed skill, system-wide and in any nested tree, from top to bottom, including every reference file it carries. Bias hard toward loading: read all of them in full, not a curated subset, because reading deeply is cheap and acting on a topic blind is not.
- Execute all of their rules, especially the design, naming, and maintenance rules that touch the layers you are working in.
- Apply the user-facing and design-coherence checks to all text, journeys, UI, and UX, walking a real end-to-end scenario.

## Step 4: Confirm With Subagents

- Recursively assign subagents to independently verify complex, cross-cutting, or niche findings.
- Separate the surface among agents for parallel, unbiased evaluation. No single context is comprehensive enough for a true monolith pass.
- Only claim a finding with direct evidence: a file, a first-party doc, or a reproduced interaction.

## Step 5: Cover Every Layer In Depth

Vigilantly check, as you build and as you review, for code that is broken, obsolete, unverified, dead, duplicative, patched, or otherwise unsound across:

- Backend logic and contracts
- Data models and schema (look for drift between schema and usage)
- HTTP APIs and their actual and published contracts
- Protocol servers, transports, and handshakes
- Authentication, identity, and capability checks
- Environment contracts and stage isolation
- Background work, failure modes, and retries

For each change, map every upstream and downstream caller, the possible failures, and what future maintenance will assume about the behavior.

## Step 6: Build To The Present Standard

- Build new work, and rewrite every defect or gap, toward the current intended contract, not a workaround or a compatible shim.
- Tear out every workaround whose original reason no longer exists, and add none. Leave no orphaned workaround that might mislead a future reader.

## Step 7: Reconfirm After Edits

After applying changes, do not move on. Re-read every changed file and its callers:

- Confirm the change matches the intended contract, introduces no new smell, and aligns with installed skill rules and first-party documentation.
- Spawn a fresh subagent or checker pass over the edited areas if the change was non-trivial.
- Catch regressions, partial fixes, and newly exposed issues before declaring a layer clean.

## Step 8: Close Out

Match delivery to the mode and to what the invoking task authorized:

- Reviewing existing work with no mandate to change it: make zero commits and no irreversible changes. Leave every diff and note for the user, summarize each finding with its rationale and affected files, and finish with a plain list of files to review. Nothing is settled until the user confirms or discards each change.
- Building or fixing under a task that owns its delivery: do the work to this standard in one pass, follow the verification and promotion process that task defines, and commit only as it directs. Leave nothing half-done and no new workaround behind.
- Either way, reconfirm before declaring done, and never make an outward-facing or irreversible change the user has not sanctioned.

Run this with absolute thoroughness and no tolerance for partial or low-impact work. Whether you are building or auditing, do it right the first time: exterminate accidental complexity, legacy deadweight, and every violation of present best practices, reconfirming at every stage until the product is truly clean.
