# Mips64BitsAddition
64-bit Adds (45 points): Write a MIPS assembly program in the MARS simulator that solves the following problem. Ask the user to enter 4 unsigned (positive) 32-bit integers. Read these 4 integers; let's call them A, B, C, D. At the end of your program, registers $t8 and $t9 should contain the 64-bit result of ((A*B) + (C*D)); $t8 should have the most significant 32 bits and $t9 should have the least significant 32 bits. We will not test your code with invalid inputs, so you don't need to clutter your code with checks for invalid inputs. Hint: The tricky part here of course is to perform addition on two 64-bit values. Since you can only do 32-bit additions in MARS, you'll somehow have to figure out how to propagate a carry from the 32nd bit to the 33rd bit. When you add two large 32-bit numbers (with addu $t1, $t2, $t3), the result may be a 33-bit number, but MIPS does not give you access to that 33rd bit. So you'll have to explicitly compute that 33rd bit. Note that the 33rd bit is a 1 if at least two of the following three bits are 1: (i) the 32nd bit of the first operand, (ii) the 32nd bit of the second operand, (iii) the carry generated by the sum of the 31 least significant bits.
