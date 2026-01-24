---
layout: post
title: Design and Analysis of a Cold Gas Rocket Engine
date: 2026-01-01 13:32:20 +0300
img: RocketDiagram.png
tags:
---

<p align="center">
  <img src="{{ site.baseurl }}/assets/img/Flowchart.png" width="80%">
</p>

## Project Overview

This project involves the comprehensive mathematical modeling, design, and transient performance analysis of a simplified cold gas rocket engine system.
Link for the documentation: https://drive.google.com/file/d/1JaMCLVBxpLGqF0QaDhQRlJG_UjNIgV9N/view?usp=sharing.

The study focuses on the gas dynamics of a pressurized oxidizer source and its temporal evolution as tank pressure depletes during operation.

---

## System Configuration and Specifications

The engine model consists of three primary components designed to simulate high-performance propulsion:

- **Pressurized Tank:** A 0.5 m³ cold gas tank pressurized with air to an initial pressure of 200 bar.
- **Combustor (Heat Addition Duct):** A one-dimensional duct that simulates a combustion chamber by adding thermal energy, raising the gas temperature to a maximum of 2200 K.
- **Convergent–Divergent (CD) Nozzle:** A fixed-geometry nozzle designed at a 100-bar reference condition to optimize mass flow rate and expansion behavior.

---

## Methodology and Physical Modeling

The project utilizes an unsteady flow model based on the fundamental conservation of mass and energy. Key theoretical frameworks include:

- **Isentropic Blowdown:** Used to model gas depletion inside the tank, treated as a lumped control volume.
- **Rayleigh Flow:** Applied to estimate total pressure losses resulting from heat addition within the combustor duct.
- **Shock Logic:** Determines whether the nozzle operates in an underexpanded supersonic state or if a normal shock forms inside the nozzle due to pressure decay.

---

## Key Performance Results

The simulation, conducted over a 50-second blowdown period, yielded the following insights:

- **Thrust and Flow:** Initial thrust of approximately **8.5 kN** with a mass flow rate near **4 kg/s**.
- **Thermal Efficiency:** Heat addition introduces a realistic **4.8% stagnation pressure loss**, minimized by maintaining low Mach numbers (0.1–0.3) in the heating duct.
- **Transient Behavior:** A performance discontinuity occurs at approximately **14 seconds**, marking the transition where tank pressure can no longer sustain supersonic exit flow, causing a shock to propagate into the nozzle.
- **Physical Consistency:** Final design results in a combustor diameter of **0.0861 m**, providing a cross-sectional area approximately **5.8× larger than the throat**, ensuring efficient heat addition.

---

## Technical Implementation

The system was validated using **MATLAB simulations** to generate thrust–time curves and temporal profiles for tank pressure and temperature.

This analytical approach enabled a detailed understanding of how initial conditions and thermal energy addition dictate the lifecycle and propulsion performance of the engine.

<p align="center">
  <img src="{{ site.baseurl }}/assets/img/MatlabRocket.png" width="85%">
</p>

