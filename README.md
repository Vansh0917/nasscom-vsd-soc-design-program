# nasscom-vsd-soc-design-program
<details>
<summary>INTRODUCTION THEORY </summary>
  
 # Digital VLSI SoC/Physical Design Overview
   ![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20181617.png?raw=true)
  
   Key Steps in the Design Flow:

1. **RTL Architect**: Defines high-level architecture and specifications.
2. **Soft Copy of the Hardware**: Creates RTL (Verilog/VHDL) representation.
3. **SoC Design Flow**:
   - Processor
   - Peripherals/IPs 
   - Gate Level Netlist (synth P1)
   - Macros (synth RTL)
   - Analog IPs (func RTL)
   - SoC Integration
4. **ASIC Design Synthesis**: Translates RTL to gate-level netlist, optimizes.
5. **Floorplanning, Placement, CTS, Routing**: Defines chip layout, optimizes physical implementation.
6. **DRC/LVS Checks**: Design Rule Checks, Layout Versus Schematic verification.
7. **Testbench in C/C++**: Verifies design functionality.
8. **RTL2GDS**: Generates final GDSII layout.
The overall flow transforms RTL specifications into a physically implemented SoC design.
## VLSI Concepts Overview
![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20183852.png?raw=true)

 Overview of key VLSI concepts related to board diagrams, focusing on essential components and their functions in integrated circuit design.

 ## Package (QFN 48)
- **QFN**: Quad Flat No-lead package, a surface-mount IC package.
- **Pin Count**: The "48" indicates the package has 48 pins/leads.
- **Design Features**: QFN packages have flat, exposed metal pads on the bottom, allowing for a compact design and improved thermal performance.
![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20185133.png?raw=true)
## Wire Bonds
- **Functionality**: Thin metallic wires that electrically connect the die (chip) to the package pads.
- **Importance**: They establish signal and power connections between the integrated circuit and the package.
![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20185220.png?raw=true)
## Pads
- **Role**: Metal contact points on the die that connect with wire bonds.
- **Purpose**: Facilitate electrical routing and interconnections among various components on the chip.
## Core and Die
- **Core**: The central processing unit (CPU) of the chip where primary logic and functionality reside.
- **Die**: The physical semiconductor material that houses the core, transistors, and other necessary circuitry.
![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20185234.png?raw=true)
## Foundry IPs and Macros
- **Foundry IPs**: Pre-designed circuit blocks provided by semiconductor foundries, verified for functionality.
- **Macros**: Larger, complex IP blocks that can be reused across multiple chip designs, enhancing design efficiency.

## SDRAM Chip
- **Definition**: Synchronous Dynamic Random Access Memory (SDRAM), a type of volatile memory used in systems.
- **Functionality**: Provides high-speed, temporary data storage necessary for processors or System-on-Chip (SoC) architectures.
![image alt]()
## Board Diagram Interconnections
In a typical board diagram for an SoC design:
- The processor/SoC interfaces with multiple peripherals.
- Memory components like SDRAM are connected for data storage.
- External interfaces such as I2C, OSPI, UART, and GPIO allow communication with other devices.
- The JTAG-UART block is crucial for programming and debugging purposes.




</details>
