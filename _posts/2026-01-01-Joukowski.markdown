---
layout: post
title: Flow Simulation over a Joukowski Airfoil
date: 2026-01-01 00:00:00 +0300
description: Aerodynamic analysis and potential flow simulation of a Joukowski airfoil using MATLAB, exploring lift, moment, and pressure distribution.
img: airfoil.png
fig-caption: Joukowski airfoil geometry and flow simulation
tags: [Aerodynamics, MATLAB, Joukowski Airfoil, Potential Flow]
---

## Project Overview: Flow Simulation over a Joukowski Airfoil

This project involves the aerodynamic analysis and potential flow simulation of a Joukowski airfoil. Using the Joukowski transformation in MATLAB, the study explores the relationship between airfoil geometry (thickness and camber) and its aerodynamic performance, approximating a NACA 3408 series profile.

### Aerodynamic Specifications and Conditions

- **Airfoil Profile:** Maximum thickness-to-chord ratio 8.5%, maximum camber-to-chord ratio 3.5%.  
- **Chord Length:** \(c = 1.25\,\mathrm{m}\)  
- **Angle of Attack:** Primary \(\alpha = 6^\circ\), comparative range \(-5^\circ\) to \(10^\circ\)  
- **Free-stream Velocity:** \(V_\infty = 125\,\mathrm{m/s}\)

### Key Aerodynamic Findings

- **Flow Visualization:** Streamlines show steady, inviscid potential flow with smooth trailing edge separation.  
- **Velocity and Pressure:** Upper surface experiences higher velocity and lower pressure; lower surface has lower velocity and higher pressure, generating lift.  
- **Coefficient Variations:** Lift coefficient (\(C_L\)) increases linearly with \(\alpha\); moment coefficient (\(C_M\)) at quarter-chord varies inversely with lift.

![Velocity Distribution over Airfoil]({{ '/assets/img/Velocity-dstrivution-over-airfoil-section.png' | prepend: site.baseurl }} "Velocity Distribution over Airfoil Section")

### Technical Implementation

MATLAB was used to parametrize airfoil surface coordinates, create a Cartesian grid, define the stream function, and compute local surface velocities using Bernoulli’s equation.

---

## Core Mathematical Framework

### 1. Airfoil Surface Coordinates

The Joukowski airfoil geometry is generated parametrically:

$$
r = b \left[ 1 + e(1 - \cos\theta) + \beta \sin\theta \right]
$$

$$
x = r \cos\theta, \quad y = r \sin\theta
$$

Where \(b\), \(e\), and \(\beta\) are constants derived from chord, thickness, and camber ratios.

### 2. Stream Function for Uniform Flow

The streamlines of inviscid potential flow at angle of attack \(\alpha\):

$$
\psi = V_\infty (y \cos\alpha - x \sin\alpha)
$$

### 3. Pressure Coefficient

The pressure coefficient \(C_p\) is computed from the local velocity \(V\) via Bernoulli’s principle:

$$
C_p = 1 - \left( \frac{V}{V_\infty} \right)^2
$$

### 4. Lift and Moment Coefficients

Using thin airfoil theory:

- **Lift Coefficient:**
$$
C_L = 2\pi \alpha_\mathrm{rad}
$$

- **Moment Coefficient (quarter-chord):**
$$
C_M = -0.25 C_L
$$

---

### 📄 Full Project Documentation

You can access the full documentation [here](https://drive.google.com/file/d/1g_vqC-yOLUGE2__aj8-Hl9rcbcWXQSNd/view?usp=drive_link).

---

<!-- MathJax Integration for LaTeX -->
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
