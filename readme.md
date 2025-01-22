# RISC-V Instruction Breakdown

## Overview

This repository contains a detailed breakdown of 15 unique RISC-V instructions from the `riscv-objdump` of the application code. Each instruction is analyzed to determine its exact 32-bit instruction code in their respective instruction type formats (R, I, S, B, U, and J).

## Instructions

1. **Review the RISC-V software documentation** to understand the R, I, S, B, U, and J instruction types.
2. **Check out this [sample GitHub repository](link)** for a visual guide on decoding RISC-V instructions.
3. **Identify 15 unique RISC-V instructions** from the `riscv-objdump` of your application code.
4. **Determine the exact 32-bit instruction code** for those 15 instructions in their respective instruction type formats.
5. **Upload the 32-bit instruction patterns** to this GitHub repository.

## Instruction Breakdown

Below is the breakdown of each instruction:

### 1. `lui a0, 0x19`

- **Type**: U
- **Opcode**: `0110111`
- **Immediate**: `0x19`
- **Binary Representation**: `00000000000110010000000010110111`

### 2. `addi a0, a0, 1288`

- **Type**: I
- **Opcode**: `0010011`
- **Immediate**: `1288`
- **Binary Representation**: `00000101000000001000001010010011`

### 3. `jal 10664 <puts>`

- **Type**: J
- **Opcode**: `1101111`
- **Immediate**: `10664`
- **Binary Representation**: `00000010100100000000000011101111`

### 4. `j 101bc <main+0x80>`

- **Type**: J
- **Opcode**: `1101111`
- **Immediate**: `101bc`
- **Binary Representation**: `00000010101111000000000011101111`

### 5. `addiw a3, a1, -1`

- **Type**: I
- **Opcode**: `0011011`
- **Immediate**: `-1`
- **Binary Representation**: `11111111111100001011000110110011`

### 6. `blt a3, a4, 10182 <main+0x46>`

- **Type**: B
- **Opcode**: `1100011`
- **Immediate**: `10182`
- **Binary Representation**: `00000000000000000000000011000111`

### 7. `subw a1, a3, a4`

- **Type**: R
- **Opcode**: `0111011`
- **Function (funct3)**: `000`
- **Function (funct7)**: `0100000`
- **Binary Representation**: `01000000000000001011000110110011`

### 8. `sraiw a1, a1, 0x1`

- **Type**: I
- **Opcode**: `0011011`
- **Immediate**: `0x1`
- **Binary Representation**: `00000000000100001011000110110011`

### 9. `addw a1, a1, a4`

- **Type**: R
- **Opcode**: `0111011`
- **Function (funct3)**: `000`
- **Function (funct7)**: `0000000`
- **Binary Representation**: `00000000000000001011000110110011`

### 10. `slli a5, a1, 0x2`

- **Type**: I
- **Opcode**: `0010011`
- **Immediate**: `0x2`
- **Binary Representation**: `00000000001000001011000100110011`

### 11. `add a5, a5, a0`

- **Type**: R
- **Opcode**: `0110011`
- **Function (funct3)**: `000`
- **Function (funct7)**: `0000000`
- **Binary Representation**: `00000000000000001011000100110011`

### 12. `lw a5, 0(a5)`

- **Type**: I
- **Opcode**: `0000011`
- **Immediate**: `0`
- **Binary Representation**: `00000000000000001011000100000011`

### 13. `bne a5, a2, 10176 <main+0x3a>`

- **Type**: B
- **Opcode**: `1100011`
- **Immediate**: `10176`
- **Binary Representation**: `00000000000000000000000011000111`

### 14. `li a5, -1`

- **Type**: I
- **Opcode**: `0010011`
- **Immediate**: `-1`
- **Binary Representation**: `11111111111100001011000100110011`

### 15. `ret`

- **Type**: I
- **Opcode**: `1100111`
- **Immediate**: `0`
- **Binary Representation**: `00000000000000001011000111001111`

### task4

# RISC-V Instructions

This repository contains a set of RISC-V instructions along with their standard and hardcoded 32-bit instruction codes, as well as detailed explanations and examples.

## Instructions

### 1. ADD R6, R2, R1

- **Operation**: Adds the values in registers R2 and R1, and stores the result in register R6.
- **Example**: If R2 = 5 and R1 = 3, then R6 = 5 + 3 = 8.
- **Standard 32-bit Code**: `32'h00110333`
- **Hardcoded 32-bit Code**: `32'h02208300`

