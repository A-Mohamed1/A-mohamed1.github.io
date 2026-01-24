---
layout: post
title: Design and Analysis of a Cold Gas Rocket Engine
date: 2026-01-01 13:32:20 +0300
description: # Add post description (optional)
img: # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags:
---
Project Overview: Design and Analysis of a Cold Gas Rocket Engine
This project involves the comprehensive mathematical modeling, design, and transient performance analysis of a simplified rocket engine system. 
The study focuses on the gas dynamics of a pressurized oxidizer source and its temporal evolution as pressure depletes during operation.
System Configuration and Specifications
The engine model consists of three primary components designed to simulate high-performance propulsion:
• Pressurized Tank: A 0.5 m^3 cold gas tank pressurized with air to an initial 200 bar.
• Combustor (Heat Addition Duct): A one-dimensional duct that simulates a combustion chamber by adding thermal energy, raising the gas temperature to a maximum of 2200 K.
• Convergent-Divergent (CD) Nozzle: A nozzle with fixed geometry designed at a 100-bar reference point to optimize mass flow rates and expansion.
Methodology and Physical Modeling
The project utilizes an unsteady flow model based on the fundamental conservation of mass and energy. Key theoretical frameworks include:
• Isentropic Blowdown: Used to model the gas depletion inside the tank, treated as a lumped control volume.
• Rayleigh Flow: Applied to estimate the total pressure loss resulting from heat addition within the combustor duct.
• Shock Logic: The program incorporates logic to determine if the nozzle is operating in an underexpanded supersonic state or if a normal shock has formed inside the nozzle due to pressure drops.
Key Performance Results
The simulation, conducted over a 50-second blowdown period, yielded the following insights:
• Thrust and Flow: The engine generates an initial thrust of approximately 8.5 kN with a mass flow rate of nearly 4 kg/s.
• Thermal Efficiency: Heat addition causes a realistic 4.8% loss in stagnation pressure, which is minimized by maintaining low Mach numbers (0.1 to 0.3) in the heating duct.
• Transient Behavior: A significant performance discontinuity occurs at approximately 14 seconds, representing the transition where tank pressure becomes insufficient to maintain supersonic exit flow, causing a shock to move into the nozzle.
• Physical Consistency: The final design produced a combustor diameter of 0.0861 m, which provides a cross-sectional area roughly 5.8 times larger than the throat to ensure efficient heat addition.
Technical Implementation
The system was validated using MATLAB simulations to generate thrust-time curves and temporal behaviors for tank pressure and temperature. 
This analytical approach allowed for a detailed understanding of how initial conditions and thermal additions dictate the lifecycle and propulsion performance of the engine.
