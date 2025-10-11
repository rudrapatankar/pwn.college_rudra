# Processes and Jobs

## Suspending Processes

You have learned to interrupt processes with Ctrl-C, but there are less drastic measures you can use to get your terminal back! You can suspend processes to the background with Ctrl-Z. In this level, we'll explore how this works and, in the next level, we'll figure out how to resume those suspended processes!

This level's run wants to see another copy of itself running and using the same terminal. How? Use the terminal to launch it, then suspend it, then launch another copy while the first is suspended!

### Solve
**Flag:** pwn.college{8f0bqLiV30UQNGBHhadCDkjUes6.QX1QDO0wiNxIzNzEzW}

First launch /challenge/run in 1st terminal then suspend using ctrl+z then launch in second terminal. Therefore you get the flag

```bash
Terminal 1 :
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 07:57 pts/0    00:00:00 bash /challenge/run
root         140     138  0 07:57 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run

Terminal 2:
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 07:57 pts/0    00:00:00 bash /challenge/run
root         167     129  0 07:59 pts/0    00:00:00 bash /challenge/run
root         169     167  0 07:59 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{8f0bqLiV30UQNGBHhadCDkjUes6.QX1QDO0wiNxIzNzEzW}
```

### New Learnings
We can suspend running process using ctrl+z

### References 
N.A.
