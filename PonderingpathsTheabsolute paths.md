# Pondering paths

## Program and absolute path
challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

### Solve
**Flag:** pwn.college{gKfbfugXYiTgOJrXsWTINjw-7Xc.QX1QTN0wiNxlzNzEzW}

We have to to first invoke the directory 'challenge' so /challenge now we have to play the 'run' challenge from this directory, hence the entire command is '/challenge/run'.

```bash
/challenge/run
pwn.college{gKfbfugXYiTgOJrXsWTINjw-7Xc.QX1QTN0wiNxlzNzEzW}
```

### New Learnings
Puting in absolute paths runs the programs smoothly. The syntax of playing program 'run' from directory 'challenge' is /directory/program.

### References 
N.A.
