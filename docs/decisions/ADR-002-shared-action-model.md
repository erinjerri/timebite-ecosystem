# ADR-002: Shared Action Model

Status: Accepted

## Decision

All interfaces invoke TimeBite through a small canonical action layer rather than each interface inventing its own workflow model.

## Initial Actions

- `get_today_tasks`
- `get_current_focus`
- `create_task`
- `start_timer`
- `pause_timer`
- `complete_task`
- `get_daily_progress`
- `create_reflection`
- `get_goal_progress`

## Consequences

Meta glasses, M5Stack charm, agents, and future planner ingestion can share behavior. The production app remains free to implement internals differently as long as it honors the contract.
