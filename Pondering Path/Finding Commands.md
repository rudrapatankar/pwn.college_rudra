# Pondering Path

## Finding Commands

When you type the name of a command, something inside one of the many directories listed in your $PATH variable is what actually gets executed (of course, unless the command is a builtin!). But which file, precisely? You can find out with the aptly-named which command:

hacker@dojo:~$ which cat
/bin/cat
hacker@dojo:~$ /bin/cat /flag
YEAH
hacker@dojo:~$
Mirroring what the shell does when searching for commands, which looks at each directory in $PATH in order and prints the first file it finds whose name matches the argument you passed.

In this challenge, we added a win command somewhere in your $PATH, but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find win (with the which command), and cat the flag out of that directory!

### Solve
**Flag:** pwn.college{IypxbXfjC78-AJkVc3cpmIZmdDF.01NzEzNxwiNxIzNzEzW}

doing which win gives path of win, now we know flag is in same directory as win therefore cat /challenge/paths/7611/flag gives the flag

```bash
hacker@path~finding-commands:~$ which win
/challenge/paths/7611/win
hacker@path~finding-commands:~$ cat /challenge/paths/7611/flag
pwn.college{IypxbXfjC78-AJkVc3cpmIZmdDF.01NzEzNxwiNxIzNzEzW}
```

### New Learnings
which command enables us to locate certain files in directories

### References 
N.A.
