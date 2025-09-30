# Module Name

## Split-piping stderr and stdout

Now, let's put your knowledge together. You must master the ultimate piping task: redirect stdout to one program and stderr to another.

The challenge here, of course, is that the | operator links the stdout of the left command with the stdin of the right command. Of course, you've used 2>&1 to redirect stderr into stdout and, thus, pipe stderr over, but this then mixes stderr and stdout. How to keep it unmixed?

You will need to combine your knowledge of >(), 2>, and |. How to do it is a task I'll leave to you.

In this challenge, you have:

/challenge/hack: this produces data on stdout and stderr
/challenge/the: you must redirect hack's stderr to this program
/challenge/planet: you must redirect hack's stdout to this program

### Solve
**Flag:** `pwn.college{helloworld}`

store standard output in /challenge/planet so use only > and for standard error use 2> to store it in /challenge/the.

```bash
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >( /challenge/the ) | /challenge/planet
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{YxJTP4MVc8cziSvr_HyBzULyVzu.QXxQDM2wiNxIzNzEzW}

```

### New Learning
How to pipe the standard output and error into another file

### References 
N.A.
