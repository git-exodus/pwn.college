# Ethical Considerations
Remember that hacking into devices without permission is illegal and unethical.\
Always ensure you have the necessary permissions and are conducting these activities in a\
controlled environment for educational or security assessment purposes.

# Linux Luminarium
## Practicing Pipe
This module will teach you about input and output redirection. Simply put, every process in Linux has three initial, standard channels of communication:

- Standard Input - is the channel through which the process takes input. For example, your shell uses Standard Input to read the commands that you input.
- Standard Output - is the channel through which processes output normal data, such as the flag when it is printed to you in previous challenges or the output of utilities such as ls.
- Standard Error - is the channel through which processes output error details. For example, if you mistype a command, the shell will output, over standard error, that this command does not exist.
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
-  To access the memory contents at memory address 31337, you can do [31337] for the memory adress:
```bash
.intel_syntax noprefix
.global _start
_start:
mov rdi, [31337]
mov rax, 60
syscall
```

</details>

