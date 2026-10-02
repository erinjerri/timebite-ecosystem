# Master Gantt: October 2026 - September 2027

September 2027 is the polished integrated presentation gate, not the first release.

Legend:

- `P` primary founder attention.
- `S` secondary/supporting attention.
- `M` maintenance, monitoring, or light iteration.
- `-` parked unless a gate requires action.

## Month-By-Month Gantt

| Workstream | Oct 2026 | Nov 2026 | Dec 2026 | Jan 2027 | Feb 2027 | Mar 2027 | Apr 2027 | May 2027 | Jun 2027 | Jul 2027 | Aug 2027 | Sep 2027 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| TimeBite iOS | `P` core loop, local data, action envelope | `P` alpha: intent/task/timer/activity/reflection | `P` TestFlight checklist + internal beta | `P` external TestFlight, stability, privacy/auth | `P` beta fixes, release readiness | `P` public beta/App Store v1 if stable | `P` public release or fast iteration | `M` demo support, no dependency creep | `M` summer app baseline | `M` soft-launch support | `M` stabilize demo data/flows | `S` presentation-ready polish |
| Shared Action/Data Contracts | `P` M0 action/entity/event drafts | `P` M0 locked enough for app + interfaces | `S` device/source attribution | `S` idempotency, permissions, pairing | `S` contract freeze for external demo | `S` first external action route | `M` compatibility fixes | `S` cross-device context | `M` demo contract baseline | `M` no new schemas without gate | `M` stability only | `M` presentation support |
| Meta / External Interface | `S` capability research | `S` SDK/API map | `S` feasibility notes | `S` prototype route | `S` action-call prep | `S` first external interface if possible | `S` refine if TimeBite release is safe | `S` cross-device demo path | `S` partial ecosystem demo role | `S` optional private demo polish | `-` park unless needed | `S` polished evidence/demo |
| Unity VR Start | `-` thesis only | `-` parked | `S` scope if deadline exists | `S` bounded build only if useful | `S` test/submission prep if required | `S` credible demo/submission | `-` archive by default | `-` parked | `-` parked | `-` parked | `-` parked | `-` only show recorded evidence |
| Fashion Looks | `S` direction, mood, hero criteria | `S` select 2-3 hero looks | `S` sketches/spec direction | `S` tech drawings/pattern direction | `S` sourcing readiness gate | `S` first sample conversations | `S` samples/fitting | `S` revision/costing | `S` one hero sample for partial demo | `P` capsule preview assets | `P` soft-launch/editorial prep | `P` presentation/pop-up readiness |
| Flagship Purse | `S` concept + use case | `S` choose flagship, optional secondary | `S` dimensions + fit assumptions | `S` tech pack draft | `S` sourcing readiness gate | `S` sample conversations | `S` first sample/revision | `S` costing/MOQ | `S` purse sample/prototype for demo | `P` private preview sample | `P` soft-launch prep | `P` presentation/pop-up readiness |
| M5Stack Charm | `S` flagship character | `S` interaction script | `S` M5Stack POC | `S` BOM, dimensions, battery assumptions | `S` sourcing readiness gate | `S` TimeBite action connection | `S` enclosure/audio/motion demo | `S` cross-device demo + bare ESP32/custom PCB evidence review | `S` rough charm for partial demo | `S` integrated private demo | `S` reliability pass | `S` polished presentation demo |
| Sourcing / Manufacturing | `-` no commitments | `-` no commitments | `-` no commitments | `S` vendor question list | `P` manufacturer/sourcing readiness | `S` sample-maker outreach | `S` sample revisions | `S` costing/MOQ comparisons | `S` RFQs for plausible pieces | `S` small-run decision only | `S` packaging/vendor prep | `S` pop-up readiness, not mass production |
| Founder Attention | TimeBite + architecture | TimeBite alpha | TimeBite TestFlight | TimeBite beta | TimeBite release readiness + sourcing gate | TimeBite release + first interface | TimeBite release/iteration | cross-device proof | partial ecosystem demo | capsule/private demo | soft-launch prep | polished presentation |

