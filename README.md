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

# Simplified RTL to GDSII Flow
![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-23%20214049.png?raw=true)

### Overview of the Design Flow
This flow demonstrates the step-by-step process of converting an RTL design into a GDSII file for fabrication. Each stage plays a crucial role in ensuring the design meets its functional, timing, and physical requirements.

## Flow Stages

1. **Synthesis**  
   Converts the RTL (Register Transfer Level) description into a gate-level netlist, optimizing for area, speed, and power.

2. **Floor/Power Planning**  
   Defines the layout structure of the chip, including regions for different modules and a power distribution network.

3. **Placement**  
   Places standard cells from the synthesized netlist into the defined floorplan.

4. **Clock Tree Synthesis (CTS)**  
   Builds a balanced clock tree to minimize clock skew and ensure proper timing across the design.

5. **Routing**  
   Connects all placed cells based on the netlist using metal layers while adhering to design rules.

6. **Sign-Off**  
   Final stage, where the design is validated against specifications, including checks for timing, DRC (Design Rule Check), and LVS (Layout Versus Schematic).


### Tools for Each Stage

- **Synthesis**: Yosys  
- **Floor/Power Planning & Placement**: OpenROAD/OpenLANE  
- **CTS**: TritonCTS (part of OpenROAD)  
- **Routing**: FastRoute, detailed routing with OpenROAD  
- **Sign-Off**: Magic (DRC & LVS)

## OpenLane ASIC Flow

OpenLane is an open-source ASIC design flow built to generate GDSII layout files from RTL code with minimal human intervention. It integrates multiple open-source tools to provide a complete RTL-to-GDSII flow, ensuring seamless digital design automation.

### Objectives
- Provide a fully automated, open-source RTL-to-GDSII flow.
- Ensure a reproducible and customizable flow for ASIC design.
- Leverage open-source tools to enable silicon design accessibility.

### Inputs and Outputs
- **Inputs:** RTL files, SDC file, and PDK files.
- **Outputs:** GDSII/LEF file.

### OpenLane Flow Overview

Below is a summarized OpenLane flow representation:

