# Assembly Segmentation Fault

This repository demonstrates a common error in assembly programming: accessing memory outside the allocated space. This leads to a segmentation fault, a serious runtime error. The `bug.asm` file contains the erroneous code, while `bugSolution.asm` presents a corrected version.

The core problem is in the `mov` instruction within the `bug.asm` file.  It computes a memory address dynamically, and a potential overflow in the calculation leads to out-of-bounds memory access. The solution implements proper bounds checking and error handling to mitigate this risk.

## How to reproduce
1. Assemble `bug.asm`.
2. Run the resulting executable; observe the segmentation fault. 
3. Assemble `bugSolution.asm` and run; it will execute without errors. 

## Learning Points
* Careful attention to memory address calculations is crucial in assembly programming.
* Overflow and underflow conditions must be handled to prevent memory access violations.
* Employ bounds checking where appropriate. 
* Proper error handling can prevent crashes.