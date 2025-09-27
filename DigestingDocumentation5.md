# Digesting Documentation

## Searching for manuals

This level is tricky: it hides the manpage for the challenge by randomizing its name. Luckily, all of the manpages are gathered in a searchable database, so you'll be able to search the man page database to find the hidden challenge man page! To figure out how to search for the right manpage, read the man page manpage by doing: man man!

HINT 1: man man teaches you advanced usage of the man command itself, and you must use this knowledge to figure out how to search for the hidden manpage that will tell you how to use /challenge/challenge

HINT 2: though the manpage is randomly named, you still actually use /challenge/challenge to get the flag!

### Solve
**Flag:** pwn.college{A-QmR09jd8f7MCuLwBGnqL9PWLX.QX2EDO0wiNxIzNzEzW}

man -k/challenge searches for challenge in manual of man. mjdfuwnqwi is the required man of man. Therefore after that we get --mjdfuw NUM command to print flag using 098 as NUM.

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~$ man -k /challenge
mjdfuwnqwi (1)       - print the flag!
hacker@man~searching-for-manuals:~$ man 1 mjdfuwnqwi
hacker@man~searching-for-manuals:~$ /challenge/challenge  --mjdfuw 098
Correct usage! Your flag: pwn.college{A-QmR09jd8f7MCuLwBGnqL9PWLX.QX2EDO0wiNxIzNzEzW}
pwn.college{A-QmR09jd8f7MCuLwBGnqL9PWLX.QX2EDO0wiNxIzNzEzW}
```

### New Learnings
man -k/challenge searches for challenge in manual of man..

### References 
N.A.
