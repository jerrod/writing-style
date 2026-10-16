---
name: review
description: List every line in the given files or text that breaks the "How to write" rules, with the rule it breaks and the fix. Changes nothing. Use when asked to review or check writing.
argument-hint: "<files, folders, globs or pasted text>"
disable-model-invocation: true
---

Review `$ARGUMENTS` against the rules below, using the `plain-writing` examples. With no argument, review the files changed on the current branch.

1. List every file in scope. Skip binaries, lockfiles and data files, and say which ones you skipped.
2. Read each file line by line, top to bottom. Prose in code counts: comments, docstrings, CLI messages, prompts and commit-message templates.
3. For each line that breaks a rule, write one row:

   | File | Line | Passage | Rule it breaks | Fix |

   Quote the passage exactly. Name one rule in a few words. Write the fix as the new text, or "Delete it" for an origin story.
4. After the table, list every file you read with its line count and violation count, including files with none. A file missing from that list wasn't reviewed.

Don't edit anything. If the table runs past 15 rows, write it to `writing-review.md` and point to it.

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
