# Processes and Jobs

## Killing Process

You've launched processes, you've viewed processes, now you will learn to terminate processes! In Linux, this is done using the aggressively-named kill command. With default options (which is all we'll cover in this level), kill will terminate a process in a way that gives it a chance to get its affairs in order before ceasing to exist.

Let's say you had a pesky sleep process (sleep is a program that simply hangs out for the number of seconds specified on the commandline, in this case, 1337 seconds) that you launched in another terminal, like so:

hacker@dojo:~$ sleep 1337
How do we get rid of it? You use kill to terminate it by passing the process identifier (the PID from ps) as an argument, like so:

hacker@dojo:~$ ps -e | grep sleep
 342 pts/0    00:00:00 sleep
hacker@dojo:~$ kill 342
hacker@dojo:~$ ps -e | grep sleep
hacker@dojo:~$
Now, it's time to terminate your first process! In this challenge, /challenge/run will refuse to run while /challenge/dont_run is running! You must find the dont_run process and kill it. If you fail, pwn.college will disavow all knowledge of your mission. Good luck.

### Solve
**Flag:** pwn.college{gO6gsNHZC5kaIr_sQkIGnh-1XPx.QXyQDO0wiNxIzNzEzW}

As we have to kill the dont_run process before exce\uting /challenge/run to get flag.For killing a process we use kill PIDno. We get PID number by using ps -ef.

```bash
hacker@processes~killing-processes:~$ ps -e | grep dont_run
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 06:40 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-i
root           7       1  0 06:40 ?        00:00:00 /run/dojo/bin/sleep 6h
root         135       1  0 06:40 ?        00:00:00 su -c /challenge/.launcher hacker
hacker       136     135  0 06:40 ?        00:00:00 /challenge/dont_run
hacker       137     136  0 06:40 ?        00:00:00 sleep 6h
hacker       139       0  0 06:41 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/
hacker       145     139  0 06:41 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       156     145  0 06:42 pts/0    00:00:00 ps -ef
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{gO6gsNHZC5kaIr_sQkIGnh-1XPx.QXyQDO0wiNxIzNzEzW}
```

### New Learnings
For killing a process we use kill PIDno.

### References 
N.A.
