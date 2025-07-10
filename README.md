# Design and Implementation of a 4:1 Multiplexer Standard Cell

## Project Goal
This project focuses on expanding the open-source OSU standard cell library for the GlobalFoundries 180nm MCU (GF180MCU) process. The primary objective is to design, implement, and characterize a new 4:1 multiplexer standard cell. This new cell aims to provide an optimized, single-unit solution for 4-to-1 data selection tasks, improving upon implementations that would otherwise require discrete logic gates.

## Design Methodology
The design employs a hierarchical methodology, leveraging the existing `mux2_1` standard cell as a fundamental building block. The 4:1 MUX logic will be constructed by creating a structural schematic composed of three instances of the `mux2_1` cell. This approach ensures design reuse, consistency with the existing library, and accelerates the development and verification process.

## Directory Structure
* `designs/`: Main project workspace.
* `designs/libs/`: Contains custom cell libraries and external libraries (like the OSU cells). Our final MUX 4:1 cell will reside here.
* `designs/simulations/`: Contains all testbench schematics and simulation results. The test for our MUX 4:1 will be here.

## Tools Used
* **Xschem:** Schematic Capture
* **Magic / KLayout:** Physical Layout and Verification (DRC/LVS)
* **Ngspice:** Circuit Simulation
* **IIC-OSIC-TOOLS Docker Environment:** The containerized toolchain for the project.

## How to Simulate
The testbench for verifying the functionality of the 4:1 MUX can be found in the `designs/simulations/test_mux/` directory.

1.  Open the testbench schematic (`.sch` file) in Xschem.
2.  Click **Netlist**, then **Simulate**.
3.  The results will be displayed in the `gaw` (waveform viewer).

## Author(s)
* Nawiatsob

## License
This project is licensed under the MIT License.
