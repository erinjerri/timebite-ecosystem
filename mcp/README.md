# MCP Hub

This directory is reserved for MCP server/client/tool specifications and integration experiments.

## Rule

Use MCP when it materially improves agent/tool integration or cross-service orchestration. Prefer direct native APIs for iOS-local capabilities such as HealthKit, SwiftData, local notifications, and first-party calendar access.

## First Candidate Tools

- `get_today_tasks`
- `get_current_focus`
- `create_task`
- `start_timer`
- `complete_task`
- `get_daily_progress`

These should map to the shared action layer in `specs/actions`.
