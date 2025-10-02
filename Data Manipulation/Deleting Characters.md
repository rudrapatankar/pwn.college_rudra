# Data Manipulation

## Deleting Characters

tr can also translate characters to nothing (i.e., delete them). This is done via a -d flag and an argument of what characters to delete:

hacker@dojo:~$ echo PAWN | tr -d A
PWN
hacker@dojo:~$
Pretty simple! Now you give it a try. I'll intersperse some decoy characters (specifically: ^ and %) among the flag characters. Use tr -d to remove them!

### Solve
**Flag:** pwn.college{o2t5HpTJ-cEi4V8EgsCWOKTVaFs.0FNxEzNxwiNxIzNzEzW}

To remove the decoy characters from the flag specifically % and * then using tr -d we can do it.

```bash
hacker@data~deleting-characters:~$ /challenge/run | tr -d "%^"
Your character-stuffed flag:
pwn.college{o2t5HpTJ-cEi4V8EgsCWOKTVaFs.0FNxEzNxwiNxIzNzEzW}

```

### New Learnings
To remove the decoy characters from the flag specifically % and * then using tr -d we can do it.

### References 
N.A.
