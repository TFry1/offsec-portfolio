# Very easy disassembly exercise - RodrigoTeixeiera  
**Source:** Crackmes.one  
**Category:** Reversing   
**Status:** Solved  
**Difficulty:** 1.0  

**GOAL:** Retrieve a hard coded integer from the executable

**FILES:**
crackme.exe - binary for the crackme
screenshots/ - images for the writeup
writeup.md - this file

**Tools:** strings, Ghidra

**Analysis:**
Used strings to look for anything that will standout, strings such as "Enter the password"
Open the binary with Ghidira, go to window -> definedstrings -> "Enter the password" to jump to that section of binary
The pseudocode shows that scanf is being used to get user input and compare that variable to a hardcoded integer (hex)
After converting the hex number to decimal, you can run the program, enter the number 124816 when prompted, and the
program will print successful. 

**Takeaways:**
Don't put hardcoded integers in the source code when checking for a password, at the very least 
obfuscate/encrypt the password.

**Date:** 10/25/2025
**Writeup by:** Tyler Fry
