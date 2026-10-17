# My-Testboard

This repository contains the design files for a custom hardware development and test board built using KiCad for the Hack Club hardware track. The circuit is designed around a standard LM555 testboard.

<img width="489" height="410" alt="TESTBOARD CAD" src="https://github.com/user-attachments/assets/09ea1cf6-1259-4e7b-b2ae-bd08b5c43267" />
<img width="320" height="201" alt="TESTBOARD SCHEMATIC" src="https://github.com/user-attachments/assets/18cb0935-e3fe-47ce-89bb-a00024fb8471" />
<img width="569" height="512" alt="TESTBOARD PCB" src="https://github.com/user-attachments/assets/04328c56-fa90-4f9c-99ff-6fef196486cc" />

# Project Structure
* /CAD - Contains the 3D STEP file (TestBoard.step) of the populated PCB layout and the native project files.
* /GERBERS - Contains the production zip file (Gerbers.zip) required for manufacturing fabrication.
* TestBoard.csv - Bill of Materials (BOM) listing the complete component inventory and sourcing data.
* TestBoard-pos.csv - Component Placement List (CPL) detailing structural coordinate data for assembly alignment.
* TestBoard.pdf - Schematic drawing printout.

# Mechanical and Hardware Design
This project is a bare hardware development and test board. It focuses strictly on circuit traces and signal routing, and it does not feature a physical 3D-printed case, enclosure, or mechanical stand. 

The STEP file provided inside the /CAD folder represents the complete 3D spatial layout of the PCB alongside its mounted components. This file serves as the complete, self-contained physical project assembly to satisfy the 3D modeling submission rule.

# Component Sourcing and Assembly Plan
The circuit utilizes a through-hole design layout. Assembly is split between factory placement and manual desktop soldering:

* Integrated Circuit (U1): LM555CN  chip in a DIP-8 package.
* Potentiometer (RV1): 10K vertical rotary trimmer potentiometer (3386P package). This part is sourced via external vendor channels and will be hand-soldered locally.
* Passive Components (R1-R3, C1-C3, D1): 1K Ohm 1/4W axial resistors, ceramic disc capacitors (10nF and 100nF values), a radial electrolytic capacitor (47uF value), and a 3mm blue indicator LED. These parts are sourced via bulk electronic assortment kits and will be hand-soldered locally.
* Power Interface (J1): 2-pin horizontal screw terminal block featuring 3.5mm pad pitch spacing. This part is sourced via external vendor channels and will be hand-soldered locally.

# Manufacturing Fabrication
The bare boards will be manufactured using standard FR4 fiberglass substrate through JLCPCB using the production zip file in the gerbers directory. Remaining components will be manually populated, soldered, and verified on a test bench post-delivery.
