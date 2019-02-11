# LC3-VM Extended

## Description
This code is an extension of the LC3 Virtual Machine as linked [here](https://justinmeiners.github.io/lc3-vm/). Modifications have been made to include a special zero register (such as the one specified in the RISC-V ISA) as well as usage of the OP_RES opcode to include a bitwise XOR option. 
Due to the implementation of TRAP opcodes, the code compatibility is currently limited to UNIX-related operating systems. 

## Notes
The virtual machine was written as an educational exercise to practice implementation of basic assembly code as well as to attain a basic grasp of virtual machines. The eventual goal is to build upon the concepts explored to build a virtual machine of the RV32E instruction set of the [RISC-V ISA](https://riscv.org/risc-v-isa/).