# Project Memory

## Project Goal
Maintain a persistent, transferable memory layer for the codebase so Codex/Claude/agent harnesses can continue work without relying on chat history.

## Architecture
- Codebase
- Harness tooling
- Memory and handover files
- Session logs

## Important Constraints
- Keep handover files concise and current.
- Record why changes were made, not just what changed.
- Preserve history in append-only logs.
- Update the latest handover after each task.
- Treat platform-specific issues carefully.

## Known Issues
- Windows compatibility may be incomplete for some tooling.
- Interactive setup flows may depend on Unix-only libraries in some projects.

## Coding Conventions
- Use clear, direct markdown.
- Keep entries timestamped.
- Use consistent headings across files.

## Active Features
- Persistent project memory
- Handover trail
- Change tracking
- Session logs
