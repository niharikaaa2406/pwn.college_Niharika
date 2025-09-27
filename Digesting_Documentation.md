# Digesting Documentation
## My solve
### Challenge 1: Learning from documentation
**Flag:** `pwn.college{Ea6y1H-vLdF0tVuLWWYrmnYUC1J.QX0ITO0wiM5EzNzEzW}`
We learn the correct usage of commands for running programs.
```bash
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{Ea6y1H-vLdF0tVuLWWYrmnYUC1J.QX0ITO0wiM5EzNzEzW}
```

### Challenge 2: Learning Complex Usage
**Flag:** `pwn.college{Y4qLqLTAI8Ztm-cyJdU-fYVXmUz.QX1ITO0wiM5EzNzEzW}`

Using more than one arguments.
```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{Y4qLqLTAI8Ztm-cyJdU-fYVXmUz.QX1ITO0wiM5EzNzEzW}
```

### Challenge 3: Reading Manuals
**Flag:** `pwn.college{MxI-TKNRNcvrKHByQypigWD3iGF.QX0EDO0wiM5EzNzEzW}`
**man command** (man is short for manual) gives manual of the commands to be passed as arguments. When you are done using hit q (for quit). The path of database is /usr/share/man directory(no need for path we can just use the man command).
```bash
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --xcvryy 300
Correct usage! Your flag: pwn.college{MxI-TKNRNcvrKHByQypigWD3iGF.QX0EDO0wiM5EzNzEzW}
```

### Challenge 4: Searcing Manuals
**Flag:** ` pwn.college{ML6CTV7e1nW1cBxyEKbzhrS3QoW.QX1EDO0wiM5EzNzEzW} `
We can search in a manual with / and go to next result using n and N for previous result. ? to search backwords.
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --ulm
Initializing...
Correct usage! Your flag: pwn.college{ML6CTV7e1nW1cBxyEKbzhrS3QoW.QX1EDO0wiM5EzNzEzW}
```

### Challenge 5: Searchng For Manuals
**Flag:** `pwn.college{cB5WhOP4skgWa4UB3frs0jjgpa7.QX2EDO0wiM5EzNzEzW}`

man man is used to find the manuals we are looking for.

```bash
hacker@man~searching-for-manuals:~$ man man challenge
No manual entry for challenge
hacker@man~searching-for-manuals:~$ man -k challenge
chskgafrsj (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man chskgafrsj
hacker@man~searching-for-manuals:~$ /challenge/challenge --chskga 544
Correct usage! Your flag: pwn.college{cB5WhOP4skgWa4UB3frs0jjgpa7.QX2EDO0wiM5EzNzEzW}
```

### Challenge 6: Helpful Programs
**Flag:** `pwn.college{I13tR7gW3Fbr9ClmDr6WB6a1-VZ.QX3IDO0wiM5EzNzEzW}`
Some programs don't have a man page, but --help (-h, -?, help,/) can be used instead. 
```bash
Connected!
hacker@man~helpful-programs:~$ /challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 137
hacker@man~helpful-programs:~$ /challenge/challenge --give-the-flag 137
Correct usage! Your flag: pwn.college{I13tR7gW3Fbr9ClmDr6WB6a1-VZ.QX3IDO0wiM5EzNzEzW}
```

### Challenge 7: Help for Builtins
**Flag:** `pwn.college{sppFnxfVBSmHUNVEkogYEUXh7N4.QX0ETO0wiM5EzNzEzW}`
Some commands are bult into the shell itself meaning we can't access it through the previous two commands. These are called bulitins.We can access shell of builitin using "help". We can be specific as well.
```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "sppFnxfV".
hacker@man~help-for-builtins:~$ challenge --secret sppFnxfV
Correct! Here is your flag!
pwn.college{sppFnxfVBSmHUNVEkogYEUXh7N4.QX0ETO0wiM5EzNzEzW}
```
## What I learned
In this module I learned various commands and it's method of application for example, cat, grep, ls, diff, touch, rm, mkdir, ls -a, find, ln -s.

## References 
The video provided in the module.

