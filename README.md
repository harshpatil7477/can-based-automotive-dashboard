# CAN-Based Automotive Dashboard System

## Project Overview

The **CAN-Based Automotive Dashboard System** is an embedded systems project developed using three PIC18F4580 microcontrollers communicating through the Controller Area Network (CAN) protocol.

The system demonstrates communication between multiple ECUs to acquire, process, and display vehicle parameters. It uses Embedded C to implement CAN communication, ADC-based sensor input, keypad-based controls, and an LCD dashboard interface.

## System Architecture

The project consists of three ECUs:

### ECU 1 – Speed and Gear Monitoring
- Reads speed input through the ADC.
- Reads gear selection using a digital keypad.
- Transmits speed and gear information over the CAN bus.

### ECU 2 – RPM and Indicator Control
- Reads RPM-related analog input through the ADC.
- Accepts indicator commands through a keypad.
- Transmits RPM and indicator status over CAN.

### ECU 3 – Dashboard Display
- Receives vehicle information through CAN communication.
- Displays speed, gear, and RPM information on the CLCD.
- Controls indicator LEDs based on received commands.

## Hardware Components

- PIC18F4580 Microcontrollers (3 ECUs)
- CAN Transceivers
- 16x2 Character LCD (CLCD)
- Digital Keypads
- ADC Analog Inputs
- Indicator LEDs
- 20 MHz Crystal Oscillator

## Software and Tools

- Embedded C
- MPLAB X IDE v5.35
- MPLAB XC8 Compiler v4.00
- PIC18F4580
- CAN Protocol
- ADC
- CLCD
- Digital Keypad
- Timer Interrupts

## CAN Communication

The ECUs exchange data using standard CAN message identifiers.

| CAN ID | Parameter | Data Length |
|---|---|---|
| 0x10 | Speed | 1 Byte |
| 0x20 | Gear Position | 1 Byte |
| 0x30 | RPM | 2 Bytes |
| 0x50 | Indicator Status | 1 Byte |

## Key Features

- Multi-ECU communication using the CAN protocol.
- ADC-based vehicle parameter acquisition.
- Keypad-based gear and indicator controls.
- Real-time data exchange between ECUs.
- CLCD-based dashboard information display.
- LED-based indicator status representation.

## Learning Outcomes

Through this project, I gained practical experience in:

- Embedded C programming.
- PIC18F4580 microcontroller programming.
- CAN protocol implementation and communication.
- ADC interfacing and digital keypad handling.
- LCD interfacing.
- Multi-ECU embedded system design.
- Hardware and software integration.

## Author

**Harsh Patil**

GitHub: [harshpatil7477](https://github.com/harshpatil7477)

---

*This project was developed as part of my Embedded Systems training and practical learning.*
