# writing-style

This plugin makes Claude write the way a person talks.

## Install

```
/plugin marketplace add jerrod/writing-style
/plugin install writing-style@writing-style
```

## What you get

- The `plain-writing` skill has the rules and a table of before and after examples. Claude loads it when it writes prose.
- A hook prints the rules from the `plain-writing` skill at the start of every session.
- `/writing-style:review <files>` lists every line that breaks a rule and gives the fix. It changes nothing.
- `/writing-style:rewrite <files>` fixes every line of every file and reports what changed.

Claude runs review and rewrite only when you type the command.

## Checks

CI runs `bin/check` on every push and pull request. `bin/check` fails when:

- A manifest doesn't parse, or a skill has no name or description.
- The hook prints anything but the rules.
- A file other than the `plain-writing` skill copies a rule.
- The plugin's own prose uses a word or phrase the rules ban.
- A heading or a manifest description has a colon subtitle.
