# Hello Hacker
In this challenge we get to know the very basics of comand line
-Into to comands
-Intro to arguments
-Command History

## My solve
###Challenge-1: Intro to comands
**Flag:** `pwn.college{8lnimeKHhZ_-ruTKf-HQhOQ_hzV.QX3YjM1wiM5EzNzEzW}`
For this challenge we have to execute the whoami command that prints user name in the terminal. Then we have to type hello to get the flag.
```bash
hacker@hello~intro-to-commands:~$ whoami
hacker
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{8lnimeKHhZ_-ruTKf-HQhOQ_hzV.QX3YjM1wiM5EzNzEzW}

```
###Challenge-2: Intro to arguments
**Flag:** `pwn.college{8lnimeKHhZ_-ruTKf-HQhOQ_hzV.QX3YjM1wiM5EzNzEzW}`
For this challenge we use the echo command and the argument hello. The echo command simply 'echoes' or prints all of its arguments back out into the terminal.

```bash
hacker@hello~intro-to-commands:~$ echo Hello Hackers!
Hello Hackers!
hacker@hello~intro-to-commands:~$ hello hacker
Success! Here is your flag:
pwn.college{8lnimeKHhZ_-ruTKf-HQhOQ_hzV.QX3YjM1wiM5EzNzEzW}
```
for example, here Hello and Hackers! are two arguments to echo.

###Challenge-3:Command History
**Flag:** `{MNzIsYfXNIF4kuu5KgmrWEVETwx.0lNzEzNxwiM5EzNzEzW}`
For this challenge we use the up and down arrow key to bring back a command already typed previously. This prevents us from writing the entire code over and over again. 

```bash
hacker@hello~intro-to-commands:~$ the flag is pwn.college{MNzIsYfXNIF4kuu5KgmrWEVETwx.0lNzEzNxwiM5EzNzEzW}
```

## What I learned
**Challenge_1**:I learned that to get flag first we have to link our SSH key; and the very basic command line. 
**Challenge_2**: I learned that in this challenge to get flag we have to run the hello command with single argument.
**Challenge_3**: I learned that using the up and down arrow key we can easily get the previously written command.
## References 
The video under the command line section. 
