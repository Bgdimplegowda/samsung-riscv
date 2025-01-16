**TASK 03**

**1.INSTRUCTIONS : lui a0, 0x2b**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_17_59_53.png?raw=true)

(0002b537)

**Opcode**: 0110111 (U-type)

**funct3**: N/A (Not used in U-type)

**imm**: 0x2b000 (The 20-bit immediate is shifted left by 12 bits)

**rs1**: N/A

**rd**: a0 (x10)

**Functionality**: Loads the 20-bit immediate value into the upper 20 bits of a0, setting the lower 12 bits to 0.

**2.INSTRUCTIONS : addi sp, sp, -32**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_01_06.png?raw=true)

(fe010113)

**Opcode:** 0010011 (I-type)

**funct3:** 000 (ADDI)

**imm:** -32 (Sign-extended to 32 bits: 0xffffffffffffffe0)

**rs1:** sp (x2)

**rd:** sp (x2)

**Functionality:** Adds the immediate value (-32) to the value in sp and stores the result back in sp.

**3.INSTRUCTIONS : addi a0, a0, -976**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_17_35.png?raw=true)

(c3050513)

**Opcode:** 0010011 (I-type)

**funct3:** 000 (ADDI)

**imm:** -976 (Sign-extended: 0xfffffffffffc30)

**rs1:** a0 (x5)

**rd:** a0 (x5)

**Functionality:** Adds the immediate value (-976) to the value in a0 and stores the result back in a0.

**4.INSTRUCTIONS : sd, ra, 24(sp)** 

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_18_02.png?raw=true)

 (00113c23)
 
**Opcode:** 1100011 (S-type)

**funct3:** 011 (SD - Store Doubleword)

**imm:** 24 (Split into imm[11:5] and imm[4:0])

**rs1:** sp (x2)

**rd:** ra (x1) (rs2 in S-type)

**Functionality:** Stores the 64-bit value in ra to the memory location at sp + 24.

**5.INSTRUCTIONS : jal ra, 10438**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_18_34.png?raw=true)

(378000ef)

**Opcode:** 1101111 (J-type)

**funct3:** N/A

**imm:** 10438 (The 20-bit immediate is used to calculate the jump offset)

**rs1:** N/A

**rd:** ra (x1)

**Functionality:** Jumps to the target address (10438) and stores the return address in ra.

**6.INSTRUCTIONS : addi a1, sp, 12**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_19_23.png?raw=true)

(00c10593)

**Opcode:** 0010011 (I-type)

**funct3:** 000 (ADDI)

**imm:** 12

**rs1:** sp (x2)

**rd:** a1 (x11)

**Functionality:** Adds 12 to the value in sp and stores the result in a1.

**7.INSTRUCTIONS : jal ra, 1048c**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_20_01.png?raw=true)

(3bc000ef)

**Opcode:** 1101111 (J-type)

**funct3:** N/A

**imm:** 1048c

**rs1:** N/A

**rd:** ra (x1)

**Functionality:** Jumps to the target address (1048c) and stores the return address in ra.

**8.INSTRUCTIONS :lw a5, 12(sp)**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_20_31.png?raw=true)

(00c12783)

**Opcode:** 0000011 (I-type)

**funct3:** 010 (LW - Load Word)

**imm:** 12

**rs1:** sp (x2)

**rd:** a5 (x15)

**Functionality:** Loads a 32-bit word from memory at sp + 12 into a5.

**9.INSTRUCTIONS : andi a5, a5, 12**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_20_51.png?raw=true)

(0017f793)

**Opcode:** 0010011 (I-type)

**funct3:** 111 (ANDI)

**imm:** 1

**rs1:** a5 (x15)

**rd:** a5 (x15)

**Functionality:** Performs a bitwise AND between a5 and 1, storing the result in a5.

**10.INSTRUCTIONS :bnez a5, 100fc**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_21_31.png?raw=true)

(02079063)

**Opcode:** 1100011 (B-type)

**funct3:** 001 (BNE - Branch if Not Equal to Zero)

**imm:** Calculated from the offset to 100fc

**rs1:** a5 (x15)

**rd:** N/A (rs2 is implicitly zero)

**Functionality:** Branches to 100fc if a5 is not zero.

**11.INSTRUCTIONS :ld ra, 24(sp)**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_22_00.png?raw=true)

(01813083)

**Opcode:** 0000011 (I-type)

**funct3:** 011 (LD - Load Doubleword)

**imm:** 24

**rs1:** sp (x2)

**rd:** ra (x1)

**Functionality:** Loads a 64-bit doubleword from memory at sp + 24 into ra.

**12.INSTRUCTIONS : li a0, 0**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_22_24.png?raw=true)

(00000513)

**Opcode:** 0010011 (I-type)

**funct3:** 000 (ADDI)

**imm:** 0

**rs1:** x0 (zero)

**rd:** a0 (x5)

**Functionality:** Loads the immediate value 0 into a0 (equivalent to addi a0, x0, 0).

**13.INSTRUCTIONS :addi sp, sp, 32**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_22_52.png?raw=true)

(02010113)

**Opcode:** 0010011 (I-type)

**funct3:** 000 (ADDI)

**imm:** 32

**rs1:** sp (x2)

**rd:** sp (x2)

**Functionality:** Adds 32 to sp.

**14.INSTRUCTIONS :ret**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_23_10.png?raw=true)

(00008067)

**Opcode:** 1100111 (I-type for JALR)

**funct3:** 000 (JALR)

**imm:** 0

**rs1:** ra (x1)

**rd:** x0 (zero)

**Functionality:** Returns from a function (jumps to the address in ra).

**15.INSTRUCTIONS :j 100ec**

![image alt](https://github.com/Bgdimplegowda/samsung-riscv/blob/main/task%203/VirtualBox_vsdworkshop_16_01_2025_18_23_48.png?raw=true)

(fe5ff06f)

**Opcode:** 1101111 (J-type)

**funct3:** N/A

**imm:** Calculated offset to 100ec

**rs1:** N/A

**rd:** x0 (zero)

**Functionality:** Unconditional jump to 100ec.

