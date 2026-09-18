# ESP32-S3-MESO-FEATHER

Open-source ESP32-S3 hardware project with a practical bring-up path from PCB design to first firmware smoke tests.

## Choose Your Goal
Start with one of these paths:
1. Review/edit PCB design in KiCad
2. Generate manufacturing outputs (Gerber/drill/BOM)
3. Start firmware development for board bring-up

## Required Tools
- **KiCad 8.x** (schematic/PCB)
- **Git** (version control)
- **Optional for firmware:** VS Code + PlatformIO extension

## Repository Structure
- `/hardware` — KiCad source files (`.kicad_pro`, `.kicad_sch`, `.kicad_pcb`)
- `/production` — manufacturing outputs (Gerber, drill, BOM)
- `/firmware` — PlatformIO starter project for ESP32-S3 smoke tests

## Current Status
The repository is now prepared for setup, but **real KiCad project files are still required** in `/hardware` before fabrication outputs can be generated.

## Hardware Workflow
1. Put KiCad project files into `/hardware`
2. Open project in KiCad 8.x
3. Run ERC and DRC
4. Verify rules, footprints, and ESP32-S3 pin mapping
5. Export Gerber, drill, and BOM to `/production`

## Prototype Workflow
1. Order PCB from `/production` outputs
2. Assemble first prototype
3. Run bring-up checks:
   - Power rails
   - USB connection
   - Boot mode behavior
   - Programming/upload path

## Firmware Quick Start (PlatformIO)
1. Open `/firmware` in VS Code with PlatformIO
2. Build and upload smoke test
3. Validate:
   - UART output
   - LED blink behavior
   - Basic Wi-Fi init (optional expansion)

See `/firmware/src/main.cpp` for starter LED + UART smoke test.
