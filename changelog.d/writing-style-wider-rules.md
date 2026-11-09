Version 0.3.0 adds six rules, widens three, and keeps one copy of the rules.

The new rules catch:

- Several names for one thing, like "the session export" in one sentence and "the session-to-bill rows" in the next.
- A heading, label or tag that repeats the text next to it, and a count in a heading.
- A sentence that describes the document or points around it.
- A claim nobody checked, headings included.
- A number with no noun, and a sentence with more than two numbers.
- A set of items where each one has the same parts, needed or not.

The wider rules catch:

- A second point tacked on with "so", "and" or "because". The rule used to cover only "which".
- Data as the subject of a human verb, like "4,006 phones carry 8,076 bills". The subject is the person or program that acts.
- A term the writer never defined, and a column name used as an English word.

The plain-writing table has nine new before and after rows, and the checklist has two new questions.

The `plain-writing` skill holds the only copy of the rules. The hook prints them from the skill, and the review and rewrite skills load the skill. The repo has no `CLAUDE.md`, and the README no longer offers the rules as a prompt to paste.

`bin/check` fails when a second file copies a rule, when the hook prints anything but the rules, and when the plugin's own prose points up or down the document.
