# Changelog

All notable changes to the Memory Bank MCP extension will be documented in this file.

## [2.2.0] - 2025-02-27

### Added

- **API Key Management** — Create, revoke, rotate, export, and search API keys for HTTP mode
- **API Keys Tree View** — Dedicated sidebar view for managing API keys
- **HTTP-Aware Tree Providers** — All sidebar views now adapt based on connection mode (stdio vs HTTP)
- **Split Copilot Agent Instructions** — Separate STDIO and HTTP instruction templates with 36-tool catalog
- **Remote Server Connect** — Inline connect action in Remote Servers tree
- **Publishing Support** — Added `npm run publish` and `npm run publish:pre-release` scripts

### Changed

- Consolidated MCP tool reference from 47 to 36 tools (v1.10.0 server compatibility)
- Unified config resolution — `.vscode/mcp.json` now used for both STDIO and HTTP modes
- Status view shows connection mode and transport indicator
- Files view shows "(database)" indicator for HTTP-stored files
- Stores view shows "Not available in HTTP mode" when connected via HTTP
- Extension commands increased from 24 to 39

### Fixed

- Stale tool calls updated (`graph_rebuild` → `graph_maintain`, `getCurrentMode` → `switch_mode`, etc.)
- Missing `apiKeysTreeView` in extension variables

## [2.0.0] - 2025-02-26

### Added

- Initial standalone release (extracted from monorepo)
- Dual transport support (stdio + HTTP)
- Full MCP client abstraction with `BaseMcpClient`, `StdioMcpClient`, `HttpMcpClient`
- Knowledge Graph visualization with React Flow
- GitHub Copilot integration (Language Model Tool + Chat Participant)
- Multi-store support
- Remote server management
- 5 AI assistant modes (architect, code, debug, test, ask)
- Interactive graph webview with entity management
