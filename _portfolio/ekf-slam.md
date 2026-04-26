---
title: "EKF-SLAM and LQR Control"
excerpt: "Autonomous vehicle simulation integrating state estimation and optimal control."
collection: portfolio
permalink: /portfolio/ekf-slam/
---

## Overview

This project implements an autonomous vehicle simulation combining **state estimation (EKF-SLAM)** and **optimal control (LQR)**.

The goal is to enable robust navigation under uncertainty by integrating perception and control into a closed-loop system.

---

## Key Contributions

- Implemented **Extended Kalman Filter (EKF)** for localization and mapping  
- Derived and implemented **Jacobian-based linearization** for nonlinear systems  
- Designed a **discrete-time LQR controller** for trajectory tracking  
- Integrated estimation and control in a closed-loop simulation  

---

## Results

- Achieved ~1.36 m average tracking error  
- Completed trajectory in ~100 s (benchmark: 250 s)  
- Demonstrated stable navigation under sensor noise  

---

## Tools & Technologies

- Python  
- NumPy  
- Robotics simulation environment  
- Control theory (LQR, linearization)  
