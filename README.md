# nasscom-vsd-soc-design-program
<details>
<summary>INTRODUCTION THEORY </summary>
  
 # Digital VLSI SoC/Physical Design Overview
  
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
</details>
