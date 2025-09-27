# Pondering Paths
## My solve
### Challenge 1:The Root
**Flag:** `pwn.college{0qNI3fSqodXfj9DOUleQ6GrTRck.QX4cTO0wiM5EzNzEzW}`
/ is the root directory.

### Challenge 2: Program and absolute paths
**Flag:** `pwn.college{IOXmAD87HMZK1dfP-L545Zn3eY2.QX1QTN0wiM5EzNzEzW}`
Any path starting with / is called an absolute path.
```bash
hacker@commands~catting-absolute-paths:~$ /challenge/run
pwn.college{IOXmAD87HMZK1dfP-L545Zn3eY2.QX1QTN0wiM5EzNzEzW}
```

### Challenge 3: Position thy self
**Flag:** `pwn.college{ALZkqNhH80-TxCF5Z7bf9B5boXL.QX2QTN0wiM5EzNzEzW}`
cd is used to change directory or current location.
```bash
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```

### Challenge 4: Position elsewhere
**Flag:** `pwn.college{kxG4z41elNULr5SfKu8dijdrEhb.QX3QTN0wiM5EzNzEzW}`

Another example of previous understanding.
```bash
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```

### Challenge 5: Position yet elsewhere
**Flag:** `pwn.college{Axxos208gkTsNHCGQWn9nzN2RBW.QX4QTN0wiM5EzNzEzW}`

### Challenge 6: implicit relative paths from /
**Flag:** `pwn.college{k6eXP_EXTbzwM_UETOuiOk5NyTf.QX5QTN0wiM5EzNzEzW}`
Depending on our location we can access any file example
<br>Imagine we want to access some file located at /tmp/a/b/my_file.
<br>
If my cwd is /, then a relative path to the file is tmp/a/b/my_file.<br>
If my cwd is /tmp, then a relative path to the file is a/b/my_file.

### Challenge 7: explicit relative paths, from /
**Flag:** `pwn.college{4lssgf_MZRwZacyboybB5crKSlK.QXwUTN0wiM5EzNzEzW}`
"." is used to say that we are in the same directory. <br>Example<br> /challenge
<br>/challenge/.<br> both are same.
```bash
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{0x2g_j5tSzFEmUQgQA9iVzUNpPD.QXwMDO0wiM5EzNzEzW}
hacker@commands~touching-files:/tmp$
```

### Challenge 8: implicit relative path
**Flag:** `pwn.college{Qnssht1rbwHoReGX8NqAg7lUHWM.QXxUTN0wiM5EzNzEzW}`
some times linux explicitly avoid automatically looking in the current directory when we provide "naked" path. So we write it as
```bash
hacker@dojo:~$ cd /challenge
hacker@dojo:/challenge$ ./run
```

### Challenge 9: home sweet home
**Flag:** `pwn.college{EKTwIHDgExekuOhe-GI0zuWlX-w.QXzMDO0wiM5EzNzEzW}`
~ is a short hand for /home/hacker
```bash
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{EKTwIHDgExekuOhe-GI0zuWlX-w.QXzMDO0wiM5EzNzEzW}
```
## What I learned
In this module I learned that linus file storing system is like a tree and how directories and files are organised.
I also learned differnt paths to mention a file and how to access them.
## References 
The video provided in the module.

