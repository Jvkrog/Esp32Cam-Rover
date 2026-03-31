
##  WiFi Car — ESP32-CAM Autonomous Rover

> Real-time video streaming rover with web-based remote control and embedded networking.

---

## Overview

WiFi Car is a compact robotic rover built using the ESP32-CAM, designed for remote navigation in environments that are unsafe or difficult for humans to access.
```
The system integrates:
- real-time video streaming  
- web-based control interface  
- embedded motor control  
```
This enables **live human-machine interaction over WiFi using a single microcontroller**.

---

## Key Features
```
-  Live camera feed via browser  
-  Web-based control dashboard  
-  Real-time movement control (Forward / Back / Left / Right)  
-  Compact and low-cost design  
-  WiFi-based remote access  
```
---

## System Architecture

```

    ┌──────────────┐
    │   User       │
    │  (Browser)   │
    └──────┬───────┘
           │  WiFi Commands
           ▼
    ┌──────────────┐
    │ ESP32-CAM    │
    │ (Web Server) │
    └──────┬───────┘
           │
  ┌────────┴────────┐
  ▼                 ▼
┌──────────────┐   ┌──────────────┐
│ Motor Driver │   │ Camera Stream│
│   (L298N)    │   │   (Live Feed)│
└──────────────┘   └──────────────┘

```

---

## System Flow

```

User Input → Web Server → Motor Control → Movement → Camera Feedback

```

### Working Logic
```
- ESP32-CAM hosts a local web server  
- User connects via WiFi using a browser  

**On user input:**
- Command is sent to ESP32  
- Motor driver executes movement  
- Camera streams live video back to user  
```
This creates a **real-time feedback loop for remote navigation**.

---

## Hardware Used
```
- ESP32-CAM  
- L298N Motor Driver  
- DC motors + robotic chassis  
- Battery pack  
```
---

## Software Stack
```
- Arduino framework  
- ESP32 Web Server  
- HTML / CSS / JavaScript (control interface)  
```
---

## Design Decisions

### Why ESP32-CAM
```
- Combines camera + WiFi + processing  
- Reduces hardware complexity and cost  
```
### Why Web-Based Control
```
- No app installation required  
- Accessible from any device with a browser  
```

### Why L298N Driver
```
- Simple and reliable motor control  
- Suitable for small robotic platforms  
```
---

## Real-World Use Cases
```
- Remote inspection in hazardous areas  
- Surveillance and monitoring  
- Educational robotics platforms  
- Prototype for autonomous vehicles  
```
---

## Limitations & Challenges
```
- Limited FPS due to ESP32-CAM constraints  
- WiFi range dependent on environment  
- No autonomous navigation (manual control only)  
```
---

## Key Learnings
```
- ESP32-CAM can handle both vision and control simultaneously  
- Real-time systems require efficient resource management  
- Power management is critical in mobile robotics  
- Simple architectures can still deliver strong functionality  
```
---

## Future Improvements
```
- Obstacle avoidance using sensors (ultrasonic / LiDAR)  
- Autonomous navigation modes  
- Cloud-based video streaming  
- Integration with mobile app control  
```


