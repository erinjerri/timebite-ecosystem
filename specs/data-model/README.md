# Canonical Data Model

## Entities

### Task

Fields: `task_id`, `title`, `status`, `project_id`, `goal_id`, `priority`, `due_at`, `created_at`, `updated_at`.

### Project

Fields: `project_id`, `name`, `status`, `goal_id`, `created_at`, `updated_at`.

### Goal

Fields: `goal_id`, `name`, `horizon`, `status`, `created_at`, `updated_at`.

### DailyIntent

Fields: `daily_intent_id`, `date`, `priority_task_ids`, `note`, `created_at`, `updated_at`.

### TimerSession

Fields: `timer_session_id`, `task_id`, `started_at`, `ended_at`, `duration_minutes`, `status`, `source`.

### Reflection

Fields: `reflection_id`, `task_id`, `timer_session_id`, `text`, `mood`, `created_at`, `source`.

### Device

Fields: `device_id`, `type`, `name`, `capabilities`, `paired_user_id`, `paired_at`, `last_seen_at`.

## Open Questions

- Exact sync provider.
- Whether external devices call a cloud API directly or relay through iPhone for early demos.
- Final auth model for Meta and charm.
