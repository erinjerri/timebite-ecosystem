# Meta Interfaces

## Meta AI Glasses

Treat glasses as a TimeBite interface. They should not contain an independent TimeBite database.

Initial desired commands:

- "What should I work on?"
- "What are my three priorities?"
- "Start my portfolio timer."
- "Add contact manufacturer to Tagimata."
- "How much focused time have I done today?"
- "Complete this task."

Target architecture:

```text
Meta Glasses
      |
Meta-supported interface
      |
TimeBite Action Layer
      |
TimeBite context/data
      |
response
      |
audio/display
```

Capability tracking must distinguish:

- currently supported
- experimentally possible
- hack/demo only
- unavailable or speculative

Do not invent SDK capability. Record unknowns until verified against Meta documentation and real device tests.

## Meta VR Start / Unity

Goal: minimum credible Unity implementation for a hackathon/prototype path.

Reuse conceptually:

- Daily Intent
- focus task
- timer/progress
- completion/reflection

Mock when appropriate:

- auth
- sync
- full project hierarchy
- historical analytics
- production AI

Do not build:

- a second production TimeBite
- a canonical database
- broad app feature parity
