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
![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20185257.png?raw=true)

**In a typical board diagram for an SoC design:**
- The processor/SoC interfaces with multiple peripherals.
- Memory components like SDRAM are connected for data storage.
- External interfaces such as I2C, OSPI, UART, and GPIO allow communication with other devices.
- The JTAG-UART block is crucial for programming and debugging purposes.

 ![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20192215.png?raw=true )
## Key Concepts
* **Compiler input:** The source code written in a high-level programming language (e.g., C)
* **Compiler output:** Assembly language instructions
* **Assembler output:** Machine code (binary instructions)
* **RISC-V assembly language program:** A program written in a low-level language for the RISC-V architecture.
* **Chip layout:** Shows the layout of components on a computer chip.
## Overall Process
* Compiling C code into assembly language.
* Assembling assembly code into machine code.
* Loading and executing the machine code on the hardware.
* System software helps in managing and controlling the execution of the program. 

</details>

# Section 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK
## Open Source Digital ASIC Design

## What is an ASIC?

An **Application-Specific Integrated Circuit (ASIC)** is a type of integrated circuit customized for a particular use rather than being designed for general-purpose use. ASICs are widely used in industries such as communications, automotive, healthcare, and consumer electronics to provide optimized performance and power efficiency for specific applications.

---

## Open Source Digital ASIC Design
![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20214026.png?raw=true)
Open-source digital ASIC design is an innovative field that leverages community-driven tools and resources to design and fabricate ASICs at lower costs. This ecosystem fosters innovation, collaboration, and learning by providing access to open-source tools, reusable designs, and publicly available process design kits (PDKs).

### Key Components of Open-Source ASIC Design

1. **EDA Tools (Electronic Design Automation)**:  
   EDA tools are software solutions that automate the design process for ASICs. Examples include:  
   - **Qflow**: A lightweight toolchain for digital synthesis, placement, and routing, ideal for small-to-medium-scale designs.  
   - **OpenROAD**: Provides a fully automated end-to-end open-source ASIC design flow, reducing the complexity of digital design.  
   - **OpenLANE**: A comprehensive ASIC design framework that integrates tools like Yosys (for logic synthesis) and Magic (for layout editing) into a single flow.

2. **RTL Designs**:  
   RTL (Register Transfer Level) designs describe the functional behavior of digital systems using hardware description languages like Verilog or VHDL. Open-source platforms provide ready-to-use modules, such as:
   - **Processor Cores**: Example RTL designs include RISC-V cores, such as PicoRV32, which is a lightweight RISC-V processor for embedded applications.  
   - **Communication Protocols**: OpenCores offers designs for UART, SPI, and I2C controllers that can be integrated into custom ASIC projects.

3. **PDK Data (Process Design Kits)**:  
   The **Process Design Kit (PDK)** contains essential files required to translate RTL designs into physical silicon layouts.  
   - **SkyWater 130nm PDK**: Provides an open-source 130nm process node, enabling experimentation with real-world silicon manufacturing. The PDK includes device libraries, layout rules, and SPICE models for circuit simulations.

---

## Benefits of Open-Source ASIC Design

- **Accessibility**: Provides entry-level access for students, researchers, and startups to experiment with ASIC design.
- **Collaboration**: Enables a community-driven approach to solving complex problems.
- **Cost Efficiency**: Reduces barriers to silicon prototyping by utilizing open-source resources and foundry partnerships.

---

