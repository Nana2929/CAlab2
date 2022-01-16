
## RISC-V CPU 
### NTU CSIE Computer Architecture Lab 2
* Features: 
  * off-chip data memory + 2-way associative cache
    * Size: 16 KB 
    * LRU Replacement policy 
    * Cache Line size: 32 bytes 
    * RW Alignment: Align to 8 bytes 
    * Write Hit/Miss Policy: Write back, Write allocate
    * bit-length: tag = 23, idx = 4, offset = 5 
  * in-chip instruction memory 
  * pipelined (5 stages)
* supported instructions: 
  AND, XOR, SLL, ADD, SUB, MUL, ADDI, SRAI, LW, SW, BEQ
* Env: MacOS, Vscode, iverilog 
* Additional specs: 
    * 32-bit instruction
    * support Forwarding, Hazard Detection
    * 10-cycle memory latency 
* Compile (using lab2 testbench, namely testbench.v)
    * cd codes
    * iverilog -o ./CPU/testbench.vvp ./CPU/testbench.v
    * vvp ./CPU/testbench.vvp
    * outputs: output_{}.txt, cache_{}.txt for register/dmem states and cache history repectively. 
    
    
![alt text](https://github.com/Nana2929/CAlab2/blob/master/cpu_fig.png)