### 2. SUB R7, R1, R2

- **Operation**: Subtracts the value in register R2 from the value in register R1, and stores the result in register R7.
- **Example**: If R1 = 10 and R2 = 4, then R7 = 10 - 4 = 6.
- **Standard 32-bit Code**: `32'h402083b3`
- **Hardcoded 32-bit Code**: `32'h02209380`

### 3. AND R8, R1, R3

- **Operation**: Performs a bitwise AND operation on the values in registers R1 and R3, and stores the result in register R8.
- **Example**: If R1 = 6 (binary 110) and R3 = 3 (binary 011), then R8 = 2 (binary 010).
- **Standard 32-bit Code**: `32'h0030f433`
- **Hardcoded 32-bit Code**: `32'h0230a400`

### 4. OR R9, R2, R5

- **Operation**: Performs a bitwise OR operation on the values in registers R2 and R5, and stores the result in register R9.
- **Example**: If R2 = 6 (binary 110) and R5 = 3 (binary 011), then R9 = 7 (binary 111).
- **Standard 32-bit Code**: `32'h005164b3`
- **Hardcoded 32-bit Code**: `32'h02513480`

### 5. XOR R10, R1, R4

- **Operation**: Performs a bitwise XOR operation on the values in registers R1 and R4, and stores the result in register R10.
- **Example**: If R1 = 6 (binary 110) and R4 = 3 (binary 011), then R10 = 5 (binary 101).
- **Standard 32-bit Code**: `32'h0040c533`
- **Hardcoded 32-bit Code**: `32'h0240c500`

### 6. SLT R1, R2, R4

- **Operation**: Sets register R1 to 1 if the value in register R2 is less than the value in register R4, otherwise sets it to 0.
- **Example**: If R2 = 3 and R4 = 5, then R1 = 1.
- **Standard 32-bit Code**: `32'h0045a0b3`
- **Hardcoded 32-bit Code**: `32'h02415580`

### 7. ADDI R12, R4, 5

- **Operation**: Adds the immediate value 5 to the value in register R4, and stores the result in register R12.
- **Example**: If R4 = 7, then R12 = 7 + 5 = 12.
- **Standard 32-bit Code**: `32'h004120b3`
- **Hardcoded 32-bit Code**: `32'h00520600`

### 8. BEQ R0, R0, 15

- **Operation**: Branches to the address 15 instructions ahead if the values in registers R0 and R0 are equal. Since R0 is always zero, this condition is always true.
- **Example**: The program counter will jump to the address 15 instructions ahead.
- **Standard 32-bit Code**: `32'h00000f63`
- **Hardcoded 32-bit Code**: `32'h00f00002`

### 9. SW R3, R1, 2

- **Operation**: Stores the value in register R3 into the memory address calculated by adding the value in register R1 and the offset 2.
- **Example**: If R3 = 10 and R1 = 100, the value 10 will be stored at the memory address 102.
- **Standard 32-bit Code**: `32'h0030a123`
- **Hardcoded 32-bit Code**: `32'h00209181`

### 10. LW R13, R1, 2

- **Operation**: Loads a 32-bit word from the memory address calculated by adding the value in register R1 and the offset 2, and stores it in register R13.
- **Example**: If the memory address 102 contains the value 20 and R1 = 100, then R13 = 20.
- **Standard 32-bit Code**: `32'h0020a683`
- **Hardcoded 32-bit Code**: `32'h00208681`

### 11. SRL R16, R14, R2

- **Operation**: Performs a logical right shift on the value in register R14 by the number of positions specified in register R2, and stores the result in register R16.
- **Example**: If R14 = 16 (binary 10000) and R2 = 2, then R16 = 4 (binary 100).
- **Standard 32-bit Code**: `32'h0030a123`
- **Hardcoded 32-bit Code**: `32'h00271803`

### 12. SLL R15, R1, R2

- **Operation**: Performs a logical left shift on the value in register R1 by the number of positions specified in register R2, and stores the result in register R15.
- **Example**: If R1 = 3 (binary 11) and R2 = 2, then R15 = 12 (binary 1100).
- **Standard 32-bit Code**: `32'h002097b3`
- **Hardcoded 32-bit Code**: `32'h00208783`
