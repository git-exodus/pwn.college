# Computing101
## Memory manipulation

<details>
<summary style="cursor:pointer">Loading from memory</summary>
  
-  To access the memory contents at memory address 31337, you can do [31337] for the memory adress:
```bash
.intel_syntax noprefix
.global _start
_start:
mov rdi, [31337]
mov rax, 60
syscall
```
then:  hacker@dojo:$ as -o programm.o programm.s\
then:  hacker@dojo:$ ld -o programm programm.o\
then:  hacker@dojo:$ programm

- mov -- mov DOES NOT move the memory content out, from one memory adress into the next one >> it COPYS it - both memory adresses have the same content!
- as -- The "as" tool reads in program.s, assembles it into binary code, and outputs an object file called program.o.\
- ld -- Linking Object Files into an Executable. In a typical development workflow, source code is compiled and assembly is assembled to object files, and there are typically many of these (generally,
 each source code file in a program compiles into its own object file). These are then linked together into a single executable. Even if there is only one
 file, we still need to link it, to prepare the final executable. This is done with the ld (stemming from the term "link editor") command.\

- When the CPU executes this instruction, it of course understands that 31337 is an address, not a raw value. If you think of the instruction as a person
telling the CPU what to do, and we stick with our "houses on a street" analogy, then instead of just handing the CPU data, the instruction/person points 
at a house on the street. The CPU will then go to that address, ring its doorbell, open its front door, drag the data that's in there out, and put it into
rdi. Thus, the 31337 in this context is the memory address and serves to point to the data stored at that memory address. After this instruction executes, 
the value stored in rdi will be 42!
</details>

<details>
<summary style="cursor:pointer">More loading practice</summary>
  
-  same with 123400 - programm name loadingfrommemorymore.s
```bash
.intel_syntax noprefix
.global _start
_start:
mov rdi, [123400]
mov rax, 60
syscall

hacker@memory~more-loading-practice:~/assambly/memory$ as -o loadingfrommemorymore.o loadingfrommemorymore.s
hacker@memory~more-loading-practice:~/assambly/memory$ ld -o loadingfrommemorymore loadingfrommemorymore.o
hacker@memory~more-loading-practice:~/assambly/memory$ /challenge/check ~/assambly/memory/loadingfrommemorymore

Checking the assembly code...
... YES! Great job!

Let's check what your exit code is! It should be our secret value
stored at memory address 123400 (value 71) to succeed!

hacker@memory~more-loading-practice:/home/hacker/assambly/memory$ /tmp/your-program
hacker@memory~more-loading-practice:/home/hacker/assambly/memory$ echo $?
71
hacker@memory~more-loading-practice:/home/hacker/assambly/memory$ 

Neat! Your program passed the tests! Great job!

Here is your flag!
pwn.college{
```
</details>
