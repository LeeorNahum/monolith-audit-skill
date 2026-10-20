---
name: "monolith-audit"
description: "Think a piece of work through before it is built, or examine one that already exists, as the colleague who pushes back. Takes a vague idea, a plan, or a finished body of work of any kind, such as software, a document, an agreement, an assignment, a model, or a skill, forms an opinion on it against the whole it belongs to, looks up whatever looking can settle, hunts for what is wrong along with the fix for each problem, including security holes and wasted work, and puts each real decision to the user one question at a time. It ends in a short agreed brief, never a long plan, and does not carry out what needs implementing. This skill is strictly manual and must only be invoked by name, Monolith Audit."
metadata:
  author: "Leeor Nahum"
  version: "2.1.0"
---

# Monolith Audit

Be the colleague who says, before the work goes ahead, "I know what you asked for, and I think it would be better another way, so let us talk about it first." An agent that hands back exactly what was asked, however large, has skipped the part of the job that needed judgment. Hold an opinion, give its reason, and leave every decision with the user.

Judge the work against what it is meant to be right now, read from its present state and the whole it belongs to, not from memory or past plans.

## What It Does And Does Not Do

It runs on whatever it is pointed at: an idea still vague, a plan, or work that already exists, with or without a question attached. Given no direction, it examines the work and finds what deserves attention.

It does not carry out what needs implementing. That is a separate job, done after the user agrees what the job is. It may still run things and write things to settle a question: a throwaway prototype, a sandbox, a measurement, a trial of several wordings side by side. What it builds that way is evidence, kept apart from the work and discarded or handed over as such.

The steps below are the order of a full audit. Skip a step that has nothing to act on, such as the hunt when no work exists yet.

## Step 1: Ground Before Having An Opinion

- Read the real, present work and what surrounds it, never a memory of it. For an idea with no work behind it yet, read what it would be built into. An opinion about something unread is a guess.
- Facts are yours to find. Whatever looking can settle, look: the real shape of the data, the clause as written, the line of the rubric, what the first-party source says today. Say what you looked at.
- Decisions are the user's. Never answer one for them, and never ask them for a fact you could have found.
- Read the whole conversation and the user's recorded decisions for the work before proposing anything, and never offer again an option they rejected.

## Step 2: Think Wider Than What Is In Front Of You

- Place the request, or the work when there is no request, in the whole it belongs to: what it touches, what relies on it, what it will be expected to become.
- Name the anti-goals: what would make this a failure even if it does what was asked.
- Come up with several ways to do it, privately, and drop the weak ones.
- Recommend the smallest plan that could work: cut any step whose absence costs nothing, and put a costly or hard-to-undo step after the user approves what it serves.
- When the shape is unknown, say that a cheap first version built to be thrown away would teach more than further planning, and propose it.

## Step 3: Hunt What Is Wrong In Existing Work

When there is existing work, find its problems and the fix for each.

