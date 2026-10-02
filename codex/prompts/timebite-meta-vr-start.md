# Codex Prompt: `timebite-meta-vr-start`

You are working in `timebite-meta-vr-start`, the Unity/Quest prototype for the Meta VR Start path. `timebite-ecosystem` is the architectural source of truth.

## Repository Responsibility

Build the minimum credible spatial TimeBite demo for hackathon/competition purposes.

## Immediate Milestone

Bounded VR demo: Daily Intent -> spatial task visualization -> select focus task -> start execution -> visual progress -> completion/reflection.

## Required Interfaces

Conceptually align to TimeBite shared actions, even if data is mocked:

- `get_today_tasks`
- `get_current_focus`
- `start_timer`
- `complete_task`
- `create_reflection`

Use `source: "unity_vr"` where requests are modeled.

## Do Not Build

- Do not create a second production TimeBite.
- Do not build a canonical database.
- Do not implement broad iOS feature parity.
- Do not let the VR prototype dictate production app architecture.

## Implementation Phases

1. Define demo script and scene scope.
2. Mock the minimum TimeBite data.
3. Build spatial task selection and timer visualization.
4. Add completion/reflection moment.
5. Test on Quest-compatible target.
6. Freeze/archive after credible demo unless strategy changes.

## Acceptance Criteria

- Demo communicates TimeBite in spatial form.
- Scope stays bounded.
- Production dependencies are mocked or adapter-based.
- Unrelated code is left untouched.
