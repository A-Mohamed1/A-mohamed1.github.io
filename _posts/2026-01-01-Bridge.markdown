---
layout: post
title: Phase Two Bridge Final Design
date: 2026-01-01 00:00:00 +0300
description: Design, fabrication, and analysis of a lightweight Pratt truss bridge with optimized strength-to-weight ratio.
img: Bridge-Drawing.png
tags: [Mechanics, Structures, Truss Bridge, MATLAB, Engineering]
---

## Project Overview: Phase Two Bridge Final Design

This project involved the design, fabrication, and structural analysis of a lightweight truss bridge prototype developed for the Mechanics of Materials course. The primary goal was to optimize the strength-to-weight ratio while ensuring ease of assembly using common materials.

### System Configuration and Specifications

- **Truss Type:** Pratt truss configuration, efficient for tension-dominated lower members.
- **Materials:** Constructed using tongue depressors as structural members.
- **Dimensions:** Main span \(0.40\,\mathrm{m}\), height \(0.12\,\mathrm{m}\), depth \(0.12\,\mathrm{m}\).
- **Physical Weight:** \(0.220\,\mathrm{kg}\).

### Technical Methodology and Analysis

- **Member Force Analysis:** Members were classified under tension (T) or compression (C).
- **Geometric Stability:** Tongue depressors arranged into vertical and diagonal units to maximize structural integrity.
- **Stress Distribution:** Internal forces under a simulated 100 kg load ranged from 50.0 to 100.0 units.
- **Safety Margin:** Experimental results suggest the bridge can support additional weight beyond the test limits.

### Key Performance Results

- **Load Capacity:** Successfully supported a maximum load of 58 kg without failure.
- **Efficiency Score:** Calculated as 263.63.
- **Predictive Capacity:** Estimated additional support of up to +40 kg.

---

## Key Mathematical Frameworks

### 1. Bridge Performance Metric

The efficiency of the bridge was quantified by:

$$
\text{Score} = \frac{\text{Load (without failure)}}{\text{Weight of the bridge}}
$$

### 2. Experimental Calculation

$$
\text{Score} = \frac{58\,\mathrm{kg}}{0.220\,\mathrm{kg}} \approx 263.63
$$

### 3. Member Force Analysis

Internal forces in the Pratt truss:

- **Compression Members:** \(F_{\text{top\_chord}} = 100.0\,\mathrm{units} \,(\mathrm{C})\)  
- **Tension Members:** \(F_{\text{bottom\_chord}} = 50.0\,\mathrm{units} \,(\mathrm{T})\)  

![Member Force Analysis]({{ '/assets/img/Member-force-analysis.png' | prepend: site.baseurl }} "Member Force Analysis")

### 4. Reaction Forces

For a centrally applied load of 100 units:

$$
\sum F_y = 0 \implies A_y + E_y = 100.0, \quad A_y = 50.0, \, E_y = 50.0
$$

---

### 📄 Full Project Documentation

You can access the full documentation [here](https://drive.google.com/file/d/1m-5r0eqV4NRF8oGtmTI7A6ttSU9DQUL4/view?usp=drive_link).

---

<!-- MathJax Integration for LaTeX -->
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
