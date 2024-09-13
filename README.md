

This project implements a **computer architecture simulator** that emulates the key stages of a simple pipelined CPU architecture, including **instruction fetch, decode, execution, memory access,** and **write-back**. The simulator models the behavior of a CPU as it processes assembly-like instructions, handling control flow, memory access, and pipeline stages to simulate a real CPU’s instruction cycle.

### Key Features:
- **Instruction Fetching**: The simulator fetches instructions from memory sequentially, using the program counter (PC) to determine which instruction to process next.
- **Instruction Decoding**: Instructions are decoded into components such as opcodes, register operands, immediate values, and addresses. Bitmasking techniques are employed to extract the necessary fields.
- **Execution**: Arithmetic operations, logic operations, and control flow instructions (e.g., branching and jumping) are processed. The simulator supports operations like addition, subtraction, multiplication, shifting, and memory access.
- **Memory Access**: Memory operations are performed based on the instruction type. For instance, memory read/write operations (MOVR, MOVM) are simulated, allowing interaction between registers and memory.
- **Write-Back**: Results computed during the execution phase are written back into the register file, ensuring the processor state is correctly updated after each instruction is executed.
- **Pipelining**: The simulator models a pipelined architecture, where multiple instructions are processed in overlapping stages, improving throughput and reducing overall execution time.

### Project Flow:
1. **Global Initialization**: The simulator initializes key global variables like the program counter, register file, memory, and clock cycles.
2. **Fetch Stage**: The simulator fetches the next instruction from memory using the program counter.
3. **Decode Stage**: The fetched instruction is decoded into its constituent parts, including opcode, registers, and immediate values.
4. **Execution Stage**: The simulator executes the instruction, performing operations like arithmetic calculations, logical shifts, and control flow changes.
5. **Memory Access**: Instructions that involve memory read/write (MOVR, MOVM) are processed, interacting with the memory subsystem.
6. **Write-Back Stage**: Results of operations are written back into the register file, ensuring the correct state of the processor.
7. **Pipelining**: The simulator executes instructions in a pipelined manner, allowing instructions to flow through multiple stages concurrently.

### Output:
The output includes the final state of the register file, memory contents, and the total number of clock cycles taken to execute all instructions. The simulator calculates clock cycles based on the entry of instructions into the pipeline, demonstrating the efficiency gained through pipelining.

Collaborators: Youssef Elshamy, Diana Rehan, Nabila Shreif, Jana Saad, Shahd Abdelkhalek
