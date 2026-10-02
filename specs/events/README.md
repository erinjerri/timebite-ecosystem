# Event Model

## Event Envelope

```json
{
  "event_id": "EVT_ID",
  "type": "timer_started",
  "source": "meta_glasses",
  "user_id": "USER_ID",
  "created_at": "2026-10-01T17:00:00Z",
  "payload": {
    "task_id": "TASK_ID",
    "timer_session_id": "TIMER_ID"
  }
}
```

## Initial Event Types

- `task_created`
- `task_completed`
- `daily_intent_set`
- `timer_started`
- `timer_paused`
- `timer_completed`
- `reflection_created`
- `device_paired`
- `device_action_requested`
- `device_action_failed`

## Use

Events support auditability, sync, device debugging, and cross-interface demos. They do not require a full event-sourced backend in alpha.
