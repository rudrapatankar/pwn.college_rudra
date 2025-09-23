#Pondering Paths

## Implicit relative paths from /.

Imagine we want to access some file located at /tmp/a/b/my_file.

If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
If my cwd is /tmp, then a relative path to the file is a/b/my_file.
If my cwd is /tmp/a/b/c, then a relative path to the file is ../my_file. The .. refers to the parent directory.
Let's try it here! You'll need to run /challenge/run using a relative path while having a current working directory of /. For this level, I'll give you a hint. Your relative path starts with the letter c

### Solve
**Flag:** pwn.college{0S7xXYs2R0b_wrPnMs8qBTEujkO.QX5QTN0wiNxIzNzEzW}

run /challenge/run as usual, gives us the address of directory / . Now after doing cd / ,  we have to do challenge/run without previous / as we are using relative path and not absolute path

```bash
/challenge/run
cd /
challenge/run
pwn.college{0S7xXYs2R0b_wrPnMs8qBTEujkO.QX5QTN0wiNxIzNzEzW}
```

### New Learnings
Understood the difference between absolute and relative paths. Absolute path we use /challenge/run and in relative challenge/run

### References 
N.A.