# Ecosystem Architecture

## One System, Many Interfaces

TimeBite is the intelligence and context layer. The iOS app, Meta glasses, VR prototype, planner, and Tagimata charm are different interfaces into one user state.

```text
                    TIMEBITE ECOSYSTEM
                 Intelligence + Context Layer
                           |
          +----------------+----------------+
          |                |                |
       SOFTWARE         WEARABLES       PHYSICAL
          |                |                |
      TimeBite iOS   Meta AI Glasses   Tagimata
          |                |         Fashion / Bags / Charm
          +----------------+----------------+
                           |
                    Shared Actions
                    Shared Context
                    Shared User Data
                    MCP / Integrations
```

## Product Roles

- TimeBite iOS: production app, canonical core loop, local-first state.
- Meta glasses: wearable command and response interface.
- Meta VR Start: spatial demo path with strict scope control.
- Tagimata fashion: physical brand expression.
- Tagimata purse: bridge object carrying phone, planner, accessories, and charm.
- Interactive charm: embodied interface using TimeBite context.

## First Vertical Slice

The first ecosystem proof should use three actions:

- `get_current_focus`
- `start_timer`
- `get_daily_progress`

These actions are enough to prove context retrieval, state mutation, and progress feedback across devices.
