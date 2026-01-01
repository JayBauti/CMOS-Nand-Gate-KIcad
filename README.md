## CMOS NAND Gate Simulation using KiCad and ngspice

####Overview:
This project demonstrates the design and transient simulation of a CMOS NAND gate using discrete NMOS and PMOS transistors in KiCad 9.The goal was to understand CMOS logic operation at the device level and verify the NAND truth table using time-domain analysis.

---

####Objective:-
 -Design a CMOS NAND gate using PMOS pull-up and NMOS pull-down networks
 -Apply pulse inputs to generate all logic combinations
 -Verify NAND logic behavior through transient simulation

---

####Tools used:
 -KiCad 9(Schematic + Simulation)
 -Generic NMOS / PMOS SPICE models

---

####Circuit description:
 -Two PMOS transistors in parallel connected to VDD (pull-up network)
 -Two NMOS transistors in series connected to GND (pull-down network)
 -Output taken at the common node between pull-up and pull-down networks

---

####Steps during simulation setup

Supply
VDD = 5 V (DC source)

2) Input Source
Two independent PULSE voltage sources were used with different delays
 to generate all four input combinations (00, 01, 10, 11).

3) Making the Circuit 

4) Generating the Simulations from the working of the circuit.


####Results
- Output goes LOW only when both inputs are HIGH
- Output remains HIGH for all other input combinations
- NAND truth table behavior verified through transient waveform

| A | B | Output |
|---|---|--------|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |


####Issues faced
-SPICE netlist errors due to rescued symbols and incorrect model paths
-Incorrect pulse timing causing only extreme logic states

These were resolved by:
- Replacing rescued symbols with proper SPICE-compatible symbols
- Adding correct simulation directives
- Phase-shifting pulse input

---

####Limitations
- Idealized transistor models
- No layout or parasitic extraction
- No noise margin or delay analysis
- Educational / learning-focused project

---

####Learnings
- CMOS logic operation at transistor level
- Importance of timing in transient simulations
- KiCad simulation workflow and pitfalls

---

## Author
Jay Bauti
