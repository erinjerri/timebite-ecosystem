# Final System Design Answers

1. Minimum TimeBite TestFlight: Daily Intent, tasks, projects/goals, prioritization, timer, completed session, Activity Ring, reflection, local persistence, basic calendar visibility, speech-to-task capture.
2. App Store submission requires reliability, privacy/auth compliance, stable persistence/migrations, polished core UX, accessible states, and no dependency on unfinished experimental integrations.
3. Meta glasses should initially demonstrate asking for current focus, starting/completing a task, and hearing/seeing daily progress from the shared action layer.
4. VR Start should receive a strict hackathon time box: enough for a convincing spatial Daily Intent -> focus -> timer -> progress -> reflection demo, then freeze/archive unless strategic value is proven.
5. Prioritize 2-3 looks: contemporary Filipiniana top + bottom + purse + charm; black evening/halter or LBD-inspired look + purse + charm; one alternate silhouette such as longer skirt/dress with 16-point motif.
6. Prioritize one flagship purse for phone/planner/charm/accessories and one optional compact evening/crossbody variant.
7. First M5Stack prototype character: choose the strongest flagship Tagimata character for emotional expression, simple motion, and brand recognition; do not split electronics across characters.
8. Optional second character should demonstrate visual/product variation only: different shell, plush, charm styling, or colorway using the same electronics envelope.
9. Before February 2027: hero looks, drawings/specs, material direction, purse dimensions/tech pack, charm POC dimensions, movement/audio/battery assumptions, preliminary BOM.
10. After February: custom PCB, certification, production tooling, broad collection expansion, multi-character electronics, large inventory commitments.
11. M5Stack is the first ESP32-family charm platform. Move to a smaller bare ESP32/devboard only after interaction value, connectivity, battery envelope, motion, audio, and enclosure constraints are validated.
12. Before paying for custom PCB: working M5Stack demo, stable feature list, target dimensions, power budget, BOM, manufacturer input, and evidence users care. Firmware should be embedded C/C++ or Rust; do not use MicroPython for production firmware.
13. Stabilize early: actions, entity schemas, event model, device/source attribution, idempotency, pairing/permissions.
14. Do not stabilize yet: AI provider, sync provider, Unity architecture, final Meta UX, final charm shape, full fashion sizing, PCB layout.
15. First shared architecture proof: whichever is fastest between Meta glasses and M5Stack, but the best thesis demo is Meta `get_current_focus` plus charm `get_daily_progress` reading the same state.
16. Realistic critical path: TimeBite beta -> shared actions -> February sourcing readiness -> March/April public beta or App Store v1 -> first external interface -> May cross-device demo -> June partial ecosystem demo -> July/August capsule preview or soft launch -> September polished presentation.
17. If schedule slips, stop Unity expansion, Meta/charm polish beyond first external action proof, second electronics platform, extra looks, purse electronics, custom PCB, broad AI orchestration, and non-demo-critical integrations.
