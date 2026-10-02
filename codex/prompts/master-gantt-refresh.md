# Codex Prompt: Refresh The Master Gantt Around Earlier Release Gates

You are working in `timebite-ecosystem`, the architectural source of truth for TimeBite x Tagimata.

## Objective

Rework the master Gantt and roadmap so September 2027 is not treated as the first release. The plan should show a staged release ladder:

1. March/April 2027: TimeBite iOS public beta or App Store v1.
2. June 2027: partial ecosystem demo.
3. July/August 2027: capsule preview, private demo, or soft launch.
4. September 2027: polished integrated presentation/pop-up readiness.

## Files To Review First

- `README.md`
- `ARCHITECTURE.md`
- `ROADMAP.md`
- `REPO-MAP.md`
- `docs/product/master-roadmap.md`
- `docs/product/master-gantt.md`
- `docs/product/milestones.md`
- `docs/product/final-questions.md`
- `docs/product/risk-register.md`
- `docs/product/cost-model.md`
- `docs/fashion/initial-looks.md`
- `docs/fashion/purse-roadmap.md`
- `docs/hardware/charm-roadmap.md`
- `docs/hardware/manufacturing-readiness.md`

## Required Gantt Changes

Create a more detailed month-by-month Gantt from October 2026 through September 2027 that distinguishes:

- release gates
- prototype gates
- sourcing/manufacturing gates
- founder attention level
- dependencies
- stop-work triggers

The Gantt should explicitly show:

- TimeBite TestFlight before public release.
- TimeBite public beta/App Store v1 in March or April.
- February 2027 manufacturer/sourcing readiness.
- First external interface by March if possible.
- Cross-device demo by May.
- Partial ecosystem demo in June.
- Capsule preview/private demo/soft launch in July or August.
- September as polished integrated presentation/pop-up readiness.

## Constraints

- Do not make a fantasy Gantt where all six workstreams receive full effort every month.
- Do not let Meta, Unity, M5Stack, fashion, or purse work block TimeBite release.
- Keep Unity time-boxed and archivable after a credible demo.
- Keep charm work on one M5Stack platform until evidence supports ESP32/custom PCB.
- Keep fashion to 2-3 hero looks.
- Keep purse to one flagship purse and optionally one secondary design.
- Do not add production code.

## Output Expectations

Update existing documentation rather than creating duplicate parallel plans unless a new file is clearly useful.

At minimum, update:

- `ROADMAP.md`
- `docs/product/master-roadmap.md`
- `docs/product/master-gantt.md`
- `docs/product/milestones.md`

Also update any related final-answer, risk, or stop-work sections if they still imply September is the first meaningful release.

## Acceptance Criteria

- A reader can tell what can be released in spring, summer, and September.
- The plan protects the TimeBite iOS release from experimental dependencies.
- June has a credible partial ecosystem scope.
- July/August has a credible soft-launch/capsule-preview scope.
- September remains useful as the polished integrated presentation gate.