## Release Gates

| Gate | Target | Release Meaning | Must Be True | Must Not Block |
| --- | --- | --- | --- | --- |
| TestFlight | Dec 2026/Jan 2027 | TimeBite can be tested by external users | core loop works, privacy/auth path known, no founder hand-holding | Meta, Unity, charm, fashion, purse |
| Public beta/App Store v1 | Mar/Apr 2027 | TimeBite has its own public release | stable daily-use loop, persistence confidence, accessible/polished core UX | experimental integrations |
| Partial ecosystem demo | Jun 2027 | credible connected preview | released/stable TimeBite, one external interface action, one hero look sample/mockup, purse sample/prototype, rough M5Stack charm | custom PCB, full collection, production inventory |
| Capsule/private demo/soft launch | Jul/Aug 2027 | controlled audience preview | photographed looks, flagship purse sample, charm demo using shared context, optional Meta flow | Unity productization, extra SKUs |
| Integrated presentation/pop-up readiness | Sep 2027 | polished story and operational readiness | coherent demo, cost model, risk register, go/no-go decisions, presentation-ready samples | mass manufacturing unless justified |

## Prototype And Sourcing Gates

| Gate | Target | Decision |
| --- | --- | --- |
| Action contract M0 | Oct/Nov 2026 | stable enough for TimeBite, Meta, and charm to share one context language |
| Manufacturer/sourcing readiness | Feb 2027 | hero look specs, purse tech pack draft, charm POC envelope/BOM ready for vendor conversations |
| First external interface | Mar 2027 | Meta or M5Stack invokes a shared TimeBite action without changing TimeBite release scope |
| Cross-device demo | May 2027 | two interfaces read/write the same TimeBite context |
| Bare ESP32/custom PCB evidence review | May/Jun 2027 | stay on M5Stack unless interaction value, dimensions, battery, motion/audio, and vendor input justify migration |

## Dependency Rules

- TimeBite TestFlight and public release depend only on the iOS app and core shared contracts.
- Meta, Unity, M5Stack, fashion, and purse work cannot block TimeBite public beta/App Store v1.
- Meta and charm integration depend on the shared action contract, not on each other.
- June requires a partial ecosystem demo, not production-ready manufacturing.
- July/August requires controlled preview quality, not a full public launch.
- September requires polish, narrative coherence, and pop-up readiness.
- Fashion stays limited to 2-3 hero looks.
- Purse stays limited to one flagship purse and optionally one secondary design.
- Charm stays on one M5Stack ESP32-family platform until evidence supports a smaller bare ESP32/devboard or custom PCB path.
- Charm firmware uses embedded C/C++ or Rust. MicroPython is not a production firmware stack.
- Unity is time-boxed and archivable after a credible demo/submission.

## Stop-Work Triggers

| Trigger | Stop | Continue |
| --- | --- | --- |
| TimeBite release slips past April | Meta polish, Unity, extra hardware, extra fashion/purse scope | TimeBite core release, shared contract fixes |
| February sourcing packet is incomplete | new looks, new purse concepts, custom PCB exploration | specs, dimensions, BOM, vendor questions |
| First external interface is not credible by March | Meta-specific polish or second interface work | simplest Meta or M5Stack action invocation |
| Cross-device demo is not credible by May | bare ESP32/custom PCB decision, extra charm features | one shared context path across two interfaces |
| June partial demo is at risk | Unity, extra SKUs, second electronics platform | TimeBite baseline, one external action, one look, one purse, one charm |
| Sample costs or MOQs exceed budget | production commitments and broad inventory | sample-only path, private demo, vendor alternatives |
| M5Stack cannot prove interaction value | bare ESP32/custom PCB and certification planning | revise interaction script or archive charm production path |
