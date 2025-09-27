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
**Flag:** `pwn.college{4vVibc6gdw_aUP2Qxtpi65C1o0R.QXwITO0wiM5EzNzEzW}`

Some more cat command with absolute path examples.
```bash
hacker@commands~more-catting-practice:~$ cat /lib/X11/flag
pwn.college{4vVibc6gdw_aUP2Qxtpi65C1o0R.QXwITO0wiM5EzNzEzW}
hacker@commands~more-catting-practice:~$
```

### Challenge 4: Searcing Manuals
**Flag:** `pwn.college{ggC2CC4vmYScsHKk8g-w8ez5Keu.QX3EDO0wiM5EzNzEzW}`

**grep command** is used to search for the context we need for times when the files are too big. There are multiple ways to grep.

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep "pwn.college" /challenge/data.txt
pwn.college{ggC2CC4vmYScsHKk8g-w8ez5Keu.QX3EDO0wiM5EzNzEzW}
```

### Challenge 5: comparing files
**Flag:** `> pwn.college{A8THlHbuTyIZOGFndPvgbNV7UTW.01MwMDOxwiM5EzNzEzW}`

**diff command** compares two files line by line and shows exactly why they are different. 
<br>
example, 2c2 means line 2 of file one is different from that f file 2<br>
1a2 means after line 1 of file 1 another line is added to line 2 of file 2.

Here to get the flag we have to find the diff between two files having many fake flags and one different actual flag.


```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
92a93
> pwn.college{A8THlHbuTyIZOGFndPvgbNV7UTW.01MwMDOxwiM5EzNzEzW}
```

### Challenge 6: listing files
**Flag:** `pwn.college{ABMxGPyUBLw5UwUGxq2GIzyfa67.QX4IDO0wiM5EzNzEzW}`

For cases when we don't know the entire content od a directory we can use ls command to list all files in a directory.
If ls command is used without any argument it will list all files in the current directory.

```bash
hacker@commands~listing-files:~$ ls /challenge
21556-renamed-run-19519  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/21556-renamed-run-19519
Yahaha, you found me! Here is your flag:
pwn.college{ABMxGPyUBLw5UwUGxq2GIzyfa67.QX4IDO0wiM5EzNzEzW}
hacker@commands~listing-files:~$
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

