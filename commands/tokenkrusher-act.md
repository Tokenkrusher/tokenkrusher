---
description: Run a TokenKrusher tip's action (pass the tip id)
allowed-tools: "Bash(*tokenkrusher.exe:*)"
---
Run `"${CLAUDE_PLUGIN_ROOT}/bin/tokenkrusher.exe" act $ARGUMENTS --session auto` with the Bash tool and show its output exactly as printed, with no extra commentary. If it exits with code 2, show the message and stop.
