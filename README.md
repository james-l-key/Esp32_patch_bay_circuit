
# ESP32 Patch Bay - Hardware

This repository contains the hardware design files for the **ESP32 Patch Bay**, a project for dynamically reconfiguring guitar pedal signal chains. The main firmware repository can be found [here](https://github.com/phi/Esp32_patch_bay).

## Features
- **Schematic**: Designed in KiCad 9.0 (`circuit.kicad_sch`).
- **8-Pedal Support**: The design supports routing for up to 8 mono guitar pedals.
- **Audio Buffering**: Utilizes TL072 op-amps for input and output buffering to maintain signal integrity.
- **Power Isolation**: A TMA-1215D DC/DC converter generates isolated ±15V rails for the analog audio circuitry, ensuring low-noise operation.

## Hardware
The patch bay is built around the following key components:

- **Microcontroller**: ESP32-S3 (e.g., ESP32-S3-WROOM-1 module).
- **Audio Routing**:
  - CD4051B 8-channel analog multiplexers.
  - 3x TL072 dual op-amps for buffering.
- **Control**:
  - 74HC595 8-bit shift registers to control the multiplexers.
- **Power**:
  - The system is powered by a **12V DC** input.
  - Onboard regulators provide **±15V**, **+5V**, **-5V**, and **+3.3V** for all components.

For a complete list of components, please see the **Bill of Materials (BOM)** in the `docs` folder or the `HARDWARE.md` file.

## Power Requirements
- **Input Power**: The system uses an external **24V DC power supply**.
- **Isolated Dual Rails (±15V)**: 
- **Regulated Rails**: Onboard linear regulators provide stable **+5V**, **-5V**, and **+3.3V** is supplied by the ESP32-s3-Devkit-C for the digital components and ESP32-S3.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
