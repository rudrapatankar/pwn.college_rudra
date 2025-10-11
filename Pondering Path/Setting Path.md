# Pondering Path

## Setting Path

Okay, so things break when you blank out PATH. But what about doing something useful with PATH?

Let's explore how we would, for example, add a new directory of programs to our command repertoire. Recall that PATH stores a list of directories to find commands in and, for commands in nonstandard places, we must typically execute them via their path:

hacker@dojo:~$ ls /home/hacker/scripts
goodscript	badscript	okayscript
hacker@dojo:~$ goodscript
bash: goodscript: command not found
hacker@dojo:~$ /home/hacker/scripts/goodscript
YEAH! This is the best script!
hacker@dojo:~$
If you maintain useful scripts that you want to be able to launch by bare name, this is annoying. However, by adding directories to or replacing directories in this list, you can expose these programs to be launched using their bare name! For example:

hacker@dojo:~$ PATH=/home/hacker/scripts
hacker@dojo:~$ goodscript
YEAH! This is the best script!
hacker@dojo:~$
Let's practice. This level's /challenge/run will run the win command via its bare name, but this command exists in the /challenge/more_commands/ directory, which is not initially in the PATH. The win command is the only thing that /challenge/run needs, so you can just overwrite PATH with that one directory. Good luck!

### Solve
**Flag:** pwn.college{MXbvSYNcKIYgipECUqgvZGdKhyo.QX1cjM1wiNxIzNzEzW}

putting PATH=/challenge/more_commands/ then doing /challenge/run as win command is executed with bare name by /challenge/run therefore specify path earlier only.
```bash
hacker@path~setting-path:~$ PATH = /challenge/more_commands
bash: PATH: command not found
hacker@path~setting-path:~$ PATH=/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{MXbvSYNcKIYgipECUqgvZGdKhyo.QX1cjM1wiNxIzNzEzW}
```

### New Learnings
setting path to useful address helps run command or files with bare name

### References 
N.A.
