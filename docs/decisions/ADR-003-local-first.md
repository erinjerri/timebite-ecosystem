# ADR-003: Local-First TimeBite Core

Status: Accepted

## Decision

The production TimeBite app should remain useful locally and should not require experimental cloud, Meta, Unity, or charm infrastructure for its core loop.

## Consequences

- Alpha can ship faster.
- TestFlight is not blocked by integrations.
- Sync and external interfaces can be layered in after core value is proven.
- External devices may need a mediated API later, but they should not dictate alpha storage.
