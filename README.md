# writing-style

This plugin and prompt make Claude write the way a person talks. Install one, not both.

## The plugin

```
/plugin marketplace add jerrod/writing-style
/plugin install writing-style@writing-style
```

It gives you:

- A hook that loads the rules from [CLAUDE.md](CLAUDE.md) at the start of every session.
- The `plain-writing` skill holds the rules and before and after examples. Claude loads it when it writes prose.
- `/writing-style:review <files>`: lists every line that breaks a rule, with the fix. Changes nothing.
- `/writing-style:rewrite <files>`: fixes every line of every file and reports a ledger of what changed.

Claude runs review and rewrite only when you type the command.

## The prompt

To get the rules without the plugin, add [CLAUDE.md](CLAUDE.md) to `~/.claude/CLAUDE.md`:

```sh
cat CLAUDE.md >> ~/.claude/CLAUDE.md
```

## Checks

`bin/check` checks the manifests, the hook and the skill frontmatter. It fails when a skill drops or rewords a line of [CLAUDE.md](CLAUDE.md). It also fails when the plugin's own prose uses a word the rules ban or a heading or manifest description has a colon subtitle. CI runs it on every push and pull request.
