# Mobile Manipulator for Automated Hospital Delivery
### MATLAB + CoppeliaSim Robotics Simulation

## Overview
This project presents a **mobile manipulator robot** capable of automatically delivering essential supplies such as **food and medicines inside a hospital environment**. The system is simulated in **CoppeliaSim** and controlled using **MATLAB Remote API communication**.

The robot navigates through hospital corridors, detects objects using sensors, picks up supplies using a robotic arm, and delivers them to patient rooms.

This project was developed for **EEE 318 – Control Systems Laboratory**.

---

## Project Demo
Drive Link:  
https://drive.google.com/file/d/1zuleHLC0dWJZ8TA0cO7QtPaF3qz-WQCm/view

---

## Features
- Autonomous robot navigation
- Line following algorithm using vision sensors
- Object detection and localization
- Robotic arm pick-and-place operation
- Obstacle avoidance using proximity sensors
- MATLAB–CoppeliaSim remote communication
- Hospital environment simulation

---

## System Architecture

Main components of the system:

1. **Simulation Environment**
   - Virtual hospital environment created in CoppeliaSim
   - Patient cabins, corridors, dispatch center

2. **Mobile Robot**
   - KUKA YouBot mobile manipulator
   - Wheeled mobile platform
   - Robotic manipulator arm

3. **Sensors**
   - Vision sensors (line tracking and object detection)
   - Proximity sensors (obstacle detection)

4. **Control System**
   - MATLAB control scripts
   - Remote API communication

---

## Technologies Used

| Technology | Purpose |
|------------|--------|
| MATLAB | Control algorithms |
| CoppeliaSim | Robot simulation |
| KUKA YouBot | Mobile manipulator model |
| Vision Sensors | Line following & object detection |
| Proximity Sensors | Obstacle avoidance |
| Remote API | Communication between MATLAB and CoppeliaSim |

---

## Navigation System

The robot follows a **black path inside hospital corridors** using a vision sensor.

### Sensor Intensity Values
| Surface | Intensity |
|--------|-----------|
| Black Path | ~0.153 |
| White Floor | ~0.8 |

When the robot deviates from the black path, the sensor intensity changes significantly and the robot corrects its trajectory.

---

## Line Tracking Algorithm

Steps:

1. Read intensity value from vision sensor
2. Compare value with threshold
3. Detect deviation from path
4. Apply correction control
5. Adjust wheel velocity

This keeps the robot aligned with the navigation path.

---

## Object Detection

A vision sensor identifies supplies at the pickup point.

Process:

1. Detect object location
2. Estimate object position
3. Send coordinates to robotic manipulator

Correct object localization ensures accurate pickup.

---

## Manipulator Operation

The robotic arm performs:

- Object pickup
- Carrying supplies
- Placing items on patient room table

This enables automated delivery inside hospital cabins.

---

## Obstacle Avoidance

Proximity sensors detect obstacles such as:

- humans
- equipment
- walls

Robot behavior:

1. Detect obstacle
2. Stop movement
3. Wait until path is clear
4. Resume navigation

---

## Results

Simulation demonstrates:

- Autonomous navigation
- Object pickup and placement
- Successful delivery to hospital rooms
- Integration of sensors and control algorithms

---

## Project Structure
