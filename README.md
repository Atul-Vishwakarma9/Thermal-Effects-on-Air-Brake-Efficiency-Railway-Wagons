# Thermal Effects on Air Brake Efficiency in Railway Wagons

This repository contains a **MATLAB-based simulation project** that investigates how **ambient temperature affects the efficiency of air brake systems** used in railway wagons.

The project was carried out as part of a **Summer Internship at Wagon Repair Shop, Raipur**, under the **Department of Mechanical Engineering, NIT Raipur**.

---

##  Problem Statement

Railway air brake systems rely on compressed air to transmit braking signals along long wagon chains.  
The physical properties of air—such as **density**, **speed of pressure wave propagation**, and **viscosity**—vary significantly with ambient temperature.

These variations can lead to:
- Delayed brake application
- Uneven braking across wagons
- Increased stopping distance
- Higher safety risk in extreme weather conditions

This project quantifies these effects using thermodynamic principles and MATLAB simulations.

---

##  Objectives

- Study the effect of ambient temperature on air brake system efficiency
- Analyze variation in:
  - Air density
  - Pressure wave (sound) speed
  - Brake response time
- Develop a MATLAB simulation model
- Understand operational safety implications in cold and hot climates

---

##  Theoretical Background

The simulation is based on fundamental thermodynamics and fluid mechanics:

- **Air Density (Ideal Gas Law)**  
  \[
  \rho = \frac{P}{R T}
  \]

- **Speed of Pressure Wave (Sound Speed)**  
  \[
  v = \sqrt{k R T}
  \]

Where:
- \( P \) = Pressure  
- \( R \) = Specific gas constant for air  
- \( T \) = Absolute temperature  
- \( k \) = Adiabatic index  

---

##  Methodology

1. Ambient temperatures considered: **-10°C to 50°C**
2. Convert temperature from Celsius to Kelvin
3. Calculate air density for each temperature
4. Compute pressure wave propagation speed
5. Estimate brake response time:
   \[
   t = \frac{\text{Pipe Length}}{\text{Sound Speed}}
   \]
6. Visualize results using MATLAB plots

---

##  MATLAB Implementation

The core MATLAB script performs:
- Thermodynamic calculations
- Loop-based temperature analysis
- Graphical visualization of results

