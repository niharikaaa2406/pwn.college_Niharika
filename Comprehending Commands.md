# Comprehending Commands
type what the challenge asks

## My solve
### Challenge 1: cat:not the pet, but the command
**Flag:** `pwn.college{8fmktiP2a5cG7eJuMAeu9tQQK8v.QXxcTN0wiM5EzNzEzW}`

Explain how you arrived at the solution and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.

```bash
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{8fmktiP2a5cG7eJuMAeu9tQQK8v.QXxcTN0wiM5EzNzEzW}
hacker@commands~cat-not-the-pet-but-the-command:~$
```

### Challenge 2: catting absolute paths
**Flag:** `pwn.college{IeguGJlzXWSmFuV4z75VxgafTS_.QX5ETO0wiM5EzNzEzW}`

Explain how you arrived at the solution and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.

```bash
hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{IeguGJlzXWSmFuV4z75VxgafTS_.QX5ETO0wiM5EzNzEzW}
hacker@commands~catting-absolute-paths:~$
```

### Challenge 3: more catting practice
**Flag:** `pwn.college{4vVibc6gdw_aUP2Qxtpi65C1o0R.QXwITO0wiM5EzNzEzW}`

Explain how you arrived at the solution and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for bash.

```bash
hacker@commands~more-catting-practice:~$ cat /lib/X11/flag
pwn.college{4vVibc6gdw_aUP2Qxtpi65C1o0R.QXwITO0wiM5EzNzEzW}
hacker@commands~more-catting-practice:~$
```

### Challenge 4: grepping for a needle in a haystack
**Flag:** `pwn.college{ggC2CC4vmYScsHKk8g-w8ez5Keu.QX3EDO0wiM5EzNzEzW}`

grep command is used to search for the context we need for times when the files are too big. There are multiple ways to grep.

```bash
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep "pwn.college" /challenge/data.txt
pwn.college{ggC2CC4vmYScsHKk8g-w8ez5Keu.QX3EDO0wiM5EzNzEzW}
```

### Challenge 5: comparing files
**Flag:** `> pwn.college{A8THlHbuTyIZOGFndPvgbNV7UTW.01MwMDOxwiM5EzNzEzW}`

diff command compares two files line by line and shows exactly why they are different. 
<br>
example, 2c2 means line 2 of file one is different from that f file 2<br>
1a2 means after line 1 of file 1 another line is added to line 2 of file 2.


```bash
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
92a93
> pwn.college{A8THlHbuTyIZOGFndPvgbNV7UTW.01MwMDOxwiM5EzNzEzW}
```







## What I learned
Explain what new topics you learned/information you gained through this challenge.








## References 
Add an references or videos you used while solving the challenge.


