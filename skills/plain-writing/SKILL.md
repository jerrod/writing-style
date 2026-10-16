---
name: plain-writing
description: The "How to write" rules with before and after examples. Use whenever you write or edit prose anyone will read, including docs, READMEs, PRs, commit messages, comments, CLI messages and prompts.
---

## How to write

These rules cover everything you write: chat, docs, PRs, issues, commit messages, code comments, CLI messages, prompts and artifacts.

- Write the way you talk. If you wouldn't say it out loud, don't write it. Watch for inverted word order and written-only words like absorb, revamp, leverage, utilize, and "names" when it means references or lists.
- Say each thing once. One idea per sentence. Don't restate the heading, repeat a list from elsewhere, tack a second point on with "which", or use a colon subtitle.
- Use active voice. Name who does the thing. Write "The client confirms the use case", not "Confirmation of the use case".
- No origin stories. Delete, don't reword, every sentence about history, who's working on what, what's changing, due dates, who said what, where a doc came from, or why a thing exists. Anecdotes aren't evidence.
- Use plain words and active verbs. Drop jargon, shorthand the reader has to decode, double negatives, stacked modifiers, and filler like "actually", "in practice", "already" unless the timing is the point, and "any" when you mean "every".
- Talk to the reader. Write "you", not "the engineer". A list item says who does what, the way you'd say it to a teammate, not the way a policy reads.
- Write for anyone. Docs meant for a team name no people and don't assume the reader's current work.
- Stop when the point is made. Cut a last sentence that only says why, sums up, or offers more.

Leave data, quotes, code identifiers and test fixtures alone.

When someone asks you to fix the writing, read every line of every file, including artifacts. Don't sample or skim. Reread your own rewrites against these rules before you call it done.

## Before and after

| Before | Rule | After |
| --- | --- | --- |
| Engineering Scoping: Role, Checklist, Method | Colon subtitle | How engineers scope projects |
| TL;DR | Not spoken | The short version |
| Commit no number you can't defend. | Inverted word order | Don't commit to a number you can't defend. |
| The team lead stays accountable for the technical outcome. | Not spoken | The team lead answers for the technical result. |
| The client can absorb the change. | Written-only word | The client can handle the change. |
| Each question names the slide that raised it. | "Names" when it means references | Each question references the source slide. |
| Its real output is the list of gaps in the docs, which feeds the brief and the register. | Filler and a tacked-on "which" | What you want from it is the list of gaps in the docs. Feed them into the brief and the register. |
| Map the stack, system boundaries, model and compliance limits, volume, latency and ground truth. | Repeats the checklist below | Answer the checklist below. |
| Follow these steps on every project, and keep each output in the repo so later steps build on earlier ones. | Restates the heading, says why | Keep each step's output in the repo. |
| Each client responsibility names an owner with authority and the systems, data, SMEs and approvals. | Policy voice, no verb for the list | For everything the client owes you, name a person who can deliver it, and the systems, data, experts and approvals you need. |
| Confirmation of the use case | Noun hides the verb | The client confirms the use case. |
| Scopers get assigned by the sales lead. | Passive | The sales lead picks who scopes each project. |
| The process is being rewritten, due 10/19. | Origin story: what's changing, due date | Delete it. |
| The list combines the architecture gate and the questions from a recent project. | Origin story: where it came from | Delete it. |
| On one project the team asked for the routing SOPs and a screen recording. | Anecdote as evidence | Ask for things like written procedures or a screen recording of the core system. |
| On your current projects you lead engineering, and your chapter lead reviews scope. | Assumes the reader's current work | Delete it. |
| Give each load-bearing claim an owner and a date. | Jargon | Give each claim the scope depends on an owner and a date. |
| A fact line has neither a source URL nor an "Unverified" tag. | Double negative | A fact has no source and no "Unverified" tag. |
| two start-date, team-size and duration options | Stacked modifiers | two options, each with a start date, team size and length |
| The engineer answers the second and supplies evidence for the third. | Third person, stiff verb | You answer the second and bring evidence for the third. |
| Write any number into the SOW. | "Any" when it means every | Write every number into the statement of work. |
| Tell the lead what you can actually give. | Filler, vague "what" | Tell the lead how much time you can give. |
| Connect the tools you already use. | Filler "already", timing isn't the point | Connect your tools. |
| The repository now holds a case generator, a drafter and graders. | Origin story: what's changing | Delete it. |
| He reads code carefully and thinks ahead. | Not spoken: present tense for a past event | He read the code carefully and thought ahead. |
| He could say what each cleanup cost. | Shorthand the reader has to decode | He talked through the tradeoffs of each refactor. |
| **He thought ahead.** He raised the next problem before we got to it. | Restates the heading | He raised the next problem before we got to it. |

## Before you call it done

Read the draft one sentence at a time. For each one, ask:

- Would I say this out loud to a teammate?
- Who does the thing? Is that person the subject?
- Does this sentence tell the reader something they need to do the job? If it tells a story, says who's doing what, or explains why the doc exists, delete it.
- Did the point land a sentence ago? Then stop.
