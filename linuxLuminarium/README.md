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
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>

<details>
<summary style="cursor:pointer">Redirecting more output</summary>
  
Aside from redirecting the output of echo, you can, of course, redirect the output of any command. In this level, /challenge/run will once more give you a flag, but only if you redirect its output to the file myflag.

```bash
/challenge/run >> /home/hacker/the-flag
```

</details>

<details>
<summary style="cursor:pointer">Appending output</summary>

```bash
hacker@dojo:~$ echo pwn > outfile
hacker@dojo:~$ echo college >> outfile
hacker@dojo:~$ cat outfile
pwn
college
hacker@dojo:$
```

```
/challenge/run >> /home/hacker/the-flag
```

</details

<details>
<summary style="cursor:pointer">Redirection errors</summary>

FD 0: Standard Input
FD 1: Standard Output
FD 2: Standard Error

Redirecting errors is pretty easy from this point. If you have a command that might produce data via standard error
(such as /challenge/run), you can do:

```bash
hacker@dojo:~$ /challenge/run 2> errors.log
```

That will redirect standard error (FD 2) to the errors.log file. 
Furthermore, you can redirect multiple file descriptors at the same time! For example:

```
hacker@dojo:~$ some_command > output.log 2> errors.log
```

```
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag 

[FLAG] Here is your flag:
[FLAG] pwn.college{omF2_qusnKiCPvzLfo0WjmGN2Jy.QX3YTN0wyNxkTN1EzW}
```
</details


<details>
<summary style="cursor:pointer">Grep-ping stored resluts</summary>
  
In preparation for more complex levels, we want you to:

- Redirect the output of /challenge/run to /tmp/data.txt.
- This will result in a hundred thousand lines of text, with one of them being the flag, in /tmp/data.txt.
- grep that for the flag!

- && - combines 2 commands if the first sucessfull worked

```bash
 /challenge/run > /tmp/data.txt && grep -i 'pw' /tmp/data.txt
```

</details>


<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
<details>
<summary style="cursor:pointer">Redirecting output</summary>
  
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

```bash
echo PWN > COLLEGE
```

</details>
