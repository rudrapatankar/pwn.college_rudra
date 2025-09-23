# Pondering Paths

## Explicit relative path from /

Previously, your relative path was "naked": it directly specified the directory to descend into from the current directory. In this level, we're going to explore more explicit relative paths.

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: . and ... The first, ., refers right to the same directory, so the following absolute paths are all identical to each other:

/challenge
/challenge/.
/challenge/./././././././././
/./././challenge/././
The following relative paths are also all identical to each other:

challenge
./challenge
./././challenge
challenge/.
Of course, if your current working directory is /, the above relative paths are equivalent to the above absolute paths.

This challenge will get you using . in your relative paths.

### Solve
**Flag:** `pwn.college{AcUb1FwxFlCzlP-iyPvnwcheOZu.QXwUTN0wiNxIzNzEzW}

Here we are using '.' type of relative paths instead of standard relative path. eg : instead of challenge/run we do ./challenge/run

```bash
/challenge/run
cd /
./challenge/run
pwn.college{AcUb1FwxFlCzlP-iyPvnwcheOZu.QXwUTN0wiNxIzNzEzW}
```

### New Learnings
Learn new relative paths apart from challenge/run

### References 
N.A.
