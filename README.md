# 16-Bit RISC Processor Design Project

A modern, cycle-accurate 16-bit RISC processor simulator developed in Python. The simulator features a comprehensive 5-stage pipeline architecture with automatic hazard detection, data forwarding, and a professional graphical user interface built with PySide6.

## Features

- **5-Stage Pipeline Architecture:** Instruction Fetch (IF), Instruction Decode (ID), Execute (EX), Memory Access (MEM), and Write Back (WB).
- **Hazard Management:** Automatic detection and handling of data hazards (load-use) and control hazards (branch/jump flushes).
- **Data Forwarding:** Implemented forwarding paths from EX/MEM and MEM/WB stages to minimize pipeline stalls.
- **Integrated Assembler:** Converts custom assembly language directly into 16-bit machine code with label support.
- **Graphical Interface:** Real-time visualization of pipeline stages, registers, instruction memory, and data memory using PySide6.

## Supported Instruction Set

The processor supports a custom 16-bit instruction set categorized into three types:

### R-Type Instructions
- `ADD rd, rs, rt` : Add registers
- `SUB rd, rs, rt` : Subtract registers
- `AND rd, rs, rt` : Bitwise AND
- `OR rd, rs, rt`  : Bitwise OR
- `SLT rd, rs, rt` : Set on Less Than (signed)
- `SLL rd, rt, shamt`: Shift Left Logical
- `SRL rd, rt, shamt`: Shift Right Logical

### I-Type Instructions
- `ADDI rt, rs, imm` : Add Immediate
- `LW rt, offset(rs)`: Load Word
- `SW rt, offset(rs)`: Store Word
- `BEQ rs, rt, label`: Branch on Equal
- `BNE rs, rt, label`: Branch on Not Equal

### J-Type Instructions
- `J label`   : Jump
- `JAL label` : Jump and Link
- `JR rs`     : Jump Register
- `NOP`       : No Operation

## Installation

To run the simulator, you need Python and PySide6 installed on your system.

1. Clone the repository:
   ```bash
   git clone https://github.com/omer-torus/16-BIT-RISC-PROCESSOR-DESIGN-PROJECT.git
   cd 16-BIT-RISC-PROCESSOR-DESIGN-PROJECT
   
2. Install the required dependency:
pip install PySide6

3.Run the simulator: 
python modern_simulator.py

Usage
1. Launch the application.
2. Enter your custom Assembly code into the text editor on the left side of the interface.
3. Click "Assemble" to compile your code into machine instructions.
4. Use the "Step" button to execute the program cycle-by-cycle and observe the 5 pipeline stages (IF, ID, EX, MEM, WB). Alternatively, use "Run" for continuous execution.
5. Monitor processor efficiency, pipeline stalls, and data hazards using the "Hazard Log" and "Forwarding Log" tabs on the interface.


Screenshots
1. <img width="2559" height="1332" alt="image" src="https://github.com/user-attachments/assets/a4bf7351-bd06-4666-9fa3-71212e41c107" />
2. <img width="2559" height="1338" alt="image" src="https://github.com/user-attachments/assets/11ffcc59-5562-46c0-ae81-649626a58a9e" />

