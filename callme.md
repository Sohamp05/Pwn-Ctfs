### callme
Now in this challenge according to description we have to pass 3 args given 0xdeadbeefdeadbeef 0xcafebabecafebabfe and 0xd00df00dd00df00d to 3 callme 1,2,3 fucntions one after another.
So first we see that args are taken using rdi rsi and rdx registers and then we go on to find a gadget through which we can pop all 3 together and we get it

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/04ce2fb5-1475-48b2-80f5-399544fb9833)

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/5d1591f7-977e-49f1-9a69-46ee6d9bf574)

Now we get addr of the callme functions using the useful funcns and then we can pass buffer + args + callme1 + args + callme2 + args + callme3 and we pass all functions to get the flag using a script

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/ecd5a08d-dee0-4299-b287-a87b736de2b0)

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/1ac8674e-9aca-4d60-8e15-0ec21f51401c)

![image](https://github.com/Sohamp05/Pwn-Ctfs/assets/142091197/c2b881e4-7906-496a-8540-609c587758a7)
