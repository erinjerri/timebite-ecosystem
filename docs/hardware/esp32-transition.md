# ESP32 Transition

## When To Transition

M5Stack is already the first ESP32-family prototyping platform for the charm. In this document, "ESP32 transition" means moving from the M5Stack development module to a smaller bare ESP32/devboard or custom-board path. Make that move only after:

- the core interaction works
- TimeBite connectivity is proven
- the battery envelope is measured
- motion/audio/display requirements are known
- enclosure dimensions are constrained
- manufacturer conversations indicate the M5Stack shape/cost is unsuitable for next-stage samples

## ESP32 Prototype Goals

- reduce size
- validate component choices
- separate prototype wiring from development-kit assumptions
- prepare for PCB requirements
- keep firmware aligned to shared device protocol

## Firmware Stack

Use embedded C/C++ or Rust. Do not use MicroPython for production firmware or for prototypes that define the device protocol, BLE/Wi-Fi behavior, power behavior, or app integration contract.

## Do Not Jump Straight To PCB

ESP32 breadboard/devboard work should answer what the PCB needs. It is not skipped just because M5Stack worked once.