![image alt](https://github.com/Vansh0917/nasscom-vsd-soc-design-program/blob/main/Screenshot%202025-01-24%20195352.png?raw=true)

### Tools Used in OpenLane

| Stage | Tool(s) Used |
|--------|-------------|
| **RTL Synthesis, Technology Mapping, and Formal Verification** | Yosys + ABC |
| **Static Timing Analysis** | OpenSTA |
| **Floor Planning** | init_fp, ioPlacer, pdn, tapcell |
| **Placement** | RePLace (Global), OpenDP (Detailed) |
| **Clock Tree Synthesis** | TritonCTS |
| **Fill Insertion** | OpenDP/filler_placement |
| **Routing** | FastRoute (Global), TritonRoute (Detailed) |
| **SPEF Extraction** | OpenRCX |
| **GDSII Streaming** | Magic, KLayout |
| **DRC Checks** | Magic, KLayout |
| **LVS Check** | Netgen |
| **Antenna Checks** | Magic |
| **Circuit Validity Check** | CVC |

### Logic Synthesis and Optimization
- **Yosys** converts the HDL to a gate-level netlist using generic components.
- **ABC** maps generic components to the standard cell library of the PDK.
- **Synthesis Exploration** allows different synthesis strategies optimizing for either area or timing.

### Logic Equivalency Checking (LEC)
- Compares the gate-level netlist from synthesis with the optimized netlist after place and route.

### Antenna Rules Violation
- **Problem:** Long wire segments act as antennas, accumulating charge and potentially damaging transistor gates.
- **Solutions:**
  - **Bridging** techniques to reduce charge accumulation.
  - **Antenna diode insertion** to safely leak away excess charge.


### Tasks:-

- Run 'picorv32a' design synthesis using OpenLANE flow and generate necessary outputs.
- Calculate the flop ratio.

#### 📂 Change Directory to OpenLANE Flow Directory
![Screenshot 2025-01-25 120324](https://github.com/user-attachments/assets/233211c6-d6be-44f6-a213-3190c5f19b9a)

```sh
cd Desktop/work/tools/openlane_working_dir/openlane
cd Desktop/
cd work/
cd tools/
cd openlane_working_dir/
cd openlane/
```

## PDKs Folder Structure

The `pdks` directory contains various libraries and configurations for Sky130A.

### `libs.ref` and `libs.tech` Directories

These directories contain reference libraries and EDA tool-specific configurations:

```
cd ~/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.ref/sky130_fd_sc_hd
ls -ltr
```

![Screenshot 2025-01-25 122853](https://github.com/user-attachments/assets/b2f3bbd3-a5ee-4716-897a-fc4aaee5e3aa)

```
cd ~/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech
ls -ltr
```

![Screenshot 2025-01-25 122548](https://github.com/user-attachments/assets/3915dbd8-95cd-4f1d-b476-f43053ba8b57)

### Run 'picorv32a' design synthesis using OpenLANE flow and generate necessary outputs

```markdown 
## OpenLANE Interactive Mode Setup

Follow these steps to run OpenLANE in interactive mode within the Docker container.

Steps: 
```
1. **Run the Docker container**:
   Since the long command has been aliased to `docker`, invoke the OpenLANE flow Docker sub-system with:

   ```bash
   docker
   ```

2. **Check the current directory**:
   Navigate to the directory where OpenLANE is located. Use the following command to check your current directory:

   ```bash
   pwd
   ```
![Screenshot 2025-01-25 123859](https://github.com/user-attachments/assets/05ae20ba-b5cf-4c34-b384-d6c6e559806c)

3. **Launch OpenLANE in interactive mode**:
   To enter interactive mode, use the following command:

   ```bash
   ./flow.tcl -interactive
   ```
![Screenshot 2025-01-25 123910](https://github.com/user-attachments/assets/fe974d85-34e6-4593-9412-ff368124bd16)
   
 now running OpenLANE in interactive mode within the Docker container.


### Setting Up OpenLANE for `picorv32a`


### 1. Load OpenLANE Package  
Ensure OpenLANE is initialized with the required package:
```
package require openlane 0.9
```
![Screenshot 2025-02-01 001445](https://github.com/user-attachments/assets/67452185-ab81-4fc5-a169-cc6ebca14553)

### 2. Prepare the Design  
Set up the necessary files and directories for the `picorv32a` design:

```
prep -design picorv32a
```
This command initializes the workspace, making it ready for the OpenLANE flow.
![Screenshot 2025-01-25 133208](https://github.com/user-attachments/assets/a530ff6d-222b-40d7-aff8-ed70a82c21e2)
![Screenshot 2025-01-25 133156](https://github.com/user-attachments/assets/d7c98f02-ec6d-4b1b-963a-cfa3a33bf55f)

### In OpenLane, synthesis is executed using the `run_synthesis` command. This process consists of the following key steps:

**Logic Synthesis**
- Transforms RTL code (Verilog) into a gate-level netlist.
- Optimizes logic for area and performance.

**Static Timing Analysis (STA)**
- Verifies timing constraints and propagation delays.
- Ensures the design meets clocking requirements.

By performing these steps, OpenLane helps in achieving an optimized balance between **performance,area  and power efficiency**. 

*Screenshot is attached below.*

![Screenshot 2025-01-25 151244](https://github.com/user-attachments/assets/a14bf392-c738-4b04-a80b-7c94d3dc6f6f)

### --Flop Ratio and DFF Percentage Calculation
 It is the ratio of total number of D flip-flops to the total number of cells in a design.
 
![Screenshot 2025-02-01 001819](https://github.com/user-attachments/assets/ed051b0e-b6be-42b8-9e47-9e2d5a93b4c6)
![Screenshot 2025-02-01 001754](https://github.com/user-attachments/assets/b11bfb53-853d-4e7a-80a4-73ab95361528)

**Flop Ratio Calculation:**

Total number of D flip-flop in the design = 1613

Total number of cells in the design = 14876

Flop Ratio = 1613 / 14876 = **0.1084**

**DFF Percentage Calculation:**

Percentage of DFFs = 0.1084 × 100  = **10.84%**
# Section 2 - Good floorplan vs bad floorplan and introduction to library cells 
### Floor Planning Process

After synthesis, we initiate floor planning using:

`run_floorplan`
![Screenshot 2025-02-01 002158](https://github.com/user-attachments/assets/406b40f3-e0a9-4e28-8a2f-16ecb5bd8555)

![Screenshot 2025-02-01 001954](https://github.com/user-attachments/assets/7619fa48-60cb-4586-8b03-51af557e2a1a)

### Calculate the die area in microns from the values in floorplan def
**Viewing the Floorplan Definition**
To check the contents of the floorplan definition file, i have  used:

```sh
cd /Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/31-01_18-44/results/floorplan/
```
![Screenshot 2025-02-01 002609](https://github.com/user-attachments/assets/d7672718-5804-4263-a4ce-3d4da66b60ea)

### Given Data:
 **1000 Unit Distance:** 1 Micron
 
 **Die Width in Unit Distance:** `660685 - 0 = 660685`
 
 **Die Height in Unit Distance:** `671405 - 0 = 671405`
> ## Die Area Calculation in Microns
>
> ** Conversion to Microns:**
> - **Die Width:** 660685 ÷ 1000 = `660.685 µm`
> - **Die Height:** 671405 ÷ 1000 = `671.405 µm`
>
> **Total Die Area:** **443,587.21 µm²**
### Visualizing the floor plan using Magic:
```
# Change directory to path containing generated floorplan DEF
cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/17-03_12-06/results/floorplan/

# Command to load the floorplan DEF in Magic tool
magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```
![Screenshot 2025-02-01 003311](https://github.com/user-attachments/assets/d64b89dc-8e3d-4327-8ab1-f3cc33215df3)
**Zoomed View of the Die**

To zoom into a specific section of the die, follow these steps:

1. Move the cursor over the section you want to zoom in on.
2. Press the `s` key on your keyboard to select the section.
3. Press `z` to zoom in.
4. Press `Shift + Z` to zoom out if needed.

**Equidistant Placement of Ports**
![Screenshot 2025-02-01 004043](https://github.com/user-attachments/assets/bb7acb40-84d9-4821-98b4-5cea1c5017c4)
 ports are placed at equal distances in the floorplan.


**Run the following command to start the placement:**

   ```
   run_placement
   ```
![Screenshot 2025-02-02 204438](https://github.com/user-attachments/assets/e97fc64c-afec-4cfc-9072-222b51206a96)
![Screenshot 2025-02-02 204459](https://github.com/user-attachments/assets/80d47dc2-cf17-4508-a8e3-060e1822d4e2)
  placement results are  generated in result  files

**# Command** For Importing Placement DEF into Magic Tool:
```
  magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.placement.def & 
```
![Screenshot 2025-02-01 004538](https://github.com/user-attachments/assets/0c7c4543-4e60-4004-86bc-ea86b8aeb1da)

`**Standard** cells are arranged within standard cell rows`

![Screenshot 2025-02-01 004722](https://github.com/user-attachments/assets/395d1396-3805-452a-8d4e-09ac6c1e1cc1)

# Section 3 - Design library cell using Magic Layout and ngspice characterization

### Cloning and Setting Up Custom Inverter Standard Cell Design in OpenLane

This guide will walk you through the process of cloning the `vsdstdcelldesign` repository and setting up Magic technology files in the OpenLane directory.

> ### Steps to Clone the Repository and Setup Magic Tech Files

```
# 1. Navigate to OpenLane
cd Desktop/work/tools/openlane_working_dir/openlane

# 2. Clone repository
git clone https://github.com/nickson-jose/vsdstdcelldesign

# 3. Verify cloning
ls -ltr

# 4. Navigate to tech file location
cd /Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic

# 5. Copy tech file
cp sky130A.tech /Home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign

```
![Screenshot 2025-02-02 191723](https://github.com/user-attachments/assets/446ad8cd-639f-489c-bdf3-9e364ae014a8)

![Screenshot 2025-02-02 202136](https://github.com/user-attachments/assets/9e5130ec-2e14-4738-8e10-913dddc7b051)


 **Command to open custom inverter layout in magic**
 
`magic -T sky130A.tech sky130_inv.mag &`

![Screenshot 2025-02-02 202834](https://github.com/user-attachments/assets/8363297f-d3db-4aca-b573-9fbd1976ac0d)
### Verifying the different layers & connection of the inverter:
To know about a layer, place your cursor on it and press `s` from your keyboard, which will select the layer/cell, now type `what` in `tkcon` window of magic, it will give the name of the layer

Input A (polycont) is Identified 

![Screenshot 2025-02-02 203721](https://github.com/user-attachments/assets/8c081b57-cd62-463c-a61e-0b2e41169398)

Output Y connectivity to PMOS and NMOS drain verified

![Screenshot 2025-02-02 205545](https://github.com/user-attachments/assets/037d2242-444b-4ede-a9ab-f78ce0ee954e)

### Fixing DRC Errors in Magic VLSI

 **Finding & Fixing Errors** 

`drc find    # Find next error`

`drc why     # Highlight errors`

`drc count   # Count total errors`

`drc clear   # Clear DRC highlights`

`drc check   # Re-run DRC check`

```
##Check tkcon for error details
## Adjust layout (spacing, width, overlaps) as needed
## Run drc check until no errors remain
```
**DRC Error is being highlighted in below screnshots**
![Screenshot 2025-02-02 210019](https://github.com/user-attachments/assets/93adabb6-66ae-46bf-a46f-e2b5a6b97268)
![Screenshot 2025-02-02 210214](https://github.com/user-attachments/assets/5be3b577-084e-4c80-a6a1-502b0322ad0a)

## SPICE Extraction of Inverter

**Checking Current Directory**

*Before extracting, check which directory your `tkcon` window is opened in:*
```tcl
pwd
```

**Extracting Layout**

*Run the following command in the `tkcon` window to extract all necessary files:*
```tcl
extract all
```
![Screenshot 2025-02-02 210808](https://github.com/user-attachments/assets/26e325df-8d87-4d3c-8926-982af729635f)

This will generate a `.ext` file in the same directory.

 **Verifying Extraction**
 
*Check if the `.ext` file has been created:*
```sh
ls *.ext
```

**Generating SPICE File**

*Run the following commands to convert the extracted file into a SPICE netlist:*
```tcl
ext2spice cthresh 0 rthresh 0
ext2spice
```
![Screenshot 2025-02-02 211205](https://github.com/user-attachments/assets/8d174683-ea6f-40ae-8e2c-9b02d9ec93b0)

![Screenshot 2025-02-02 211236](https://github.com/user-attachments/assets/1348efd6-32a7-4790-8a63-ed4b7528c9a9)


**Viewing the SPICE File**

*Use the following command to open the generated SPICE file:*
```
less sky130_inv.spice
```
![Screenshot 2025-02-02 211716](https://github.com/user-attachments/assets/6e7b3fbe-3475-4505-aec3-9f67db33fe33)


 **Measuring Grid Box Size in Magic**
 
*To measure the unit grid box size in Magic, select a grid box and run:*
```tckon
box
```
This will output the size of the selected grid box.

![Screenshot 2025-02-02 213357](https://github.com/user-attachments/assets/8db0b914-d436-4a15-8f4d-f11c9891eee7)

**Editing the SPICE File**

Edit the `.spice` file in a text editor as needed
by commnad `gedit sky130_inv.spice`

**Installing NGSPICE**

Install the `ngspice` simulator using:
```
sudo apt install ngspice
**Note:** The password is `vsdiat` .
```
![image](https://github.com/user-attachments/assets/cb225df5-820a-44a6-a575-fce19eee4530)

![Screenshot 2025-02-03 115235](https://github.com/user-attachments/assets/48729089-cf57-4c8d-8ef8-995406828d97)

 **Running the SPICE Simulation**
 
To simulate the inverter:
```s
ngspice sky130_inv.spice
```
![Screenshot 2025-02-03 172628](https://github.com/user-attachments/assets/82832048-b813-4bbc-b77b-fd9efe1bfafc)

 **Plotting Output**
 
To plot the output waveform:
```
plot y vs time a
```
This will generate the output waveform based on the simulation results.

![Screenshot 2025-02-03 172641](https://github.com/user-attachments/assets/58e32eaf-b00b-4394-bbf6-983f043b2305)

 **TASK -**
 
        *Characterization of the plot::*

# Day 4: Pre-Layout Timing Analysis and the Importance of a Good Clock Tree

This document provides the complete set of commands and instructions for Day 4 of the Digital VLSI SoC Design and Planning Workshop. It covers:

1. **Integration of a Customized Inverter Cell Design**
2. **Timing Analysis Using Ideal Clocks with OpenSTA**
3. **Clock Tree Synthesis (CTS) Using TritonCTS**

---

## 1. Integration of Customized Inverter Cell Design

### A. Verify Layout Conditions in Magic

- **Condition 1:** Ports must be placed at intersections of vertical and horizontal tracks.  
- **Condition 2:** The width and height of the Place & Route (P&R) region must be multiples of the grid cell dimensions.

#### Steps:

1. **Change Directory and Open Layout in Magic:**

   ```bash
   # Change directory to the custom cell design folder
   cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign

   # Open the custom inverter layout with
    Magic -T sky130A.tech sky130_inv.mag &
```
