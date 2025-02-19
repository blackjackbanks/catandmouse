# catandmouse
# VR Remote-Controlled Robotic Mouse

## Overview
This project is a **VR-controlled robotic mouse** that allows remote interaction with pets via a VR headset. The system includes:
- **ESP32-based robotic mouse** with motor control and FPV camera streaming.
- **WebSockets for real-time control** over Wi-Fi.
- **Unity-based VR interface** for immersive remote control.
- **AI-assisted movement** to enhance pet engagement.

## Features
✅ **Motorized Movement** (Forward, Backward, Turn)  
✅ **FPV Camera Streaming** via WebRTC  
✅ **VR Headset Control** using Unity XR Toolkit  
✅ **AI-Assisted Play** with cat behavior detection (future feature)  

---

## Components & Compatibility
### **Electronics**
| Component | Model | Purpose |
|-----------|-------|---------|
| Microcontroller | ESP32 | Wireless control & processing |
| Motor Driver | DRV8833 | Controls two motors |
| Motors | N20 Micro Gear Motor | Moves the toy |
| Battery | 3.7V LiPo | Powers the system |
| FPV Camera | ESP32-CAM | Streams live video |
| Sensor | Ultrasonic HC-SR04 | Obstacle detection |

### **Software Stack**
| Component | Tool | Purpose |
|-----------|------|---------|
| Firmware | Arduino C / MicroPython | Motor control & WebSockets |
| Communication | WebSockets & WebRTC | Remote control & FPV feed |
| VR Development | Unity + XR Toolkit | VR interface |
| AI | OpenCV (future) | Cat movement tracking |

---

## Setup Instructions
### **1. Assemble the Hardware**
- Connect **ESP32** to **DRV8833 motor driver**.
- Attach **N20 motors** and **wheels**.
- Connect **ESP32-CAM** for video streaming.
- Power with **3.7V LiPo battery**.
- Mount **ultrasonic sensor** for obstacle detection.

### **2. Flash ESP32 Firmware**
1. Install **Arduino IDE**.
2. Add **ESP32 board support**.
3. Flash the provided `esp32_firmware.ino`.
4. Set up Wi-Fi credentials in the code.
5. Upload and verify WebSockets functionality.

### **3. Set Up Unity VR Interface**
1. Install **Unity 2021+ with XR Toolkit**.
2. Load the provided `UnityProject` folder.
3. Connect WebSocket client to ESP32.
4. Assign **VR controls** to Unity actions.
5. Run on **Meta Quest / HTC Vive**.

### **4. Stream FPV Camera to VR**
1. Use **WebRTC to stream ESP32-CAM video**.
2. Display video feed inside **VR UI**.
3. Optimize for **low-latency**.

### **5. Test & Iterate**
- Test movement response times.
- Improve motor acceleration curves.
- Optimize battery efficiency.

---

## Future Features
- **AI-powered cat tracking** using OpenCV.
- **Gesture-based VR control**.
- **Automatic docking & recharging**.
- **Expand to aerial toy (bird drone)**.

## Contribution Guide
1. Fork this repository.
2. Clone with `git clone https://github.com/YOUR-USERNAME/vr-robotic-mouse.git`.
3. Create a feature branch (`git checkout -b feature-name`).
4. Commit changes (`git commit -m "Added new feature"`).
5. Push and submit a PR.

---

## License
MIT License
