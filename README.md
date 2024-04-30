# VSDSquadronmini internship
# Task-1
## RISCV GNU Toolchain
To install use following command    
git clone https://github.com/riscv/riscv-gnu-toolchain  
![image](https://github.com/Sivasrikiran2004/VSDSquadronmini/assets/162977948/32043ca8-8684-43c3-a887-da0744c889b2)
## Yosys tool 
To install yosys use following commands   
git clone https://github.com/YosysHQ/yosys.git  
cd yosys  
sudo apt install  
make (if make is not installed please install it)  
sudo apt get install build essential  
![yosys](https://github.com/Sivasrikiran2004/VSDSquadronmini/assets/162977948/6c79419c-441f-4a5b-8924-7116404999c4)
## iverilog
To install iverilog use following commands    
sudo apt get install iverilog  
![iverilog 1](https://github.com/Sivasrikiran2004/VSDSquadronmini/assets/162977948/d32cfa94-7b72-4635-b6c3-5a718222b962)  
## Gtkwave
To install gtkwave use following commands  
sudo apt update  
sudo apt install gtkwave  
![gtkwave](https://github.com/Sivasrikiran2004/VSDSquadronmini/assets/162977948/88831ff2-a15f-4fd4-914b-dd0ba61fd6c1)  

## Task-2  
R-type instruction
<pre>
  These are used for operations involving only registers without immediate values.  
  Typically include arithmetic,logical and comparison instructions. 
</pre>
Format of R-type instruction
<pre>
    31      25 24    20 19    15 14    12 11     7 6        0  
    |  funct7 |  rs2   |  rs1   | funct3 |   rd   |  opcode | 
</pre>
<pre>
- opcode: It is a part of instruction which specifies the operation to be performed.  
          It is of 7 bits [6:0]
- rd: It is the destination register which stores the destination address.  
          It is of 5 bits [11:7]  
- funct3: It specifies the function code for the operation.  
          It is of 3 bits [12:14]  
- rs1: It specifies the source register 1.  
          It is of 5 bits [19:15]  
- rs2: It specifies the source register 2.  
          It is of 5 bits [19:15]  
- funct7: It specifies the function for the operation.  
          It is of 7 bits [31:25]  
</pre>
  
I-type instruction  
<pre>
  These are used for operations involving immediate values along with registers.  
  Typically include arithmetic,logical and data transfer operations.  
</pre>
Format of I-type instruction
<pre>
    31      20 19    15 14    12 11     7 6       0
    |   imm   |  rs1   |  funct3|   rd   | opcode |
</pre>
<pre>
- opcode: It is a part of instruction which specifies the operation to be performed.  
          It is of 7 bits [6:0]
- rd: It is the destination register which stores the destination address.  
          It is of 5 bits [11:7]
- funct3: It specifies the function code for the operation.  
          It is of 3 bits [12:14]
- rs1: It specifies the source register 1.  
          It is of 5 bits [19:15]
- imm: It specifies the immediate value.
          It is of 12 bits [31:20]  
</pre>
S-type instruction
<pre>
  These are used for storing data from a register into memory.
</pre>  
Format of S-type instruction  
<pre>
    31      25 24    20 19    15 14    12 11     7 6       0
    |imm[11:5]|  rs2   |  rs1   |  funct3|imm[4:0]| opcode |
</pre>
<pre>
- opcode: It is a part of instruction which specifies the operation to be performed.  
          It is of 7 bits [6:0]  
- rs1,rs2: These fields contain register numbers  
           It is of 5 bits each  
- funct3: It specifies the function code for the operation.  
          It is of 3 bits [14:12]  
- imm : It specifies the immediate value.
        It is of 12 bits
</pre>
B-type instruction
<pre>
  These instructions are used for conditional branching based on a condition evaluated from comparing two register values.
</pre>
Format of B-type instruction
<pre>
    31        30       25 24    20 19    15 14    12 11       8        7 6       0
    |  imm[12]| imm[10:5]|  rs2   |  rs1   |  funct3| imm[4:1]| imm[11] | opcode |
</pre>
<pre>
- opcode: It is a part of instruction which specifies the operation to be performed.  
          It is of 7 bits [6:0]  
- rs1,rs2: These fields contain register numbers  
           It is of 5 bits each  
- funct3: It specifies the function code for the operation.  
          It is of 3 bits [14:12]  
- imm : It specifies the immediate value.
        It is of 12 bits
</pre>
U-type instruction 
<pre>
  These instructions are used for operations with immediate values that are wider than 12 bits.
</pre>
Format of U-type instruction
<pre>
    31                   12 11     7 6       0
    | imm[31:12]           |  rd    | opcode |
</pre>
<pre>
- opcode: It is a part of instruction which specifies the operation to be performed.  
          It is of 7 bits [6:0]  
- rd: It is the destination register which stores the destination address.  
      It is of 5 bits [11:7]  
- imm: It specifies immediate value
       It is of 20 bits [31:12]  
</pre>
J-type instruction 
<pre>
  These instructions are used for unconditional jumps.
</pre>
Format of J-type instruction
<pre>
   31     30 29       21 20     19 18        12 11     7 6       0
   |imm[20] | imm[10:1] | imm[11] | imm[19:12] |    rd  | opcode |
</pre>
<pre>
- opcode: It is a part of instruction which specifies the operation to be performed.  
          It is of 7 bits [6:0]  
- rd: It is the destination register which stores the destination address.  
      It is of 5 bits [11:7]  
- imm: It specifies immediate value
       It is of 20 bits 
</pre>
Examples
<pre>
  1.add r7,r1,r2
  Type :R
  32bit code :0110011 00001 00010 000 00110 0110011

  2.sub r7,r1,r2
  Type :R
  32bit code :0110011 00001 00010 000 00111 0110011

  3.and r8,r1,r3
  Type :R
  32bit code :0110011 00001 00011 000 01000 0110011

  4.or r9,r2,r5
  Type :R
  32bit code :0110011 00010 00101 110 01001 0110011

  5.xor r10,r1,r4
  Type :R
  32bit code :0110011 00001 00100 100 01010 0110011

  6.slt r11,r2,r4
  Type :R
  32bit code :0110011 00010 00100 010 01011 0110011

  7.addi r12,r4,5
  Type :I
  32bit code :000000000101 00100 000 01100 0010011 

  8.sw r3,r1,2
  Type :S
  32bit code :00010 00011 00001 010 00010 0100011

  9.lw r13,r1,2
  Type :I
  32bit code :000000000010 00001 010 01101 0000011

  10.beq r0,r0,15
  Type :B
  32bit code :0 00000 00000 00000 000 1100011

  11.bne r0,r1,20
  Type :B
  32bit code :1 00000 00001 00000 001 1100011

  12.sll r15,r1,r2(2)
  Type :S
  32bit code :0000000 00010 01110 101 10000 0110011

  13.srl r16,r14,r2(2)
  Type :
  32bit code :
</pre>
