# LoRa-Based Water Monitoring System

## Overview
This project implements a long-range wireless water monitoring system using LoRa technology.  
The system monitors water levels in a tank and sump and automatically controls a motor based on predefined conditions.

Unlike previous implementations using RF 433 MHz modules with encoder/decoder ICs and 555 timers, this project simplifies the architecture by implementing direct LoRa-to-LoRa point-to-point communication using RYLR890 modules.

---

## Technologies Used
- ESP32 (DevKit V1 - ESP32-WROOM-32)
- JSN-SR04T Waterproof Ultrasonic Sensor
- RYLR890 LoRa Modules(868/915 MHz ISM Band)
- UART-based AT Command Communication
- 5V Relay Module

---

## System Architecture
- 2 Transmitter Nodes (Tank & Sump)
- 1 Receiver Node (Motor Control)
- Point-to-point LoRa Communication

---

## Working Logic
Motor ON only when:
- Tank = EMPTY
- Sump = FULL

Motor OFF for all other combinations.

---

## Key Highlights
- Long-range communication capability (km-scale in open environments)
- Simplified hardware compared to traditional RF + encoder/decoder systems
- Reduced circuit complexity
- Reliable UART-based communication
- Modular and scalable design

---

## Project Outcome
The system successfully demonstrated:
- Stable ultrasonic sensing
- Reliable LoRa message transmission
- Correct motor control logic execution

---

## Future Scope
- Cloud integration (IoT dashboard)
- GSM alert system
- Water usage analytics
- Multi-node scalability
