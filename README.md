# LoRa-Based Wireless Water Monitoring System

A group mini-project implementing a long-range wireless water level monitoring and automatic motor control system using ESP32 and RYLR890 LoRa modules.



## 🚀 Overview

This project replaces traditional RF + Encoder/Decoder + 555 Timer based water monitoring systems with a simplified LoRa-to-LoRa point-to-point communication architecture.

The system monitors both tank and sump levels and automatically controls the motor based on real-time conditions.



## 🔧 Technologies Used

- ESP32 (DEVKIT V1 – ESP32-WROOM-32)
- RYLR890 LoRa Module
- JSN-SR04T Waterproof Ultrasonic Sensor
- 5V Relay Module



## 📡 LoRa Communication

- Frequency Band: 868 / 915 MHz ISM
- Communication Type: Point-to-Point
- Range: 
  - 4–5 km (urban)
  - Up to 10–15 km (line-of-sight)
- Low power long-range transmission
- UART-based AT command interface

Establishing reliable LoRa-to-LoRa communication required tuning baud rate, addressing, and message formatting to ensure stable transmission without packet loss.



## ⚙️ Motor Control Logic

The motor operates based on tank–sump conditions:

| Tank | Sump | Motor |
|------|------|--------|
| TE   | SE   | OFF    |
| TE   | SF   | ON     |
| TF   | SE   | OFF    |
| TF   | SF   | OFF    |

Where:
- TE = Tank Empty  
- TF = Tank Full  
- SE = Sump Empty  
- SF = Sump Full  

The receiver ESP32 evaluates both inputs before actuating the relay, preventing overflow and dry running.



## 📊 Prototype Results

- Stable ultrasonic measurement within operational range  
- Reliable LoRa packet reception  
- Correct motor switching for all logic cases  
- Zero observed packet corruption during bench testing  



## 🔮 Future Scope

- Real-time cloud dashboard integration  
- Multi-tank scalable architecture  
- Industrial deployment using LoRaWAN  



## 📌 Project Type

Group Mini Project – Embedded Systems & Wireless Communication
