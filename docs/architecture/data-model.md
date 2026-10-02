# Shared Data Model

## Canonical Entities

- `User`: owner of TimeBite state.
- `Task`: executable unit of work.
- `Project`: grouping for tasks.
- `Goal`: higher-level desired outcome.
- `DailyIntent`: selected priorities for a day.
- `TimerSession`: timed execution period.
- `Reflection`: user note after or around execution.
- `Device`: paired interface such as iPhone, glasses, charm.
- `ActionRequest`: request to mutate or read state.
- `Event`: appendable record of meaningful changes.

## Contract Principles

- IDs must be stable across interfaces.
- Mutating actions should support idempotency.
- Every external request includes `source`.
- Device permissions should be explicit.
- Events should be appendable and easy to audit.
- Local-first app behavior should survive temporary network failure.

## Example Action Request

```json
{
  "idempotency_key": "REQ_2026_10_01_001",
  "action": "start_timer",
  "source": "tagimata_charm",
  "task_id": "TASK_ID",
  "duration_minutes": 30,
  "requested_at": "2026-10-01T17:00:00Z"
}
```
