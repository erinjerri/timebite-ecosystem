# ADR-001: Repository Boundaries

Status: Accepted

## Decision

`timebite-ecosystem` is the architectural source of truth. Child repositories implement bounded responsibilities and do not redefine shared TimeBite contracts independently.

## Consequences

- Production iOS work stays in `timebite-official`.
- Meta-specific work stays in `timebite-meta`.
- Unity hackathon work stays in `timebite-meta-vr-start`.
- Fashion design work stays in the Tagimata fashion repository.
- Charm firmware/hardware work stays in `tagimata-interactive`.
- Shared schema and action changes originate here.
