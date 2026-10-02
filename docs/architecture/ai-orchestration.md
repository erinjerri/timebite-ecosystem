# AI Orchestration

## Role

AI helps interpret intent, summarize context, recommend focus, transcribe speech, and generate reflective prompts. It does not become the canonical source of truth.

## Near-Term AI Uses

- speech-to-task capture
- "what should I work on next?" reasoning
- reflection prompt suggestions
- planner ingestion experiments
- summarizing daily progress for glasses or charm responses

## Guardrails

- Keep deterministic actions separate from model interpretation.
- Require explicit user confirmation for destructive or ambiguous changes.
- Log action requests and source.
- Do not let Meta, Unity, or charm-specific prompts define core data schemas.
- Prefer small prompt contracts over broad autonomous planning until the core product is stable.
