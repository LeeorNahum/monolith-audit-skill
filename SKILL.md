---
name: "monolith-audit"
description: "Build or audit a body of work to rigorous, present-day correctness: ground in the live code, verify every external assumption at the source, and eliminate or never introduce anything broken, obsolete, duplicated, incoherent, or worked-around. Runs whole-repo when invoked bare, or appended to a specific task or focus (a feature, fix, subsystem, surface, or file set), where it holds that task and everything in its blast radius to the same standard so the work is done right in one pass rather than patched and audited later. This skill is strictly manual and must only be invoked by name, Monolith Audit. When invoked, load this skill and follow it for deep, whole-product correctness, cleanliness, and coherence work across backend, data, APIs, protocols, frontend, UI, UX, copy, configuration, environment contracts, integration points, and product flows, or for self-critical building and rewrites validated against up-to-date, authoritative references."
metadata:
  author: "Leeor Nahum"
  version: "1.6.1"
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

Scale Step 1 grounding to the mode. A whole-repo run grounds the entire system. A focused run grounds only what its task depends on and deploys, and skips stage-wide promotion the task does not need. Every other step applies in full at the focus’s scope: verify at the source, confirm with subagents, build or fix to the contract, and reconfirm after editing.

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

## Step 4: Confirm With Adversarial Subagents

The builder never grades its own work. Every pass of this skill runs at least two independent checks before anything is called done, and waits for each check to return before ending the turn, because a session that ends while a critic is still running has skipped it:

- **An adversarial critic from a different provider than the builder**, or that provider's next-best model when only one provider is reachable, chosen and spawned by the subagent-spawn-book skill, installed or read at [![subagent-spawn-book on RemoteSkill](https://remoteskill.md/subagent-spawn-book-3XELJKmGsF1U/badge.svg)](https://remoteskill.md/subagent-spawn-book-3XELJKmGsF1U), and told plainly that its job is to find what is wrong, not to validate. It receives the goal, the changed files and their callers, every instruction the builder was given, the skills, the AGENTS.md files, the user's own words, and the first-party docs from Step 2. It does not receive the builder's justifications for its choices, so it judges the work against the goal rather than against the story told about it. The builder gives its reasoning in the answer round. It returns a ranked list with the evidence for each finding, and where it sees a better shape for the work than the one built, it says so as a proposal. A critic from the builder's own model shares its blind spots, so the distance is the point.
- **A separate anti-backrooms pass over everything the change produces**, by a model that can see the rendered result where there is one. It applies the anti-backrooms skill, installed or read at [![anti-backrooms on RemoteSkill](https://remoteskill.md/anti-backrooms-9tQgwGsGh24y/badge.svg)](https://remoteskill.md/anti-backrooms-9tQgwGsGh24y), judges the result rather than the source, and reports what reads wrong, not what the code says.
- Recursively assign further subagents to complex, cross-cutting, or niche findings, and split the surface among them. No single context is comprehensive enough for a true monolith pass.
- Only claim a finding with direct evidence: a file, a first-party doc, or a reproduced interaction. The builder answers every finding and every proposal in writing, and a refusal with a reason is a valid answer. A finding read and not answered launders the decision.
- The answer goes back to the same critic, resumed by its session id so it keeps its context, and it says which findings it withdraws and which it holds. Two rounds settle most disagreements. What is still held after that goes to the user as an open point, not silently dropped.
- Run this loop per unit of work, not once per release. Tell the critic to separate what blocks delivery from what should merely be recorded and, when it has a workspace it is authorized to write to, to keep one findings file there, adding each finding as it confirms it, verdict first, so a run that dies still leaves its report.
- Aim later rounds at the seams. Each unit is verified alone, so where two verified units meet is the part nobody has reviewed, and it is where the real defects live.
- Expect briefs to undercount. When a critic names several instances of a problem, ask why the rule was enforced per caller, and find the others. Prefer moving the rule to one place every caller must cross, such as a single record or gate, over adding the same check at one more place.

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
- Spawn a fresh adversarial critic over the edited areas if the change was non-trivial, chosen as in Step 4, and the anti-backrooms pass again over everything that changed.
- Catch regressions, partial fixes, and newly exposed issues before declaring a layer clean.
- Map every explicit intention and requirement the user stated to where it is met on each affected surface, integration, contract, and test, whether or not the user named that surface. A requirement that is missing from any of those places is not done.

**Mutation-check the guards that support the verdict.** Assume some checks verify something adjacent to what they claim, because that failure is common and invisible. Ask of each check what would have to be true for it to pass while the thing it names is broken. Then, in an isolated test copy, break a guard, check that its test fails for that defect, and restore it. A surviving mutation exposes a gap in the test's evidence. Strengthen the test before trusting its claim, and retain any required runtime protection. Bound the run so a hang or resource failure remains a distinct result, not proof that the test caught the defect.

## Step 8: Close Out

Match delivery to the mode and to what the invoking task authorized:

- Reviewing existing work with no mandate to change it: make zero commits and no irreversible changes. Leave every diff and note for the user, summarize each finding with its rationale and affected files, and finish with a plain list of files to review. Nothing is settled until the user confirms or discards each change.
- Building or fixing under a task that owns its delivery: do the work to this standard in one pass, follow the verification and promotion process that task defines, and commit only as it directs. Leave nothing half-done and no new workaround behind.
- Either way, reconfirm before declaring done, and never make an outward-facing or irreversible change the user has not sanctioned.

Run this with absolute thoroughness and no tolerance for partial or low-impact work. Whether you are building or auditing, do it right the first time: exterminate accidental complexity, legacy deadweight, and every violation of present best practices, reconfirming at every stage until the product is truly clean.
