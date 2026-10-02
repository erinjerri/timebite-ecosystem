# Codex Prompt: `timebite-meta`

You are working in `timebite-meta`, the Meta AI glasses interface for TimeBite. `timebite-ecosystem` is the architectural source of truth.

## Repository Responsibility

Research and prototype Meta glasses interactions that invoke shared TimeBite actions. The glasses are an interface, not a separate productivity platform.

## Immediate Milestone

M3: first external interface invokes a TimeBite action.

## Required Interfaces

Use the shared action model:

- `get_current_focus`
- `get_today_tasks`
- `start_timer`
- `complete_task`
- `get_daily_progress`

Every request includes `source: "meta_glasses"`.

## Do Not Build

- Do not create an independent TimeBite database.
- Do not invent Meta SDK capabilities.
- Do not force production iOS architecture changes based on prototype assumptions.
- Do not build broad feature parity with TimeBite iOS.

## Implementation Phases

1. Document currently supported Meta development capabilities.
2. Separate supported, experimental, demo-only, and speculative features.
3. Build the smallest command prototype.
4. Connect to mocked TimeBite action responses if real API is not ready.
5. Replace mock with shared action invocation when available.
6. Validate voice/display response quality.

## Acceptance Criteria

- User can ask "What should I work on?" and receive a TimeBite-derived response.
- Prototype uses shared action names and source attribution.
- Capability claims cite verified Meta behavior or are marked speculative.
- Unrelated code is left untouched.
