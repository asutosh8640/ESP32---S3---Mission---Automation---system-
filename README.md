# ESP32-S3 Mission Automation System

An ESP32-S3 based embedded mission automation and control system developed and simulated in Wokwi.

The project demonstrates embedded firmware development using a state-machine architecture, timers, GPIO control, dual TM1637 displays, LEDs, buzzer, servo control, button-based event handling, override logic, and safety/fail states.

## 🚀 Project Overview

This project uses an ESP32-S3 as the main controller for a multi-stage automated mission sequence.

The firmware controls different system events through a structured state machine. User inputs trigger individual stages, while automatic sequences handle timed visual, audio, and actuator responses.

The complete system is currently implemented as a Wokwi simulation.

## ✨ Key Features

- ESP32-S3 based embedded controller
- Multi-stage state-machine architecture
- Master countdown timer
- Launch countdown timer
- Dual TM1637 7-segment displays
- Multiple push-button inputs
- 8 status and warning LEDs
- Buzzer/audio feedback
- Servo-controlled mechanism
- Override control logic
- Deactivation sequence
- Extraction sequence
- Win and completion states
- Game-fail/safety state
- Timer pause, resume and reset
- Adjustable master timer
- Demo mode for rapid simulation
- Serial debugging at 115200 baud
- Custom low-level TM1637 driver without an external display library

## 🧠 State Machine

The firmware uses the following states:

`text
READY
  ↓
RUNNING
  ↓
CAGE_RELEASED
  ↓
OPERATIONS
  ↓
WAKEUP
  ↓
EVENT_REVEAL
  ↓
WALL_RELEASE
  ↓
LAUNCH
  ↓
DEACTIVATION
  ↓
SHUTDOWN
  ↓
WIN
  ↓
EXTRACTION
  ↓
COMPLETE
