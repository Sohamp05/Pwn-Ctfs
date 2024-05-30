### split
As you can see in the description it says bin/cat flag.txt is still there somewhere and we have got a useful function in it which we see at what address system() is call to pass the string cat flag so, first of all
pwnme function we need to put rdi function at the string's address and then call the system() so, now we search strings in the binary using -z in rabin2. and then find the pop rdi function's address using ropper and grep.

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/563f7378-5dfe-4361-b746-92392e042bdc)

Now to find the system's address we can use ghidra or get imp functions' address using r2

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/306e74bf-0bd2-4e37-93e5-7bd1a580fc89)

Now writing a script with offset of 40 first then a ret addr to resolve my movaps issue then the pop addr func then the string's address and then the system()

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/f801ccaf-2b9d-4475-8ad2-2c7646121fce)

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/f0b7a4ed-99c5-4479-8d35-8497c496b523)
