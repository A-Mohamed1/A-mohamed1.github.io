---
layout: post
title: Automobile Active Suspension System Control
date: 2026-01-10 00:00:00 +0300
img: Quarter-car-model.png
tags:
---

## Project Overview

This project focuses on the **mathematical modeling, analysis, and control system design** of an automotive **active suspension system**.  
The primary objective is to overcome the inherent trade-off between **ride comfort** (passenger comfort) and **handling stability** (road holding) by introducing an **active force actuator** operating in parallel with passive suspension components.

**📄 Full Documentation:**  
[View technical report (Google Drive)](https://drive.google.com/file/d/1mTypBeYipgtXAwsrK_uZZkxzaRj4vfiB/view?usp=drive_link)

---

## System Configuration and Modeling

The vehicle dynamics are represented using a **two-degree-of-freedom (2-DOF) linear quarter-car model**, capturing the essential vertical dynamics of the suspension system.

<p align="center">
  <img src="{{ site.baseurl }}/assets/img/Quarter-car-model.png" width="65%">
</p>

- **Sprung Mass ($m_1$):** Represents the vehicle body and passenger load  
- **Unsprung Mass ($m_2$):** Represents the wheel and tire assembly  
- **Actuator ($u$):** Hydraulic or electromagnetic actuator generating control force  
- **Road Disturbance ($w$):** External input representing road irregularities  

The equations of motion are derived using **Newton’s Second Law** and later converted into a **state-space representation** to enable advanced control design.

<p align="center">
  <img src="{{ site.baseurl }}/assets/img/Modeling-equations.png" width="75%">
</p>

---

## Methodology and System Analysis

Before controller synthesis, the system’s fundamental properties were analyzed using **MATLAB**:

- **Controllability:**  
  The controllability matrix was full rank (**Rank = 4**), confirming that all system states can be driven by the actuator input.

- **Observability:**  
  The observability matrix also achieved **Rank = 4**, ensuring that all internal states can be reconstructed from measured outputs.

- **Open-Loop Stability:**  
  Eigenvalue analysis of the state matrix $A$ showed all eigenvalues with **negative real parts**, indicating an inherently stable open-loop system.

<p align="center">
  <img src="{{ site.baseurl }}/assets/img/state-space.png" width="75%">
</p>

---

## Control Strategies

Three control approaches were designed and evaluated:

- **State Feedback Controller:**  
  Designed using **pole placement**, achieving a settling time below **5 seconds**.

- **Linear Quadratic Regulator (LQR):**  
  Optimized using **Bryson’s rule**, with weighting matrices  
  $Q = \mathrm{diag}(10^6, 10^3, 10^4, 10^2)$  
  to strongly penalize body displacement while limiting actuator effort.

- **PID Controller:**  
  Implemented for comparison using gains  
  $K_p = 5000,\; K_i = 1000,\; K_d = 2000$  
  to regulate suspension displacement.

---

## Technical Results and Validation

The controlled system was subjected to a **0.1 m step road disturbance**.

- **Performance:**  
  Significant reduction in vertical acceleration of the sprung mass, improving ride comfort.

- **Settling Behavior:**  
  Both **LQR** and **State Feedback** controllers satisfied the **5-second settling time constraint**.

- **Numerical Simulation:**  
  Time-domain responses were solved using **Simulink** and a **fourth-order Runge–Kutta (RK4)** integration scheme.

<p align="center">
  <img src="{{ site.baseurl }}/assets/img/Numerical-solution-displacements.png" width="80%">
</p>

---

## Summary

This project demonstrates how **modern control techniques** can be applied to automotive suspension systems to simultaneously improve **comfort and handling**.  
The combination of **state-space modeling**, **optimal control**, and **numerical simulation** provides a robust framework for real-world vehicle dynamics applications.
