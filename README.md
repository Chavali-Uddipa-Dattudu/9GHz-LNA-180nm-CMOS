# 9 GHz Low Noise Amplifier (LNA) in 180nm CMOS

Welcome to my project repository! During my summer research internship at NIT Calicut, I designed and optimized a 9 GHz Low Noise Amplifier (LNA) using a 180nm CMOS technology node. I built this project for X-Band radar applications, specifically to help radar receivers detect small targets like drones, where low thermal noise and high stability are very important.

## Design Architecture

Working with a 180nm process at high frequencies can be difficult because of parasitic effects like signal leakage (the Miller Effect). To fix this, I used an **Inductively Degenerated Cascode Topology**. 

I also built an **Active LC L-Match Network** at the output. This helped step down the high internal impedance (150 Ω) to a standard 50 Ω RF output, which allowed me to get great gain without losing the perfect impedance match.

## Key Performance Metrics (Simulated at 9.0 GHz)

* **Forward Gain (S21):** 11.06 dB
* **Noise Figure (NF):** 1.41 dB
* **Input Return Loss (S11):** -17.06 dB (50 Ω Match)
* **Output Return Loss (S22):** -23.27 dB (50 Ω Match)
* **Reverse Isolation (S12):** -38.14 dB
* **Power Consumption (PDC):** 14.13 mW (from a 1.8V supply)
* **Figure of Merit (FoM):** 21.05 GHz/mW
* **Stability:** Unconditionally stable across the spectrum (Edwards-Sinsky μ > 1)

## Tools & Technologies Used

* **EDA Tool:** Cadence Virtuoso
* **Simulation:** ADE L, Spectre RF Simulator
* **Analysis:** S-Parameter sweeps, Noise Analysis, Z-Smith Charts, DC Operating Point
