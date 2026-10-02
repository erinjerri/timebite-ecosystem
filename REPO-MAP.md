# Repository Map

## `timebite-ecosystem`

Purpose: master architecture, contracts, roadmap, cross-repository orchestration, MCP/integration design.

Inputs: product strategy, implementation learnings from child repos, integration requirements, manufacturing constraints.

Outputs: shared schemas, action contracts, device protocol, ADRs, roadmap, Codex prompts, integration specs.

Dependencies: all child repos report contract changes here.

Stack reference: [docs/architecture/tech-stack.md](docs/architecture/tech-stack.md) maps the intended framework and language choices across child repositories.

Belongs here:

- system architecture
- MCP architecture
- connector architecture
- shared actions and schemas
- event model
- device protocol
- roadmap and Gantt
- integration tests/specs

Does not belong here:

- production SwiftUI app implementation
- fashion pattern source files
- Unity production code
- embedded firmware as the primary implementation

## `timebite-official`

Purpose: production TimeBite Apple-platform application.

Outputs: TestFlight/App Store app, core user workflows, canonical local-first app behavior.

Belongs here: Swift/SwiftUI, SwiftData, tasks/projects/goals, Daily Intent, timers, Activity Ring, reflection, calendar, speech capture, HealthKit when ready.

Does not belong here: unstable Meta experiments, M5Stack firmware, Unity demo logic, fashion production files.

## `timebite-meta`

Purpose: Meta AI glasses interface into TimeBite.

Outputs: wearable commands, voice/display experiments, shared action invocation, pairing/auth research.

Belongs here: Meta-specific interface code and feasibility notes.

Does not belong here: independent TimeBite database or new task schema.

## `timebite-meta-vr-start`

Purpose: bounded Unity/Quest hackathon prototype.

Outputs: minimum credible spatial TimeBite demo.

Belongs here: Unity/C# prototype, mocked data where appropriate, Quest testing.

Does not belong here: production TimeBite architecture decisions or long-term app logic.

## Tagimata Fashion Repository

Purpose: apparel collection and industrial/fashion design.

Outputs: sketches, patterns, tech packs, sample notes, material decisions, presentation assets.

Belongs here: garments, materials, manufacturing, sourcing, packaging, photography concepts.

Does not belong here: electronics architecture or TimeBite schemas.

## `tagimata-interactive`

Purpose: interactive charm hardware and firmware.

Outputs: M5Stack prototype, evidence-gated bare ESP32 experiments, C/C++ or Rust device protocol implementation, BOM, enclosure constraints.

Belongs here: embedded C/C++ or Rust firmware, BLE/Wi-Fi, audio, display, motion, power, battery, manufacturer notes.

Does not belong here: production MicroPython firmware, one-off electronics for every character, independent productivity logic, final custom PCB before POC evidence.

## Contract Rule

No child repository may independently redefine shared `Task`, `Goal`, `Project`, `TimerSession`, `Action`, `Device`, `Event`, `User`, or synchronization contracts. Proposed changes are captured here first.
