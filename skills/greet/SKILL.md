---
description: Greet someone using a Go binary compiled by this plugin
---

Run the greeter binary that was compiled by this plugin's SessionStart hook.

The binary is at: `${CLAUDE_PLUGIN_DATA}/bin/greeter`

Run it via Bash with "$ARGUMENTS" as arguments. Show the full output to the user.

If the binary doesn't exist, tell the user the SessionStart hook may not have run yet — they should restart Claude Code with the plugin enabled.
