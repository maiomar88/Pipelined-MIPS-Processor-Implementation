# Pipelined-MIPS-Processor-Implementation
a simple 16-bit MIPS-like processor with seven 16-bit general-purpose registers: R1 through R7. R0 is hardwired to zero and cannot be written. There is also one special-purpose 12-bit register, which is the program counter (PC). All instructions are 16 bits
The program will be loaded and will start at address 0 in the instruction memory. The data segment will be loaded and will start also at address 0 in the data memory the last instruction in the program can jump or branch to itself indefinitely (because there is no underlying operating system to terminate the program).
To verify the correctness of the design we show the values of all registers (R1 to R7) at the top-level of the design
Phase 2: Building Pipeline processor
Design the control logic to detect data dependencies among instructions and implement the forwarding logic, handle properly the control hazards of the branch and jump instructions. Also, stall the pipeline after a LW instruction, if it is followed by a dependent instruction.
