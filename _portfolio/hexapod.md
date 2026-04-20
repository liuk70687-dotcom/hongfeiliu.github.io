---
title: "Dancing Hexapod Robot"
excerpt: "A human-carrying legged robot for assistive performance, integrating mechanical design, embedded control, and autonomous robotics."
collection: portfolio
permalink: /portfolio/hexapod/
author_profile: true
---

## Overview

The **Dancing Hexapod Robot** is an ongoing CMU Mechatronic Design project developed for **Kinematic/Kinesthetic**, a live performance by **AXIS Dance Company**. The goal is to build a **human-carrying mobility robot** that uses **legs rather than wheels as the primary locomotion system**, while remaining compact, safe, and expressive on stage.

This project is especially meaningful to me because it treats assistive robotics not only as a mobility tool, but also as a medium for **performance, embodiment, and creative motion**.

---

## Project Goals

The robot is being designed to satisfy several core performance and engineering requirements:

- Carry a rider safely and stably
- Move forward and backward with **leg-driven locomotion**
- Perform **zero-radius turning**
- Operate safely around performers with predictable behavior
- Maintain a compact footprint for stage use and transport
- Support low-noise, robust operation with emergency-stop capability

---

## My Role

I contribute primarily to the **mechanical design and system integration** side of the project.

My work includes:

- Designing and refining the **Klann-linkage-based leg assemblies**
- Creating detailed CAD models for the **chassis, leg mechanisms, and mounting interfaces**
- Supporting the integration of **Jetson Nano**, **ESP32**, motors, and sensing hardware
- Contributing to **gait development**, manufacturability improvements, and subsystem iteration
- Helping translate high-level system goals into practical mechanical and embedded implementation choices

---

## System Architecture

The robot uses a layered cyber-physical architecture:

- **Jetson Nano** for higher-level perception, navigation, and autonomy tasks
- **ESP32 microcontrollers** for timing-critical motor control, sensing, and low-level I/O
- A forward sensing stack centered around RGB-D perception, IMU feedback, and force/contact sensing
- A locomotion pipeline that converts body-level commands into gait timing and leg actuation

This split architecture makes it possible to combine **embedded real-time control** with more computationally intensive autonomy functions. :contentReference[oaicite:2]{index=2}

---

## Mechanical Design

A central design decision was the use of a **Klann-style linkage** for the primary leg mechanism. Compared with more complex articulated legs, this approach reduces actuator count and software dependence while preserving a mechanically encoded walking trajectory. The design direction prioritizes:

- Reproducible gait timing under load
- Lower integration risk
- Fewer actively controlled degrees of freedom
- Better manufacturability and robustness for staged testing

The overall robot is organized into several major subsystems:

- Main body/base structure for rider support
- Wheel-support assembly for load sharing
- Left and right Klann-style leg sets for forward/backward locomotion
- Side-leg subsystem for stabilization and expressive motion
- Protected electronics compartment for compute, wiring, and power distribution

Turning is implemented through a **differential-speed strategy**, where independently controlled left and right leg sets enable in-place turning. :contentReference[oaicite:3]{index=3}

---

## Embedded and Controls Work

On the controls side, the project combines embedded firmware bring-up, gait control, and sensing integration.

Current implementation directions include:

- Motor control through a structured local control stack
- ESP32 telemetry for IMU and force-sensor readings
- Operator-side GUI and ROS-based interfaces
- Simulation support through **MuJoCo + ROS**
- Jetson-side RGB-D SLAM and deployment tooling

This has made the project a strong systems-engineering experience, because it requires consistent interfaces across simulation, embedded firmware, and real hardware. :contentReference[oaicite:4]{index=4}

---

## Key Engineering Challenges

This project involves several nontrivial engineering tradeoffs:

### 1. Stability under payload
Because the robot carries a rider, stability is a primary requirement. Mechanical geometry, support polygon design, and gait smoothness all directly affect rider safety.

### 2. Mechanical simplicity vs. locomotion flexibility
The Klann linkage reduces control complexity, but it also constrains gait shape. This means performance must be improved through **mechanism tuning and hardware iteration**, not only software.

### 3. Compute split and integration
Keeping autonomy onboard improves capability, but tightens power, packaging, and thermal constraints. The Jetson/ESP32 split helps manage this tradeoff.

### 4. Stage-safe operation
Unlike many robotics projects, this system must also satisfy artistic and live-performance constraints: predictable motion, low noise, compact packaging, and safe human interaction. :contentReference[oaicite:5]{index=5}

---

## Current Status

The project is still in progress. Current work spans:

- CAD refinement of the body and leg assemblies
- Embedded and sensing bring-up
- Gait control development
- MuJoCo/ROS simulation support
- Integration of perception and low-level interfaces
- Mechanical prototyping and manufacturability improvements

The broader implementation stack already includes simulation, operator UI, Jetson deployment, and ESP32 firmware pathways, while physical assembly and final packaging continue to evolve. :contentReference[oaicite:6]{index=6}

---

## What I Learned

This project has strengthened my ability to work across the boundary between:

- **Mechanical design**
- **Embedded control**
- **Systems integration**
- **Robotics architecture**

More importantly, it has taught me how to make design decisions under real constraints: payload, safety, manufacturability, noise, packaging, and integration schedule. It is the most complete example of my interest in building **real robotic systems**, rather than isolated components.

---

## Links

- [Team Website](https://mechatronic-design-s2026-team-2.github.io/Website/)
