# TimeBite x Tagimata Roadmap

Period: October 2026 through September 2027.

## Strategic Priority

1. Ship a focused TimeBite TestFlight before experimental integrations can slow the core product.
2. Stabilize a small shared action contract.
3. Prove one external interface can invoke TimeBite actions.
4. Build one M5Stack-powered charm prototype, not a family of electronics.
5. Sample a small Tagimata capsule: 2-3 looks, one flagship purse, one optional secondary purse.
6. Release in layers: TimeBite first, a summer ecosystem preview next, and a coherent September 2027 public presentation/pop-up readiness package last.

## Release Ladder

September 2027 is not the first release target. It is the polished integrated presentation target.

| Window | Release | Minimum Scope |
| --- | --- | --- |
| March-April 2027 | TimeBite iOS public beta or App Store v1 | Daily Intent, tasks/projects/goals, timer, Activity Ring, reflection, local persistence, beta-safe calendar/speech capture if stable |
| June 2027 | Partial ecosystem demo | TimeBite stable beta or public app, one external interface invoking shared actions, one hero look sampled, purse prototype/sample, rough M5Stack charm demo |
| July-August 2027 | Capsule preview / private demo / soft launch | 1-2 photographed looks, flagship purse sample, charm demo using shared context, optional Meta glasses command flow |
| September 2027 | Integrated presentation / pop-up readiness | Polished story across TimeBite, Tagimata, purse, charm, and wearable/spatial interface evidence |

## Release Protection Rule

TimeBite ships first and independently. Meta, Unity, M5Stack charm, fashion, and purse work can enrich the story, but none of them may block TestFlight, public beta, or App Store v1. Experimental work must use the shared action layer or remain a demo artifact.

## Month-By-Month Capacity Plan

| Month | Primary | Secondary | Maintenance | Parked |
| --- | --- | --- | --- | --- |
| Oct 2026 | TimeBite core loop, shared contracts | Architecture docs | Fashion mood/direction | Custom PCB, full collection |
| Nov 2026 | TimeBite alpha | Meta SDK research, M5Stack interaction design | Fashion sketches | Unity expansion |
| Dec 2026 | TestFlight readiness | M5Stack POC, purse dimensions | Meta feasibility notes | Manufacturing commitments |
| Jan 2027 | Beta testing/stabilization | Fashion tech drawings, purse tech pack, charm BOM | Unity scope | Custom electronics |
| Feb 2027 | TimeBite release readiness + manufacturer/sourcing gate | Japan/Asia vendor questions, M5Stack demo envelope | beta fixes | New product lines |
| Mar 2027 | TimeBite public beta/App Store v1 if stable | first external interface, sample conversations | VR demo if deadline-driven | PCB until evidence exists |
| Apr 2027 | TimeBite public release or rapid iteration | sample revisions, charm enclosure | Meta prototype refinement | Multi-character hardware |
| May 2027 | Cross-device demo | M5Stack evidence review for any bare ESP32/custom PCB path | fashion/purse costing | Large inventory buys |
| Jun 2027 | Partial ecosystem demo | RFQs for plausible pieces, app iteration | cost controls | New app features outside core |
| Jul 2027 | Capsule preview/private demo | small-run production decision | Meta polish if useful | Full VR productization |
| Aug 2027 | Soft launch/editorial prep | QA, packaging, narrative | cost controls | Late new SKUs |
| Sep 2027 | Polished integrated presentation/pop-up readiness | post-demo decisions | maintenance | Anything not demo-critical |

## Critical Paths

Software:
TimeBite core loop -> TestFlight -> stable shared actions -> March/April public beta or App Store v1 -> first external action invocation -> May cross-device demo -> June partial ecosystem demo -> September polished integrated presentation.

Hardware:
interaction spec -> M5Stack POC on one ESP32-family platform -> physical packaging -> evidence review -> optional bare ESP32/Rust-or-C firmware prototype -> PCB decision only if justified -> engineering samples -> feasibility for production.

Fashion:
hero look selection -> patterns/specs -> materials -> first samples -> fitting/revision -> editorial samples -> production decision.

Bag:
flagship design -> dimensions/tech pack -> materials/hardware -> sample -> revision -> costing/MOQ -> manufacturer decision.

Shared dependencies:

- The action contract gates Meta and charm integration.
- TimeBite release does not wait for Meta, Unity, M5Stack, fashion, purse, or manufacturing.
- Fashion/purse sampling must be ready enough for February 2027 sourcing.
- Bare ESP32 or custom PCB decisions must wait for M5Stack evidence.
- Charm firmware should use embedded C/C++ or Rust, not production MicroPython.
- Unity must stay time-boxed so it does not threaten TestFlight.

## Stop-Work Rules

If schedule slips, stop:

- Unity work after credible demo/submission needs are met.
- Meta or charm polish that is not needed for the first external interface.
- second charm electronics platform.
- additional Tagimata looks beyond 2-3 hero samples.
- custom PCB before M5Stack evidence.
- purse electronics in v1.
- integration work that does not use the shared action layer.
- any scope that delays March/April TimeBite public beta or App Store v1.

Keep moving:

- TimeBite core loop.
- TestFlight, public beta, and App Store readiness.
- shared action/data contracts.
- one flagship charm.
- one flagship purse.
- February sourcing readiness.
- June partial ecosystem demo.
- July/August capsule preview or soft launch.
