# Terminal Multiplexing

## Detaching and Attaching

Now we'll start digging in with the magic of detaching!

Imagine you're working on something important over a remote connection, and your connection drops. With a normal terminal (outside of this awesome dojo environment), everything's gone. With screen, your work keeps running, and you can reattach later!

You can also detach on purpose, which we'll do in this challenge. You detach by pressing Ctrl-A, followed by d (for detach). This leaves your session running in the background while you return to your normal terminal.

hacker@dojo:~$ screen
[doing some work...]
[Press Ctrl-A, then d]
[detached from 12345.pts-0.hostname]
hacker@dojo:~$ 
To reattach, you can use the -r argument to screen:

hacker@dojo:~$ screen -r
For this challenge, you'll need to:

Launch screen
Detach from it.
Run /challenge/run (this will secretly send the flag to your detached session!)
Reattach to see your prize
FUN FACT: Ctrl-A is screen's activation key for all of its shortcuts in its default configuration. All screen functionality is activated by some command combination starting with Ctrl-A.

HINT: Remember: Hold Ctrl and press A, then release both and press d.

HINT: If you see [detached from...], you did it right!

### Solve
**Flag:** pwn.college{AwvS40wKH_uUjWCUIxfK74bLTzI.0lN4IDOxwiNxIzNzEzW}

Detaching of screen do ctrl-A +d then /challenge/run, reattaching do screen -r

```bash
screen
ctrl-A +d
/challenge/run
screen -r
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{AwvS40wKH_uUjWCUIxfK74bLTzI.0lN4IDOxwiNxIzNzEzW}
Yes! Flag is: pwn.college{AwvS40wKH_uUjWCUIxfK74bLTzI.0lN4IDOxwiNxIzNzEzW}
```

### New Learnings
Detaching of screen do ctrl-A +d reattaching do screen -r

### References 
N.A.
