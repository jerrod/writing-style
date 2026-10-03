---
name: review
description: List every line in the given files or text that breaks the plain-writing rules, with the rule it breaks and the fix. Changes nothing. Use when asked to review or check writing.
argument-hint: "<files, folders, globs or pasted text>"
---

Review `$ARGUMENTS` against the rules in the `plain-writing` skill. If no argument is given, review the files changed on the current branch.

1. List every file in scope. Skip binaries, lockfiles and data files, and say which ones you skipped.
2. Read each file line by line, top to bottom. Don't sample or skim. Prose in code counts: comments, docstrings, CLI messages, prompts and commit-message templates.
3. For each line that breaks a rule, write one row:

   | File | Line | Passage | Rule it breaks | Fix |

   Quote the passage exactly. Name one rule in a few words. Write the fix as the new text, or "Delete it" for an origin story.
4. After the table, list every file you read with its line count and violation count, including files with none. A file missing from that list wasn't reviewed.

Don't edit anything. If the table runs past 15 rows, write it to `writing-review.md` and point to it.
