# TimeBite Actions

## Request Envelope

```json
{
  "idempotency_key": "REQ_UNIQUE",
  "action": "start_timer",
  "source": "meta_glasses",
  "requested_at": "2026-10-01T17:00:00Z",
  "payload": {}
}
```

## Initial Actions

| Action | Type | Payload |
| --- | --- | --- |
| `get_today_tasks` | read | optional date |
| `get_current_focus` | read | optional context hint |
| `create_task` | write | title, project_id, goal_id, due/context fields |
| `start_timer` | write | task_id, duration_minutes |
| `pause_timer` | write | timer_session_id |
| `complete_task` | write | task_id, optional reflection |
| `get_daily_progress` | read | date |
| `create_reflection` | write | task_id/timer_session_id, text |
| `get_goal_progress` | read | goal_id |

## Source Values

- `ios_app`
- `meta_glasses`
- `tagimata_charm`
- `unity_vr`
- `planner_ingestion`
- `agent`

## Contract Rules

- Mutations include `idempotency_key`.
- Every request includes `source`.
- Unknown fields should be ignored during early prototypes when safe.
- Responses should include success/error status and event IDs for mutations.
