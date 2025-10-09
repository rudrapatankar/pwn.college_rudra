# Chaining Commands

## Redirecting Script Output

Let's try something a bit trickier! You've piped output between programs with |, but so far, this has just been between one command's output and a different command's input. But what if you wanted to send the output of several programs to one command? There are a few ways to do this, and we'll explore a simple one here: redirecting output from your script!

As far as the shell is concerned, your script is just another command. That means you can redirect its input and output just like you did for commands in the Piping module! For example, you can write it to a file:

hacker@dojo:~$ cat script.sh
echo PWN
echo COLLEGE
hacker@dojo:~$ bash script.sh > output
hacker@dojo:~$ cat output
PWN
COLLEGE
hacker@dojo:~$
All of the various redirection methods work: > for stdout, 2> for stderr, < for stdin, >> and 2>> for append-mode redirection, >& for redirecting to other file descriptors, and | for piping to another command.

In this level, we will practice piping (|) from your script to another program. Like before, you need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command!Let's try something a bit trickier! You've piped output between programs with |, but so far, this has just been between one command's output and a different command's input. But what if you wanted to send the output of several programs to one command? There are a few ways to do this, and we'll explore a simple one here: redirecting output from your script!

As far as the shell is concerned, your script is just another command. That means you can redirect its input and output just like you did for commands in the Piping module! For example, you can write it to a file:

hacker@dojo:~$ cat script.sh
echo PWN
echo COLLEGE
hacker@dojo:~$ bash script.sh > output
hacker@dojo:~$ cat output
PWN
COLLEGE
hacker@dojo:~$
All of the various redirection methods work: > for stdout, 2> for stderr, < for stdin, >> and 2>> for append-mode redirection, >& for redirecting to other file descriptors, and | for piping to another command.

In this level, we will practice piping (|) from your script to another program. Like before, you need to create a script that calls the /challenge/pwn command followed by the /challenge/college command, and pipe the output of the script into a single invocation of the /challenge/solve command!

### Solve
**Flag:** pwn.college{4OY6MiA3Ux2n92iQY9fYOTbUh2z.QX4ETO0wiNxIzNzEzW}

Doin nano create run_both shell then put in the /challenge/pwn and /challenge/college in the shell then give execution access to all then ./run_both.sh | /challenge/solve for stdout
& ./run_both.sh 2>&1 | /challenge/solve for stdout


```bash
hacker@chaining~redirecting-script-output:~$ nano run_both.sh
hacker@chaining~redirecting-script-output:~$ chmod +x run_both.sh
# pipe stdout only:
./run_both.sh | /challenge/solve

# or, if /challenge/solve needs stderr too:
./run_both.sh 2>&1 | /challenge/solve
./run_both.sh: /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/share/bashdb/bashdb-main.inc: No such file or directory
./run_both.sh: warning: cannot start debugger; debugging mode disabled
Correct! Here is your flag:
pwn.college{4OY6MiA3Ux2n92iQY9fYOTbUh2z.QX4ETO0wiNxIzNzEzW}
```

### New Learnings
for creating shell use nano command. For running stdout do ./run_nameofshell.sh | command and stderr do ./run_shellname.sh 2>&1 | command

### References 
N.A.
