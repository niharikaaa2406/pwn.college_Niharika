# File Globbing
## My solve
### Challenge 1: Matching with *
**Flag:** `pwn.college{8UvTn6n44QAONFnnxNj41mN4nfm.QXxIDO0wiM5EzNzEzW}`
* shell will treat it as a "wildcard" and try to replace that argument with any files that matches the pattern.
* If zero results are matched it will give nope_*. * can be any part except / and . characters.
```bash
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8UvTn6n44QAONFnnxNj41mN4nfm.QXxIDO0wiM5EzNzEzW}
```

### Challenge 2: Matching with ?
**Flag:** `pwn.college{o4OrzjU09LJt7TuoZyn2tUggdb0.QXyIDO0wiM5EzNzEzW}`
? is used in plavce of single character wildcard unlike *
```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{o4OrzjU09LJt7TuoZyn2tUggdb0.QXyIDO0wiM5EzNzEzW}
```

### Challenge 3: Matching with []
**Flag:** `pwn.college{MgS20XNxBbvixST5xBJdDvWJTba.QXzIDO0wiM5EzNzEzW}`
It is a limited form of ?, it dosen't match any character but a subset of potential characters, specified within the brackets.
```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{MgS20XNxBbvixST5xBJdDvWJTba.QXzIDO0wiM5EzNzEzW}
hacker@globbing~matching-with-:/challenge/files$
```

### Challenge 4: Matching paths with []
**Flag:** ` pwn.college{ML6CTV7e1nW1cBxyEKbzhrS3QoW.QX1EDO0wiM5EzNzEzW} `
We can search in a manual with / and go to next result using n and N for previous result. ? to search backwords.
```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --ulm
Initializing...
Correct usage! Your flag: pwn.college{ML6CTV7e1nW1cBxyEKbzhrS3QoW.QX1EDO0wiM5EzNzEzW}
```

### Challenge 5: Multiple globs
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

### Challenge 6: Mixing globs
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

### Challenge 7: Exclusionary globbing
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
I learned how to refer files without typing the full path out.
## References 
The resources provided in the module.

