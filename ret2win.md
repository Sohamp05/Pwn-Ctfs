### ret2win

After downloading and reversing the executable file, we find the following helpful functions:

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/25a1d6ce-36dc-42f3-9b74-a74255cd97c5)

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/7336cf9c-6732-4eca-bf2d-24791f8d9c13)

Disassembling these functions in gdb and ghidra we find the read function having vulnerability that it reads 56 bytes but the array has 32 bytes only so we can see the offset is 32 but what about the padding thus we put a patterned input to find the offset in gdb

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/c6c2cd95-eb82-4038-b45c-7cf34b42058a)

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/eb9a75ac-5a28-477a-bf79-78c38794aec1)

and thus offset is of 32 bytes and length of that string is padding 8 bytes and therefore we can run a python line script to get the flag

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/8b546204-e373-4757-b44b-661cc55a7267)

Ig the cat function is having some problem reading the file in my system but that should be the flag.
