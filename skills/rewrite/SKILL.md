---
name: rewrite
description: Rewrite every line of the given files so they follow the "How to write" rules, and keep a ledger of what changed. Use when asked to fix, rewrite or clean up writing.
argument-hint: "<files, folders, globs or pasted text>"
disable-model-invocation: true
---

Load the `plain-writing` skill. Rewrite `$ARGUMENTS` so it follows its rules and examples. With no argument, rewrite the files changed on the current branch.

1. List every file in scope. Skip binaries, lockfiles and data files, and say which ones you skipped.
2. Read each file line by line, top to bottom. Prose in code counts: comments, docstrings, CLI messages, prompts and commit-message templates.
3. Fix every line that breaks a rule. Don't change facts, behavior or anything a test or linter reads.
4. Run the repo's tests and linters if it has them.
5. Report a ledger: every file you read, its line count, its edit count and what changed, including files with no edits. A file missing from the ledger wasn't rewritten. If the ledger runs past 15 rows, write it to `writing-ledger.md` and point to it.
