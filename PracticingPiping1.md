# Practicing Piping 

## Redirecting Output

First, let's look at redirecting stdout to files. You can accomplish this with the > character, as so:

hacker@dojo:~$ echo hi > asdf
This will redirect the output of echo hi (which will be hi) to the file asdf. You can then use a program such as cat to output this file:

hacker@dojo:~$ cat asdf
hi
In this challenge, you must use this output redirection to write the word PWN (all uppercase) to the filename COLLEGE (all uppercase).

### Solve
**Flag:** pwn.college{UBNVUYAtzhFTolcX3Ioz5wixBzq.QX0YTN0wiNxIzNzEzW}

In this we redirect the argument of echo to specified file 

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
pwn.college{UBNVUYAtzhFTolcX3Ioz5wixBzq.QX0YTN0wiNxIzNzEzW}
```

### New Learnings
> is used to redirect the argument of echo into specified file name

### References 
N.A.
