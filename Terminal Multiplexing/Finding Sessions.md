# Terminal Multiplexing

## Finding Sessions

Time for some screen detective work!

If you become an avid screen user, you will inevitably end up with multiple sessions running. How do you find the right one to reattach to?

Well, we can list them:

hacker@dojo:~$ screen -ls
There are screens on:
        23847.mysession   (Detached)
        23851.goodwork    (Detached)
        23855.morework    (Detached)
3 Sockets in /run/screen/S-hacker.
The identifiers of the sessions are the PID of each respective screen process, a dot, and the name of the screen session. To attach to a specific one, you use its name or its PID by giving it as an argument to screen -r.

hacker@dojo:~$ screen -r goodwork
In this challenge, we've created three screen sessions for you. One of them contains the flag. The other two are decoys!

You'll need to check each one until you find it. Don't forget to detach (Ctrl-A d) before trying the next session!

### Solve
**Flag:** pwn.college{QFQTtMPoIm0RTqvHMRzU6_fh6p4.01N4IDOxwiNxIzNzEzW}

first see list of sessions in screen program using screen -ls then do reattaching as one of the programs contains flag

```bash
screen -ls
screen -r ""
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'
Congratulations! You found the right session!
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{QFQTtMPoIm0RTqvHMRzU6_fh6p4.01N4IDOxwiNxIzNzEzW}
pwn.college{QFQTtMPoIm0RTqvHMRzU6_fh6p4.01N4IDOxwiNxIzNzEzW}
```

### New Learnings
screen -ls lists down all deattached and running sessions of screen program

### References 
N.A.
