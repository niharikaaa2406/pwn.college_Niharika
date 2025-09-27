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
**Flag:** `pwn.college{Qwq0efHbSwM7wfu9anmNYeTkdnf.QX0IDO0wiM5EzNzEzW}`
An entire path can be globbed. For example:
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{Qwq0efHbSwM7wfu9anmNYeTkdnf.QX0IDO0wiM5EzNzEzW}
```

### Challenge 5: Multiple globs
**Flag:** `pwn.college{QQKJVKCVRqjjhvfNfeP5B4PisVn.0lM3kjNxwiM5EzNzEzW}`

We can use multiple glob at a time.

```bash
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{QQKJVKCVRqjjhvfNfeP5B4PisVn.0lM3kjNxwiM5EzNzEzW}
```

### Challenge 6: Mixing globs
**Flag:** `pwn.college{I13tR7gW3Fbr9ClmDr6WB6a1-VZ.QX3IDO0wiM5EzNzEzW}`
Some programs don't have a man page, but --help (-h, -?, help,/) can be used instead. 

### Challenge 7: Exclusionary globbing
**Flag:** `pwn.college{sppFnxfVBSmHUNVEkogYEUXh7N4.QX0ETO0wiM5EzNzEzW}`
It is used to filter out files in a glob using ! and ^.
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

### Challenge 8: Tab completion
**Flag:** `pwn.college{YjaczaUNdCbaQKiZFxOVQbp70yC.0FN0EzNxwiM5EzNzEzW}`
Instead of * to shorten it we can use tab to auto-complete.
```bash
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​
pwn.college{YjaczaUNdCbaQKiZFxOVQbp70yC.0FN0EzNxwiM5EzNzEzW}
```

### Challenge 9: Multiple option for tab completion
**Flag:** `cat: /challeng/files/pwn-college: No such file or directory`
In case of multiple options the number of time you press tab the next option is told. 
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{Qwq0efHbSwM7wfu9anmNYeTkdnf.QX0IDO0wiM5EzNzEzW}
```

### Challenge 10: Tab completion on commands
**Flag:** `pwn.college{Qwq0efHbSwM7wfu9anmNYeTkdnf.QX0IDO0wiM5EzNzEzW}`
An entire path can be globbed. For example:
```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{Qwq0efHbSwM7wfu9anmNYeTkdnf.QX0IDO0wiM5EzNzEzW}
```

## What I learned
I learned how to refer files without typing the full path out.
## References 
The resources provided in the module.

