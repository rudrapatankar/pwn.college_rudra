# File Globbing 

## Mixing globs

Now, let's put the previous levels together! We put a few happy, but diversely-named files in /challenge/files. Go cd there and, using the globbing you've learned, write a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning"!

### Solve
**Flag:** pwn.college{8wqTbja8t4CoThDUUWjb0x120nF.QX1IDO0wiNxIzNzEzW}

cd to /challenge/files then run /challenge/run [pce]* to get flag

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run *p*c*e
Error: you did not use a square bracket glob...
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [*p*c*e]
Error: your argument is too long! It must be 6 characters or less.
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [pc]
Your expansion did not expand to the requested files (challenging, educational,
pwning). Instead, it expanded to:
[pc]
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]
Your expansion did not expand to the requested files (challenging, educational,
pwning). Instead, it expanded to:
[cep]
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [p*ce]
Your expansion did not expand to the requested files (challenging, educational,
pwning). Instead, it expanded to:
[p*ce]
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [pce]*
pwn.college{8wqTbja8t4CoThDUUWjb0x120nF.QX1IDO0wiNxIzNzEzW}
```

### New Learnings
running /challenge/run [pce]* to run challenge,educational and pwning

### References 
N.A.
