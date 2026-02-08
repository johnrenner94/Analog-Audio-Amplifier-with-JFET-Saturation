# Analog Audio Preamp with JFET Saturation

This repository contains the design and documentation for a small-signal analog audio preamp intended for guitar or line-level use. The circuit combines op-amp gain stages with a discrete JFET stage operated into soft saturation, followed by an active Baxandall tone control and output conditioning.

The project is documented as an engineering design exercise, with emphasis on signal flow, gain staging, biasing, and distortion behavior rather than enclosure or manufacturing details.

---

## Project Status

**Work in progress**

The design is functionally complete at the **schematic and preliminary simulation level**.

LTspice simulations have been used to evaluate:
- DC operating points  
- Gain structure and headroom  
- Frequency response and tone control range  
- Distortion behavior under nominal and driven conditions  

Hardware prototyping and bench measurements are planned but not yet finalized.

---

## Overview

The signal path is organized as follows:

1. **Input Gain Stage**  
   Adjustable clean gain used to establish the nominal internal signal level.

2. **JFET Saturation Stage**  
   A single-ended JFET stage biased for soft, asymmetrical clipping when driven, favoring even-order harmonic content.

3. **Buffering and Tone Control**  
   An active Baxandall bass/treble EQ buffered on both sides to prevent loading interactions and maintain predictable control behavior.

4. **Output Stage**  
   Final gain and output level control providing low output impedance for downstream equipment.

Design choices were informed by standard small-signal audio practice, with reference to *The Art of Electronics* and *Small Signal Audio Design*.

---

## Repository Contents

- **report/**  
  Design report (PDF) describing theory of operation, design rationale, and simulation results.

- **schematic/**  
  Current schematic of the full circuit (PDF).

- **simulation/**  
  LTspice schematics used for AC, transient, and distortion analysis.

- **ltspice_components/**  
  Custom LTspice potentiometer symbol and component files used in the schematic and simulations.

- **README.md**  
  Project overview and status.

---

## Tools Used

- LTspice for circuit simulation  
- PDF documentation for design narrative and results  

---

## Future Work

- Breadboard prototyping and bench validation  
- THD / THD+N measurements under controlled drive conditions  
- Minor component value refinement based on measured results  
- PCB layout and physical implementation  

---

## Notes

This project is intended as a documented analog design study and portfolio piece.  
It is not presented as a finished commercial product.
