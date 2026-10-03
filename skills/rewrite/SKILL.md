---
name: rewrite
description: Rewrite every line of the given files so they follow the plain-writing rules, and keep a ledger of what changed. Use when asked to fix, rewrite or clean up writing.
argument-hint: "<files, folders, globs or pasted text>"
---

Rewrite `$ARGUMENTS` so it follows the rules in the `plain-writing` skill. If no argument is given, rewrite the files changed on the current branch.

1. List every file in scope. Skip binaries, lockfiles and data files, and say which ones you skipped.
2. Read each file line by line, top to bottom. Don't sample or skim. Prose in code counts: comments, docstrings, CLI messages, prompts and commit-message templates.
3. Fix every line that breaks a rule. Delete origin stories outright. Don't change facts, behavior, code identifiers, quotes, test fixtures or anything a test or linter reads.
4. Reread each file you changed, start to finish, against the rules. Your own rewrites break rules too. Fix them.
5. Run the repo's tests and linters if it has them.
6. Report a ledger: every file you read, its line count, its edit count and what changed, including files with no edits. A file missing from the ledger wasn't rewritten. If the ledger runs past 15 rows, write it to `writing-ledger.md` and point to it.
