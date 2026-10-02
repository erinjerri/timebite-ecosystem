# Interactive Charm Roadmap

## Scope

Build one flagship robotic charm using one M5Stack development platform. M5Stack is the first ESP32-family platform; do not run a separate bare ESP32/custom PCB track until the M5Stack prototype produces evidence. Optionally explore one second character visually without a separate electronics platform.

## Firmware Stack

Use embedded C/C++ or Rust for charm firmware and the device protocol implementation. Do not use MicroPython for production firmware or architecture-defining prototypes.

## Primary Prototype Goals

- TimeBite action invocation
- voice or button interaction
- audio response
- simple expressive motion
- simple display if useful
- BLE/Wi-Fi proof
- battery envelope
- purse/charm attachment constraints
- emotional resonance

## Roadmap

1. Choose flagship character.
2. Define interaction script and emotional states.
3. Build M5Stack proof of concept.
4. Connect to TimeBite action endpoint or mock contract.
5. Add audio and simple motion.
6. Test battery and latency.
7. Explore plush/enclosure.
8. Decide whether moving from M5Stack to a smaller bare ESP32/devboard path is justified.
9. Create preliminary manufacturable module concept.
10. Decide whether custom PCB evidence threshold is met.

## Do Not Build Yet

- multiple electronic characters
- custom PCB
- production firmware architecture
- MicroPython production firmware
- certification package
- purse-integrated electronics
