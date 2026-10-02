# Hardware Architecture

## Principle

Build one excellent M5Stack prototype before designing multiple robotic characters or a custom PCB. M5Stack is the first ESP32-family hardware platform for the charm; "ESP32 transition" means moving from the M5Stack development module to a smaller bare ESP32/devboard or custom electronics path only after evidence supports it.

```text
            ONE ELECTRONICS PLATFORM

                   M5Stack
                      |
          +-----------+-----------+
          |           |           |
       Audio        Motion      Display
          |           |           |
          +-----------+-----------+
                      |
                 TimeBite API
                      |
                      v
                 Character
```

## Firmware Stack

Use embedded C/C++ or Rust for charm firmware. Do not use MicroPython for product firmware; at most, it can be a disposable bench-test tool that does not define architecture, device protocol, or production behavior.

## Reusable Module Path

M5Stack proof of concept -> evidence review -> optional bare ESP32/Rust-or-C firmware prototype -> custom PCB only if justified -> manufacturable electronics module -> reusable module across future Tagimata characters.

## Early Prototype Scope

Validate:

- voice or button-triggered interaction
- TimeBite connectivity
- audio response
- simple display if useful
- simple motion
- BLE/Wi-Fi behavior
- battery assumptions
- physical packaging constraints
- emotional expression

Defer:

- custom PCB
- multiple character-specific electronics
- certification spend
- production tooling
