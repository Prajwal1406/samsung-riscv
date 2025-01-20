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
