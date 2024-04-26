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
