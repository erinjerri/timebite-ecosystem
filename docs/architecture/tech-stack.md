# Internal Tech Stack Map

This document maps the intended implementation stacks across TimeBite x Tagimata repositories. It is an internal planning reference, not a dependency lockfile. Child repos can refine details, but major stack changes should be reflected here before they become architecture.

## Stack Principles

- TimeBite iOS ships independently of experimental interfaces.
- Shared actions, entities, and device protocols are defined in this ecosystem repo before child repos specialize them.
- Prototype stacks should be close enough to production to produce trustworthy learning.
- Hardware firmware should be embedded C/C++ or Rust, not production MicroPython.
- Meta, M5Stack, Unity, and computer-vision experiments must convert into shared TimeBite actions instead of creating parallel product models.

## Repository Stack Summary

| Area | Repository | Primary Stack | Purpose | Notes |
| --- | --- | --- | --- | --- |
| TimeBite iOS app | `timebite-official` | Swift, SwiftUI, SwiftData/local-first storage | Production iOS app, TestFlight, App Store v1 | Owns canonical consumer UX and trusted local user state |
| iOS capture / planner ingestion | `timebite-official` or capture module | VisionKit, Vision, Swift concurrency | Phone-based document/image capture, OCR preprocessing, planner capture | Feeds confidence-scored ingestion into shared actions/entities |
| Handwriting/OCR evaluation | evaluation harness, possibly from `CYRA-AgentBeatsHackathon` learning | Swift/visionOS telemetry patterns, FastAPI/Python evaluation services, AI/OCR outputs | Score handwriting recognition accuracy and confidence | Internal QA/evaluation, not user-facing product logic |
| TimeBite Torus / cycles prototype | `timebite-torus-agentbeats` | Swift/SwiftUI iOS, visionOS spatial UI, Python backend/services, telemetry runs | Mini TimeBite beta, cycle matrix, torus/3D cycles, AgentBeats-related Green/Purple agent work | Carries the TimeBite/CYRA productivity direction separate from the CYRA newsletter submission repo |
| Meta glasses interface | `timebite-meta` | Meta AI glasses APIs, shared action client, converter layer | Voice/display interface into TimeBite | Converts Meta capture/commands into shared TimeBite actions |
| Meta CV capture + AI classes | `timebite-meta` or derived from `CYRA-AgentBeatsHackathon` patterns | Meta camera/capture APIs, AI classification/converter layer | Glasses-based capture, classification, action conversion | Must report confidence and preserve user correction flow |
| VR Start prototype | `timebite-meta-vr-start` | Unity, C#, Quest/VR Start tooling | Bounded spatial TimeBite demo | Archive after credible demo unless strategic evidence says otherwise |
| Marketing website | `timebite-site` or `cyra-site` derivative | Next.js, Tailwind CSS, Payload CMS, MongoDB, Cloudflare R2, Netlify | Public site, editorial pages, launch pages | Can reuse `erinjerri-portf-template` / `cyra-site` patterns |
| Interactive charm prototype | `tagimata-interactive` | M5Stack, embedded C/C++ or Rust, BLE/Wi-Fi | First charm behavior, audio/motion/display, device protocol | M5Stack is the first ESP32-family platform |
| Later charm electronics | `tagimata-interactive` | evidence-gated bare ESP32/devboard, C/C++ or Rust, possible custom PCB later | Smaller manufacturable module exploration | Only after M5Stack proves value and constraints |
| Shared contracts | `timebite-ecosystem` | Markdown specs, JSON schemas where useful, action/event/device contracts | Source of truth for cross-repo models | No child repo independently redefines core entities |
| MCP / connectors | `timebite-ecosystem` and child integration repos | MCP patterns, connector specs, TypeScript/Python only where appropriate | Agent/tool integrations and external service bridges | Must not replace local-first TimeBite product logic |

## TimeBite iOS Stack

Primary frameworks:

- Swift and SwiftUI for production UI.
- SwiftData or local-first persistence for canonical app state.
- Apple speech APIs for speech-to-task capture when reliable.
- EventKit for calendar visibility when privacy and UX are ready.
- WidgetKit, App Intents, ActivityKit, or Live Activities only if they support the core loop without delaying release.
- HealthKit only when it has a clear product reason and permission story.

Core user flows:

- Daily Intent.
- Tasks, projects, goals.
- Timer sessions.
- Activity Ring.
- Reflection.
- Local persistence and eventual sync.

Release rule:

The iOS app can ship without Meta, Unity, M5Stack, fashion, purse, or computer-vision capture. Capture features should not block the March/April 2027 public beta or App Store v1.

## TimeBite Torus And CYRA Lineage

There are two related but distinct AgentBeats-era references:

- `CYRA-AgentBeatsHackathon`: the Apple Vision Pro / visionOS-native CYRA Green Agent submission featured in the LinkedIn newsletter article.
- `timebite-torus-agentbeats`: the mini TimeBite / TimeBite Torus platform repo, with iOS, visionOS, cycle matrix, 3D torus/cycles, telemetry, and AgentBeats-related Green/Purple agent structure.

Use `CYRA-AgentBeatsHackathon` as the reference for visionOS-native agent evaluation, deterministic scoring, trace telemetry, FastAPI backend orchestration, A2A/MCP aspirations, and the Apple Vision Pro newsletter story.

Use `timebite-torus-agentbeats` as the reference for TimeBite-specific cycle modeling, torus/3D cycles, iOS/visionOS product structure, cycle dashboards, constrained assistant behavior, and telemetry-backed app evaluation.

