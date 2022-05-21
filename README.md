# Pipelined-MIPS-Processor-Implementation
a simple 16-bit MIPS-like processor with seven 16-bit general-purpose registers: R1 through R7. R0 is hardwired to zero and cannot be written. There is also one special-purpose 12-bit register, which is the program counter (PC). All instructions are 16 bits
The program will be loaded and will start at address 0 in the instruction memory. The data segment will be loaded and will start also at address 0 in the data memory the last instruction in the program can jump or branch to itself indefinitely (because there is no underlying operating system to terminate the program).
To verify the correctness of the design we show the values of all registers (R1 to R7) at the top-level of the design
we start by building phase 1: single-cycle processor
the datapath and control of a single-cycle processor and ensure its correctness
Phase 2: Building Pipeline processor
Design the control logic to detect data dependencies among instructions and implement the forwarding logic, handle properly the control hazards of the branch and jump instructions. Also, stall the pipeline after a LW instruction, if it is followed by a dependent instruction.
Testing and verification
To demonstrate that  CPU is working:
we  test all components and sub-circuits independently to ensure their correctness. For example, test the correctness of the ALU, the register file, the control logic separately, before putting our components together.
 Test each instruction independently to ensure its correct execution.
 Write a sequence of instructions to verify the correctness of ALL instructions : the correctness of all ALU R-type and I-type instructions, LW and SW instructions,  all branch and jump instructions.
 Testing in phase_2: Test sequences of dependent instructions to ensure the correctness of the forwarding logic. Also, test a LW (load word) followed by a dependent instruction to ensure stalling the pipeline correctly by one clock cycle.
 Test the behavior of taken and untaken branch instructions and their effect on stalling the pipeline.
 Translate test programs into machine instructions. Load the instructions into the instruction memory starting at address 0 ( we've special work in this since each instruction will be converted to machine code and send to processor circuit to be executed. Moreover we need to translate the binary code representing the instruction to hexadecimal code due to simulate it using logisim that required the data to be loaded in hexadecimal format.
Our team developed a compiler to do this job in order to simplify our work.
The way of using our compiler is so simple, you just write your code and then click assemble and it will translate it into hexadecimal code and save the file
