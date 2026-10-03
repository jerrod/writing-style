# writing-style

This plugin and prompt make Claude write the way a person talks. Install one, not both.

## The plugin

```
/plugin marketplace add jerrod/writing-style
/plugin install writing-style@writing-style
```

It gives you:

- A hook that loads the rules from [CLAUDE.md](CLAUDE.md) at the start of every session.
- The `plain-writing` skill: before and after examples. Claude loads it when it writes prose.
- `/writing-style:review <files>`: lists every line that breaks a rule, with the fix. Changes nothing.
- `/writing-style:rewrite <files>`: fixes every line of every file and reports a ledger of what changed.

Claude only runs review and rewrite when you type the command, so their descriptions stay out of every session.

## The prompt

To get the rules without the plugin, add [CLAUDE.md](CLAUDE.md) to `~/.claude/CLAUDE.md`:

```sh
cat CLAUDE.md >> ~/.claude/CLAUDE.md
```

## Checks

`bin/check` validates the manifests, the hook and the skill frontmatter. CI runs it on every push.
