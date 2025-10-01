# Comprehending Commands

## More catting practice

You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with cd, so no cat flag for you. You must retrieve the flag by absolute path, wherever it is.

### Solve
**Flag:** pwn.college{kAiRcNDztRy4JyIZ0uYmw05vKj5.QXwITO0wiNxIzNzEzW}

if we use absolute path '/lib/apt/flag' with cat. Then we can directly direct to the required lib  

```bash
cat /lib/apt/flag
pwn.college{kAiRcNDztRy4JyIZ0uYmw05vKj5.QXwITO0wiNxIzNzEzW}
```

### New Learnings
We can directly open file using absolute path located in different directory.

### References 
N.A.