## Capture, OCR, And Handwriting Recognition

Capture sources:

- iPhone camera capture through VisionKit/Vision where possible.
- Meta glasses capture through the Meta interface when available.
- Future planner or image imports if they preserve user consent and correction.

Processing shape:

1. Capture image or document.
2. Run OCR/handwriting recognition.
3. Classify recognized content into TimeBite concepts such as task, goal, project, date, timer, reflection, or note.
4. Produce candidate shared actions with confidence scores.
5. Ask the user to confirm or correct low-confidence results.
6. Store accepted output through the canonical TimeBite model.

Confidence requirements:

- Every capture result should expose confidence at the field or candidate-action level.
- Low confidence should trigger confirmation, not silent task creation.
- Evaluation should measure false positives, missed tasks, date/time mistakes, and user correction rate.
- Phone and glasses capture should be evaluated separately because image quality and framing will differ.

Evaluation stack:

- Reuse the actual `CYRA-AgentBeatsHackathon` stack pattern where useful: Swift/visionOS capture and telemetry concepts, FastAPI/Python backend evaluation services, structured traces, and reproducible scoring.
- Evaluation tools should compare raw recognition output, converted TimeBite action candidates, confidence, and corrected ground truth.
- Evaluation output should inform product thresholds, not become production app logic.

## Meta Interface Stack

Meta glasses should be treated as an interface into TimeBite, not a new productivity system.

Expected layers:

- Meta capture, voice, and display APIs.
- Converter layer from Meta intent/capture into shared TimeBite actions.
- Pairing/auth mediation where needed.
- Confidence and user-confirmation flow for capture-derived actions.
- Read-only commands first, then small write actions once trust is established.

Initial useful commands:

- `get_current_focus`
- `get_today_tasks`
- `start_timer`
- `complete_task`
- `get_daily_progress`

Meta CV and AI classes:

- Use AI classification for capture interpretation, not for defining canonical schema.
- Convert classified output into shared actions.
- Preserve confidence scores and source attribution.
- Keep the path optional for TimeBite release.

## Website And Marketing Stack

Default stack:

- Next.js.
- Tailwind CSS.
- Payload CMS.
- MongoDB.
- Cloudflare R2 for assets.
- Netlify for hosting.

Starting points:

- `erinjerri-portf-template`
- `cyra-site`

Site responsibilities:

- Product storytelling.
- Waitlist or interest capture.
- Editorial/launch pages.
- Press or pop-up readiness assets.
- CMS-managed fashion/product content if useful.

Site non-goals:

- It should not own canonical TimeBite user data.
- It should not block the iOS release.
- It should not become the primary app shell unless a later strategy explicitly changes that.

## Interactive Charm Hardware Stack

First platform:

- M5Stack as the first ESP32-family development platform.
- One flagship charm character.
- One electronics platform.
- Embedded C/C++ or Rust firmware.

Prototype capabilities:

- BLE/Wi-Fi connectivity.
- Button or voice-triggered interaction.
- Audio response.
- Simple display if useful.
- Simple expressive motion or haptics.
- Battery-envelope testing.
- Purse/charm attachment constraints.

Not the stack:

- Production MicroPython firmware.
- Multiple electronics platforms.
- One-off electronics per character.
- Custom PCB before M5Stack evidence.
- Purse-integrated electronics for v1.

Later hardware path:

M5Stack proof of concept -> evidence review -> optional smaller bare ESP32/devboard prototype using C/C++ or Rust -> custom PCB only if justified -> manufacturable module.

## UI Rendering Boundaries

| Surface | UI Stack | Notes |
| --- | --- | --- |
| iPhone | SwiftUI | Production interface and primary interaction surface |
| Widgets / system surfaces | WidgetKit, App Intents, ActivityKit if useful | Add only when they reinforce the core loop |
| Meta glasses | Meta display/voice interface | Thin command and feedback layer over shared actions |
| M5Stack charm | device display, LEDs, audio, motion, haptics | Minimal embodied feedback, not a full app UI |
| Unity VR | Unity UI / spatial UI | Prototype/demo only |
| Website | Next.js + Tailwind + Payload CMS | Marketing/editorial and launch content |

## Conversion Boundaries

Every non-iOS interface needs a converter into the shared TimeBite action layer:

- Meta voice command -> shared action.
- Meta image/CV capture -> candidate actions with confidence.
- iPhone VisionKit capture -> candidate actions with confidence.
- M5Stack button/voice event -> shared action.
- Unity prototype interaction -> mocked or shared action, depending on demo maturity.
- Website waitlist/contact event -> marketing/contact workflow, not core task schema.

Converters should preserve:

- source device
- timestamp
- confidence
- raw input reference where privacy allows
- user confirmation state
- idempotency key for mutating actions

## Open Stack Decisions

| Decision | Default | Evidence Needed To Change |
| --- | --- | --- |
| iOS persistence | SwiftData/local-first | migration risk, sync requirements, or performance data |
| Capture stack | VisionKit/Vision on iPhone, Meta capture on glasses | measured accuracy or platform limitation |
| OCR/handwriting evaluation | Swift/visionOS telemetry patterns plus FastAPI/Python scoring services | better existing tooling or integration cost |
| Charm firmware | C/C++ or Rust | production constraints, library support, developer speed |
| Charm hardware | M5Stack first | interaction, battery, enclosure, and user evidence |
| Website | Next.js/Tailwind/Payload/MongoDB/R2/Netlify | launch needs, CMS needs, hosting constraints |
| VR | Unity/C# | VR Start requirement changes |
