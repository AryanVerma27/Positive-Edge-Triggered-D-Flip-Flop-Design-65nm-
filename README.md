# Positive Edge Triggered D Flip-Flop (DFF)

## Overview
This project presents the design, layout, and characterization of a Positive Edge Triggered D Flip-Flop (DFF) implemented in 65nm technology. The design focuses on minimizing area while maintaining robust timing characteristics under standard loading conditions.

## Design Specifications
* **Technology Node:** 65nm
* **Supply Voltage:** 1.2V
* **Cell Height:** 5.66 μm (Matches standard cell library)
* **Cell Width:** 3.50 μm
* **Total Area:** 19.81 μm²
* **Transistor Length:** 68 nm
* **Load Capacitance:** 45 fF

## Characterization Results
The DFF was characterized using HSPICE to determine critical timing metrics.

| Metric | Value | Description |
| :--- | :--- | :--- |
| **Setup Time** ($t_{setup}$) | **-61.9 ps** | Minimum time D must be stable *before* CLK edge. |
| **Hold Time** ($t_{hold}$) | **116.1 ps** | Minimum time D must be stable *after* CLK edge. |
| **Clock-to-Q Delay** ($t_{C-Q}$) | **198.8 ps** | Propagation delay from CLK rising edge to Q output. |
| **Average Power** | **1.35 μW** | Average power consumption @ 250 MHz. |

## Layout Details
* **Pin Pitch:** 0.52 μm
* **Offsets:** 0.39 μm (Left/Right)
* **Verification:** Passed DRC (Design Rule Check) and LVS (Layout Vs Schematic).
* **Extraction:** Parasitic R+C extracted via Calibre PEX.

## Simulation Waveforms
The repository includes simulation waveforms demonstrating:
1.  **Data Capture:** Correct latching of data on the rising clock edge.
2.  **Timing Violations:** Analysis of setup/hold failure regions.
3.  **Power Analysis:** Current draw during switching events.

---
**Authors:** Ganesh Manjunath & Aryan Verma  
**Course:** EECT / CE 6325 – VLSI Design  
**Instructor:** Prof. Carl Sechen
