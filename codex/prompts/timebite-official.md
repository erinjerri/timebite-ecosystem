# Codex Prompt: `timebite-official`

You are working in `timebite-official`, the production TimeBite Apple-platform application. `timebite-ecosystem` is the architectural source of truth for shared contracts, repository boundaries, roadmap, and integration decisions.

## Repository Responsibility

Build the production iOS app: Swift/SwiftUI, SwiftData/local persistence, tasks, projects, goals, Daily Intent, timers, Activity Ring, reflection, calendar integration, speech capture, TestFlight, and App Store readiness.

## Immediate Milestone

M1/M2: make the core loop reliable enough for TestFlight.

Intent -> prioritize -> execute task -> timer -> Activity Ring/progress -> reflection -> historical context.

## Required Interfaces

Align with shared entities and actions from `timebite-ecosystem/specs`:

- `Task`
- `Project`
- `Goal`
- `DailyIntent`
- `TimerSession`
- `Reflection`
- `Device`
- TimeBite action names, especially `get_current_focus`, `start_timer`, and `get_daily_progress`

## Do Not Build

- Do not build Meta glasses experiments here.
- Do not build Unity logic here.
- Do not build M5Stack firmware here.
- Do not let experimental integrations block TestFlight.
- Do not redefine shared schemas without updating `timebite-ecosystem`.

## Implementation Phases

1. Audit current core-loop implementation.
2. Stabilize local persistence and migrations.
3. Complete Daily Intent, task prioritization, timer, progress, and reflection.
4. Add beta-safe calendar and speech capture.
5. Add lightweight shared-action adapter surface for future integrations.
6. Prepare TestFlight checklist and acceptance testing.

## Acceptance Criteria

- User can create a task, select it for today, start a timer, complete work, see progress, and reflect.
- App remains useful without Meta, Unity, hardware, or cloud integrations.
- Tests or manual QA cover the core loop and persistence.
- Unrelated code is left untouched.
