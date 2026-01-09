# SRAM Bitline Precharge Circuit Design and Analysis

This repository documents a comparative study of SRAM bitline precharge circuits carried out as part of the EC3102 VLSI Design course.

The objective of the project was not only to design a functional precharge circuit, but to systematically evaluate multiple circuit topologies and transistor-type choices in order to identify an optimal solution for low-power, high-speed SRAM operation.

---

## Project Objective

The goal of this work was to analyze different SRAM precharge circuit topologies implemented using:
- NMOS-only transistors
- PMOS-only transistors

Each design was evaluated under identical simulation conditions to enable a fair and meaningful comparison.

---

## Design and Evaluation Methodology

The following steps were followed:

1. Designed four different precharge circuit topologies (labeled a–d).
2. Implemented each topology using both NMOS-only and PMOS-only transistor configurations.
3. Simulated all circuits using Cadence Virtuoso (gpdk 180) under identical biasing, load (100 pF), and stimulus conditions.
4. Extracted key performance metrics:
   - Propagation delay
   - Average static power
   - Average dynamic power
5. Compared results to identify the most suitable precharge circuit for SRAM bitline operation.

---

## Key Results

A total of eight precharge circuit variants were analyzed. The comparative results show that:

- Circuit (d) consistently exhibits the lowest propagation delay.
- NMOS-only implementations offer extremely low static power but vary in delay.
- The PMOS-only implementation of circuit (d) achieves:
  - Minimum propagation delay among PMOS designs
  - Near-zero static power consumption
  - Very low dynamic power

Based on these observations, **Circuit (d) – PMOS only** was selected as the optimal precharge topology.

---

## Final Design Choice

The selected precharge circuit was integrated with a standard 6T SRAM cell, providing:
- Fast bitline precharge
- Reduced leakage power
- Improved overall read/write readiness

This design choice reflects a balanced trade-off between speed and power efficiency, suitable for low-power SRAM architectures.

---

## Tools Used

- Cadence Virtuoso
- gpdk 180 nm technology node

---

## Repository Contents

- `report/`  
  Contains the complete project report with circuit schematics, simulation waveforms, extracted metrics, and comparative analysis.

---

## Notes

**Cadence Virtuoso schematic and simulation databases are not included due to licensing restrictions. Screenshots and results are provided for technical validation.**
