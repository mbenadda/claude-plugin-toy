# binary-toy

Proof-of-concept Claude Code plugin that compiles and runs a Go binary.

## What it does

1. **On session start**: a hook compiles `src/main.go` into a binary at `${CLAUDE_PLUGIN_DATA}/bin/greeter`
2. **On `/binary-toy:greet <name>`**: a skill tells Claude to run the compiled binary

## Try it

```bash
claude --plugin-dir ~/claude-plugin-toy
```

Then:

```
/binary-toy:greet Mehdi
```

## Structure

```
.claude-plugin/plugin.json   — plugin manifest
src/main.go                  — Go source for the binary
hooks/hooks.json             — SessionStart hook compiles the binary
skills/greet/SKILL.md        — skill that invokes the binary
```