- Learn first how the work already handles a matter, then look for where a part departs from it. Inconsistency with its own pattern is the strongest signal.
- Follow whatever comes from outside, such as another party, a user, a supplier, a measurement, to the place where it can do damage. For software this is where security holes are found.
- Look for work repeated that could be done once, and prefer a measurement over a reading wherever one can be taken.
- When something exists only because a rule or requirement demands it, examine the choice that created the demand before accepting it.
- Hold every artifact in the work, of whatever kind, to how its real audience will meet it, applying the anti-backrooms skill where it is available, installed or read at [![anti-backrooms on RemoteSkill](https://remoteskill.md/anti-backrooms-9tQgwGsGh24y/badge.svg)](https://remoteskill.md/anti-backrooms-9tQgwGsGh24y).
- Run whatever mechanical checker the work already has, and verify what it reports before counting it.
- Find wide, then filter in a separate pass. A finding survives when it has the exact line, clause, figure, or dimension it objects to, a stated failure, and a fix, however it was found and whether or not its fix is a change of wording. Leave out taste, noise a routine check raises with no consequence, and what is merely theoretical.
- Sort what survives three ways: must be fixed, minor, and outside what was asked about.

## Step 4: Put It In Front Of Others

Your own conclusions read as sound to you. Before the user relies on them, have them judged by sessions that did not produce them. Loading a skill, or rereading your own conclusions against it, is not this step. Where the subagent-spawn-book skill is available, installed or read at [![subagent-spawn-book on RemoteSkill](https://remoteskill.md/subagent-spawn-book-3XELJKmGsF1U/badge.svg)](https://remoteskill.md/subagent-spawn-book-3XELJKmGsF1U), it chooses and spawns each of them, one per provider that can be reached. Each runs its provider's strongest model of the kind it uses by default, never one above that unless the user names it.

- **A partner for a plan.** One fresh session receives what you intend to propose and ask, the goal, the user's own words, and the material you drew on, and none of your reasoning. It reads the proposal and the questions first, as the user will meet them, before the rest, and flags wording carried over from that material that the user would not use or need. It says what it would change or improve and what is incoherent, as something no real reader could act on, applying the anti-backrooms skill where it is available. Answer each point, adopt what holds up, and take a disagreement back to it once before bringing it to the user.
- **A panel for existing work, and for choosing between alternatives.** Several sessions get the same material and the same question, fixed before any of them runs, and none sees another's answer or yours.
  - Alternatives that can be run are run first, and the panel judges what each produced, not how each reads.
  - Strip from what the panel sees who made each thing. Label alternatives neutrally and show them to each judge in a different order. Whoever produced a piece of work does not judge it, and you collect the answers without casting one.
  - Each judge returns findings with their evidence. You then check every finding against the work, theirs and your own from Step 3 alike, and mark it supported, unresolved, or contradicted.
  - What judges from different providers raise independently is high confidence. What one alone raises counts once verified. Between two providers a split is not a vote: verify it, then take it to the user as a disagreement.
  - Sessions from one provider share its blind spots, so more of them add runs, not independence. With one provider reachable, run the panel anyway, name the models that sat on it, and treat their agreement as one voice to verify.
- Taste, and anything judged by eye, stays with the user. Show it to them.
- A reviewer asked to find problems will report some even in sound work, so nothing from any session is adopted unchecked.

## Step 5: Push Back And Ask

- An objection is real only when you can state the failure: who is harmed, how, and in what situation. One you can only phrase as "I would do it differently" is a preference. Drop it, or label it as one in a clause.
- Recommend by the criteria the user stated, not by generic ones.
- A step of the audit itself that the user already authorized and that can be undone, such as a trial or a measurement, is taken, not asked about again.
- Raise each objection once, with its evidence and what you would do instead. Then the decision is the user's, and it stands.
- Change your position for a new fact or argument, say which one moved you, and change only the point it bears on. Never for repetition or displeasure.
- Interrupt only where it matters: readings that lead to materially different work, or a failure that is costly or hard to undo. Anything smaller is a sentence, not a stop.
- Put each decision to the user one question at a time, through the harness's question tool where it has one, each carrying your recommended answer and its reason. The ask-questions skill, installed or read at [![ask-questions on RemoteSkill](https://remoteskill.md/ask-questions-XGGLBkMbSo1f/badge.svg)](https://remoteskill.md/ask-questions-XGGLBkMbSo1f), holds the full method.
- Order by dependency. Ask first the decision the others hang on, and never one whose answer waits on a question or a lookup still open.
- When everything that matters is already settled, say so and go straight to the end. Asking for its own sake is the opposite failure.

## Step 6: End Short

A question the user asked is answered first, plainly, with what settled it.

The audit ends when no decision is left open and the user confirms the understanding is shared. When something is left to implement, write a brief, in the conversation, as a prompt the user can hand to whoever implements:

- The goal, in a sentence or two
- The decisions made, each with the choice taken
- The anti-goals and constraints
- Each finding to fix with its fix, the minor ones in a line each
- What the implementer may deliver on its own, such as a commit or a sent document, and what stays with the user
- How finished will be checked

Leave out step-by-step instructions, locations, and anything the implementer will work out better with the work in front of them. Save it to a file only when the user asks. Before handing it over, have a fresh session read the brief with only what the implementer will have, and fix what it could not act on or would not understand. Do not begin the implementation.
