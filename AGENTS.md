<!-- HAMMER_MCP_START -->
## Hammer MCP (mandatory)

Hammer is the canonical workflow and skills library for this repository. Its project MCP endpoint is checked in at `.mcp.json` for Claude Code and `.codex/config.toml` for Codex.

1. Call `hammer_get_started` once at the start of each agent session.
2. Use `hammer_search` before nontrivial work and `hammer_read` for the selected guidance.
3. Record reusable lessons and gotchas with `hammer_log`.
4. Before reporting Hammer unavailable, verify `http://127.0.0.1:8791/mcp`, reconnect MCP, and restart any session opened before the config was installed.

Do not remove or bypass Hammer wiring when changing other MCP servers.
<!-- HAMMER_MCP_END -->
