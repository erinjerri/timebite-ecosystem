# TimeBite x Tagimata Ecosystem Architecture

## Executive Architecture

```text
                       USER
                        |
       +----------------+----------------+
       |                |                |
     iPhone        Meta Glasses        Charm
       |                |                |
       +----------------+----------------+
                        |
                TIMEBITE ACTION LAYER
                        |
          +-------------+-------------+
          |             |             |
        Tasks         Timers        Context
          |             |             |
          +-------------+-------------+
                        |
                    DATA MODEL
                        |
          +-------------+-------------+
          |             |             |
      Local-first      Sync          MCP
                        |
                        v
                  Integrations
```

The production TimeBite iOS app is the canonical consumer product and the first source of trusted user state. Meta glasses, Unity VR, planner ingestion, agents, and interactive charms are interfaces into TimeBite, not separate productivity systems.

## Boundary Model

| Layer | Owns | Does Not Own |
| --- | --- | --- |
| Swift/SwiftUI | Production iOS UX, local persistence, App Store delivery, core loop | Experimental hardware firmware, Unity demo logic |
| Unity/C# | Bounded VR Start spatial prototype | Canonical task database or production roadmap |
| Embedded C/C++ or Rust | M5Stack/ESP32-family charm behavior, BLE/Wi-Fi device protocol | Independent TimeBite schema, production MicroPython firmware |
| MCP | Agent/tool integration surface where useful | Native iOS-only APIs that are better direct |
| Backend services | Sync, auth, secure external interface mediation if needed | Replacing local-first product logic prematurely |
| Local storage | Fast private core loop on device | Cross-interface contracts by itself |
| Cloud services | Sync and external device access | Required dependency for alpha unless needed |
| AI models | Natural-language interpretation and prioritization support | Canonical truth without explicit user data contracts |
| Meta APIs | Wearable voice/display interface | TimeBite storage or workflow ownership |

## Shared Action Layer

Every interface should call the same conceptual action layer:

- `get_today_tasks`
- `get_current_focus`
- `create_task`
- `start_timer`
- `pause_timer`
- `complete_task`
- `get_daily_progress`
- `create_reflection`
- `get_goal_progress`

Example:

```json
{
  "action": "start_timer",
  "source": "meta_glasses",
  "task_id": "TASK_ID",
  "duration_minutes": 30
}
```

The TimeBite core should only care about source when permissions, pairing, privacy, or context quality require it.

## Flagship Demonstration

After the spring TimeBite release and summer ecosystem previews, the September 2027 integrated presentation should show:

1. User wears one Tagimata hero look and carries the flagship purse.
2. TimeBite iOS contains today's intent and tasks.
3. User asks Meta glasses, "What should I work on next?"
4. Meta interface invokes `get_current_focus`.
5. User starts the task via glasses or iPhone.
6. Activity Ring records the execution session.
7. Later, user asks the robotic charm, "How much focused work have I done?"
8. Charm retrieves the same TimeBite context and responds with audio, display, and/or motion.
9. The physical planner mirrors the same planning workflow.

This proves one identity, one context, many interfaces.

## Early Stabilization

Stabilize early:

- canonical action names and payload envelope
- `Task`, `Project`, `Goal`, `TimerSession`, `Reflection`, `Device`, `Event`, `User`
- source attribution
- idempotency keys for actions that mutate state
- device pairing and permission boundaries

Do not stabilize too early:

- final sync provider
- final AI provider
- final Meta capability assumptions
- charm industrial design
- custom PCB layout
- full fashion collection sizing
- Unity abstractions
