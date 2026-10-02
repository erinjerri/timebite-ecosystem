# ADR-004: M5Stack Before Custom PCB

Status: Accepted

## Decision

The first interactive charm prototype uses one M5Stack development platform. M5Stack is the first ESP32-family platform for the charm. A smaller bare ESP32/devboard or custom PCB path waits until interaction, battery, connectivity, audio, motion, and enclosure constraints are validated.

Firmware should be embedded C/C++ or Rust. MicroPython is not a production firmware stack for this project.

## Consequences

- Faster learning.
- Lower cost.
- Fewer parallel hardware paths.
- One reusable electronics architecture can emerge from evidence instead of speculation.
- Firmware choices stay compatible with production constraints instead of optimizing only for quick scripting.
