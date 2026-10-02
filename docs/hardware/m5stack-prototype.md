# M5Stack Prototype

## Prototype Platform

Use one M5Stack platform to validate interaction before custom electronics. Treat M5Stack as the first ESP32-family implementation path, not as a throwaway detour from ESP32.

## Firmware Stack

Use embedded C/C++ or Rust for firmware. Do not use MicroPython for production firmware or for architecture-defining prototypes.

## Minimum Demo

The charm should answer:

- "How much focused work have I done today?"
- "What am I working on?"
- "Start a 25 minute focus session" or equivalent button-triggered flow.

## Components To Evaluate

- M5Stack core device
- microphone path or paired phone voice path
- speaker/audio response
- small display
- servo/vibration/simple motor
- BLE and Wi-Fi
- battery pack
- enclosure/plush constraints

## Measurements

- wake/interaction latency
- response latency
- battery drain under demo usage
- Wi-Fi/BLE reliability
- heat
- sound quality
- motor noise
- enclosure fit

## Exit Criteria

Move beyond M5Stack only after the prototype proves users understand and enjoy the interaction and the physical envelope is plausible.
