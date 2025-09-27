# Digesting Documentation

## Searching manuals

You can scroll man pages with the arrow keys (and PgUp/PgDn) and search with /. After searching, you can hit n to go to the next result and N to go to the previous result. Instead of /, you can use ? to search backwards!

Find the option that will give you the flag by reading the challenge man page.

### Solve
**Flag:** pwn.college{ooKLFWyIPoVsHAAk5L1JgbQREwu.QX1EDO0wiNxIzNzEzW}

to search in manual we use / command. now for getting flag we did / flag and then got --exkmvha as command which gives flag.

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --exkmvha
Initializing...
Correct usage! Your flag: pwn.college{ooKLFWyIPoVsHAAk5L1JgbQREwu.QX1EDO0wiNxIzNzEzW}
Your flag: pwn.college{ooKLFWyIPoVsHAAk5L1JgbQREwu.QX1EDO0wiNxIzNzEzW}
```

### New Learnings
/ used to search in man. n to go to next search N to go to previous result. ? to search backwards

### References 
N.A.
