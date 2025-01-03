# VSD_mini_workshop
This is an exclusive Repo, created to document my task given in this workshop
---
→ TASK:1   # This task deals with the basics, how we can compile C code using GCC and RISCV compiler. this task provides you an idea that how the RISC-V architecture works.

---
#  C Code Compilation Guide
## Objective
Learn how to compile C programs using both standard GCC and RISC-V compiler on Linux.

## Part A: Regular C Compilation
1. Create and Edit Your Program
   - Open your terminal
   - Navigate to your working directory
   - Create a new C file with: sum1ton.c
   - Write a simple program to add numbers from 1 to n
   - Save with Ctrl + S and exit with Ctrl + W


2. Compile with GCC
   - In the terminal, compile your code:
   ```
   gcc sum1ton.c
   ./a.out
   

## Part B: RISC-V Compilation
1. View Your Code
   - Display your source code:
   ```
   cat sum1ton.c
   

2. RISC-V Compilation Steps
   - Compile with O1 optimization:
   ```
   riscv64-unknown-elf-objdump -O1 sum1ton.o

   riscv64-unknown-elf-objdump -d a.out
   

3. Compare Different Optimization
   - Compile with fast optimization:
  ```
   riscv64-unknown-elf-objdump -Ofast sum1ton.c
```
   
   - View optimized assembly:
```
   riscv64-unknown-elf-objdump -d a.out
  ```
```
```
   ---

## Key Learning Points
- Understanding basic C program compilation
- Learning about different compiler optimizations
- Comparing assembly output between optimization levels
- Introduction to RISC-V architecture compilation

## Sample Program Structure
c
```
#include <stdio.h>

int main() {
    int n = 10, sum = 0;
    
    for(int i = 1; i <= n; i++) {
        sum += i;
    }
    
    printf("Sum of first %d numbers is: %d\n", n, sum);
    return 0;
}
