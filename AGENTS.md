<!-- HAMMER_MCP_START -->
## Hammer MCP (mandatory)

Hammer is the canonical workflow and skills library for this repository. Its project MCP endpoint is checked in at `.mcp.json` for Claude Code and `.codex/config.toml` for Codex.

1. Call `hammer_get_started` once at the start of each agent session.
2. Use `hammer_search` before nontrivial work and `hammer_read` for the selected guidance.
3. Record reusable lessons and gotchas with `hammer_log`.
4. Native MCP tools are loaded when a session starts. If `mcp__hammer__*` is absent, immediately use the read-only machine fallback: first `hammer-mcp get-started`, then `hammer-mcp search "<task>"` and `hammer-mcp read <id>` as needed; use `hammer-mcp status` for diagnostics.
5. Never report Hammer unavailable merely because the native tool list is stale. Only report an outage when both the native MCP and `hammer-mcp status` fail, and include the exact fallback error.
6. Reconnect MCP or restart the session to restore native tools, but continue the current task through `hammer-mcp` instead of blocking.

Do not copy Hammer into this repository. Do not remove or bypass Hammer wiring when changing other MCP servers.
<!-- HAMMER_MCP_END -->
