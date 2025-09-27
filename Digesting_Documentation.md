# Digesting_Documentation
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

### Challenge 7: touching files
**Flag:** `pwn.college{0x2g_j5tSzFEmUQgQA9iVzUNpPD.QXwMDO0wiM5EzNzEzW}`
A simple way to create a file is by using **touch command** , in the format "touch filename" this will create a file in the current directory.

```bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{0x2g_j5tSzFEmUQgQA9iVzUNpPD.QXwMDO0wiM5EzNzEzW}
hacker@commands~touching-files:/tmp$
```

### Challenge 8: removing files
**Flag:** `pwn.college{ATYiAd7znlRT3Nd9kygYz3eLKcp.QX2kDM1wiM5EzNzEzW}`
To clean up a directory (delete some files) we will use the rm command in the format "rm file_name"
```bash
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{ATYiAd7znlRT3Nd9kygYz3eLKcp.QX2kDM1wiM5EzNzEzW}
hacker@commands~removing-files:~$
```

### Challenge 9: moving files
**Flag:** `pwn.college{A_DIhv2GsUfuWApumsEy3LsC8fE.0VOxEzNxwiM5EzNzEzW}`
We can also move files with **mv command**, it can be used in the format my "mv file_to_be_moved file_final"
```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{A_DIhv2GsUfuWApumsEy3LsC8fE.0VOxEzNxwiM5EzNzEzW}
```

### Challenge 10: hidden files
**Flag:** `pwn.college{gpGPP-YM93BEKcBMWrRgkuZfGsV.QXwUDO0wiM5EzNzEzW}`
We know that we can get list of files in a directory through ls command but to access the hidden files (files that start with .) as well we will use "-a"  
```bash
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.           .flag-23971838819791  challenge  home   lib64   mnt  proc  sbin  tmp
..          bin                   dev        lib    libx32  nix  root  srv   usr
.dockerenv  boot                  etc        lib32  media   opt  run   sys   var
hacker@commands~hidden-files:/$ cat .flag-23971838819791
pwn.college{gpGPP-YM93BEKcBMWrRgkuZfGsV.QXwUDO0wiM5EzNzEzW}
hacker@commands~hidden-files:/$
```


### Challenge 11: An Epic Filesystem Quest
**Flag:** `pwn.college{A_DIhv2GsUfuWApumsEy3LsC8fE.0VOxEzNxwiM5EzNzEzW}`
A small game where we will use ls, cat and cd command. I flag is hidden in challenge directory we have to use ls and cat to find it.
```bash
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{A_DIhv2GsUfuWApumsEy3LsC8fE.0VOxEzNxwiM5EzNzEzW}
```
### Challenge 12: making directories
**Flag:** `pwn.college{cJeXaRAFvKEBvZ3Y4uiL6ZLHcXk.QXxMDO0wiM5EzNzEzW}`
We know how to create files now let's know how to create directories.We will use the command **mkdir**.
```bash
Connected!
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.4mK6TfTSUV
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{cJeXaRAFvKEBvZ3Y4uiL6ZLHcXk.QXxMDO0wiM5EzNzEzW}
```

### Video 14: Symbolic Links
It is a special type of filethat refers another file.
They are created using ln -s (-s stands for symbolic). 

### Challenge 15: linking files
**Flag:** `pwn.college{UUy5yFmBgFhCRC9Lr6QxFlab2ty.QX5ETN1wiM5EzNzEzW}`
Links are of two types hard and soft(also known as symbolic). A hard link can be sad as a link described by many address so that all lead to a specific place. A soft link is when you point out to another file. It's format is "ln -s /current_file /pointing_to_a_new_file"  the new files gets the original file's content.

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{UUy5yFmBgFhCRC9Lr6QxFlab2ty.QX5ETN1wiM5EzNzEzW}
hacker@commands~linking-files:~$
```
## What I learned
In this module I learned various commands and it's method of application for example, cat, grep, ls, diff, touch, rm, mkdir, ls -a, find, ln -s.

## References 
The video provided in the module.

