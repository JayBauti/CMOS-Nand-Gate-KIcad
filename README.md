CMOS NAND Gate Simulation using KiCad and ngspice
Overview

This project demonstrates the design and transient simulation of a CMOS NAND gate using discrete NMOS and PMOS transistors in KiCad 9.
The goal is to understand CMOS logic operation at the device level and verify the NAND truth table using time-domain (transient) analysis.

Objective

Design a CMOS NAND gate using PMOS pull-up and NMOS pull-down networks

Apply pulse inputs to generate all logic combinations

Verify NAND logic behavior through transient simulation

Tools Used

KiCad 9 (Schematic capture + ngspice simulation)

Generic NMOS / PMOS SPICE models

Circuit Description

Two PMOS transistors connected in parallel to VDD (pull-up network)

Two NMOS transistors connected in series to GND (pull-down network)

Output taken at the common node between pull-up and pull-down networks

Simulation Setup
1. Power Supply

VDD = 5 V (DC voltage source)

2. Input Sources

Two independent PULSE voltage sources

Different delays were used to generate all four logic combinations:
00, 01, 10, 11

3. Circuit Implementation

CMOS NAND gate constructed using discrete PMOS and NMOS devices

Output optionally loaded with a simple RC network for observation

4. Simulation

Transient analysis used to observe time-domain behavior

Waveforms plotted to verify logical correctness

Results

Output goes LOW only when both inputs are HIGH

Output remains HIGH for all other input combinations

NAND truth table behavior verified through transient waveforms

A	B	Output
0	0	1
0	1	1
1	0	1
1	1	0
Issues Faced

SPICE netlist errors due to rescued symbols and incorrect model paths

Incorrect pulse timing caused only extreme logic states to appear

Resolutions

Replaced rescued symbols with proper SPICE-compatible symbols

Added correct simulation directives

Phase-shifted pulse input sources to generate all logic combinations

Limitations

Idealized transistor models

No PCB layout or parasitic extraction

No noise margin or delay analysis

Educational / learning-focused project

Learnings

CMOS logic operation at the transistor level

Importance of timing in transient simulations

KiCad + ngspice simulation workflow and common pitfalls

Author

Jay Bauti
