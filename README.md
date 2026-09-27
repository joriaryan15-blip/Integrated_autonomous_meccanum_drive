# Autonomous Mecanum Drive Robot

An autonomous 4-wheel mecanum drive robot developed using ESP32, encoder feedback, BNO085 IMU, PID control, mecanum kinematics, and vision-based tracking.

This repository contains the development and testing of the robot's motion-control system, including wheel-speed tuning, encoder feedback, IMU integration, kinematics, PID control, waypoint following, and vision-based tracking.

---

## 🤖 Project Overview

The robot uses a 4-wheel mecanum drive system to achieve:

- Forward and backward motion
- Left and right lateral motion
- Diagonal motion
- Rotation
- Autonomous waypoint following
- Vision-based target tracking

The ESP32 is responsible for low-level motor control, encoder feedback, IMU data processing, kinematics, and motion control.

A camera-based vision system is used for target detection and tracking.

---

## ⚙️ Hardware

- ESP32
- 4 × DC geared motors
- Quadrature encoders
- BNO085 IMU
- Mecanum wheels
- Motor drivers
- Camera / vision system
- Jetson Nano for vision processing

---

## 💻 Software & Technologies

- C / C++
- Arduino
- ESP32
- PID Control
- Mecanum Kinematics
- Forward Kinematics
- Inverse Kinematics
- Encoder Feedback
- IMU Integration
- Computer Vision
- UDP Communication
- Autonomous Waypoint Following

---

## 🧠 Control System

The robot follows the following general control pipeline:

```text
             Camera
                │
                ▼
       Vision Processing
                │
                ▼
        Target Position
                │
                ▼
        Motion Controller
                │
        ┌───────┴───────┐
        │               │
        ▼               ▼
       IMU            Encoders
        │               │
        └───────┬───────┘
                ▼
          PID Controller
                │
                ▼
      Mecanum Kinematics
                │
                ▼
         Motor Commands
                │
                ▼
        Motor Drivers
                │
                ▼
       Mecanum Drive Robot
