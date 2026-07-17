# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Detected stack
- Languages: Rust.
- Frameworks: none detected from the supported starter markers.

## Verification
- Run Rust verification from `rust/`: `cargo fmt`, `cargo clippy --workspace --all-targets -- -D warnings`, `cargo test --workspace`
- `src/` and `tests/` are both present; update both surfaces together when behavior changes.

## Repository shape
- `rust/` contains the Rust workspace and active CLI/runtime implementation.
- `src/` contains source files that should stay consistent with generated guidance and tests.
- `tests/` contains validation surfaces that should be reviewed alongside code changes.

## Working agreement
- Prefer small, reviewable changes and keep generated bootstrap files aligned with actual repo workflows.
- Keep shared defaults in `.claude.json`; reserve `.claude/settings.local.json` for machine-local overrides.
- Do not overwrite existing `CLAUDE.md` content automatically; update it intentionally when repo workflows change.

<!-- HAMMER_MCP_START -->
## Hammer MCP (mandatory)

Hammer is the canonical workflow and skills library for this repository. Its project MCP endpoint is checked in at `.mcp.json` for Claude Code and `.codex/config.toml` for Codex.

1. Call `hammer_get_started` once at the start of each agent session.
2. Use `hammer_search` before nontrivial work and `hammer_read` for the selected guidance.
3. Record reusable lessons and gotchas with `hammer_log`.
4. Before reporting Hammer unavailable, verify `http://127.0.0.1:8791/mcp`, reconnect MCP, and restart any session opened before the config was installed.

Do not remove or bypass Hammer wiring when changing other MCP servers.
<!-- HAMMER_MCP_END -->
