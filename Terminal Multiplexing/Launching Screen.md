# Terminal Multiplexing

## Launching Screen
Let's dive right in!

screen is a program that creates virtual terminals inside your terminal. It's somewhat like having multiple browser tabs, but for your command line!

Starting screen is super simple:

hacker@dojo:~$ screen
That's it! You're now inside a screen session. It looks exactly like a terminal, but there are new capabilities there, waiting to be discovered.

For this challenge, we've hooked things up so that just launching screen will get you the flag. Easy!

NOTE: When you're done with your command line, type exit or press Ctrl-D to leave the screen session. Then screen will terminate and return you to your original shell.

### Solve
**Flag:** pwn.college{EKbMq9aJHHkC9Y0SMcZV6i-RU1c.0VN4IDOxwiNxIzNzEzW}

run screen to start screen program then to exit and get flag type in exit.

```bash
screen
pwn.college{EKbMq9aJHHkC9Y0SMcZV6i-RU1c.0VN4IDOxwiNxIzNzEzW}
```

### New Learnings
To start screen program we need to enter just **screen**

### References 
N.A.
