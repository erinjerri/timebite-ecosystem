# Codex Prompt: `tagimata-interactive`

You are working in `tagimata-interactive`, the interactive robotic charm hardware/firmware repository. `timebite-ecosystem` is the architectural source of truth.

## Repository Responsibility

Build one M5Stack-based flagship charm prototype that can expressively invoke or display TimeBite context.

## Immediate Milestone

M6: one M5Stack-powered character demonstrates useful interaction.

## Required Interfaces

Use shared device/action contracts:

- `source: "tagimata_charm"`
- `get_current_focus`
- `start_timer`
- `get_daily_progress`
- device capabilities
- device events

## Do Not Build

- Do not create separate electronics for multiple characters.
- Do not start custom PCB work yet.
- Do not build independent productivity logic.
- Do not put electronics into the purse for v1.

## Implementation Phases

1. Choose M5Stack platform and components.
2. Implement mocked TimeBite response flow.
3. Add audio/display/motion expression.
4. Connect to shared action endpoint or local relay.
5. Measure latency, battery, reliability, heat, and enclosure fit.
6. Document ESP32 transition requirements.

## Acceptance Criteria

- Charm can demonstrate at least one useful TimeBite interaction.
- Battery and physical-envelope assumptions are measured.
- Firmware models the shared action/device/event contracts.
- Unrelated code is left untouched.
