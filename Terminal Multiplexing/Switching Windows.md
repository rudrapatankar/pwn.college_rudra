# Terminal Multiplexing

## Switching Windows

Okay, so far, screen is just a weird sort of terminal-with-a-terminal. But it can be much more!

Inside a single screen session, you can have multiple windows, like your browser has multiple tabs. This can be super handy for organizing different tasks!

These windows are handled with different keyboard shortcuts, all starting with Ctrl-A:

Ctrl-A c - Create a new window
Ctrl-A n - Next window
Ctrl-A p - Previous window
Ctrl-A 0 through Ctrl-A 9 - Jump directly to window 0-9
Ctrl-A " - bring up a selection menu of all of the windows
For this challenge, we've set up a screen session with two windows:

Window 0 has... well, you'll have to switch there to find out!
Window 1 has a welcome message
Attach to the session with screen -r, then use one of the key combinations above to switch to Window 1. Go get that flag!

### Solve
**Flag:** pwn.college{4VWIp_rOl_UQ25YDf25U8p_3GzV.0FO4IDOxwiNxIzNzEzW}

doing screen -r gives us welcome message with the clue that flag is hidden in window 0 so doing ctrl-A + 0 gives us the flag

```bash
screen -r 
ctrl-A + 0
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{4VWIp_rOl_UQ25YDf25U8p_3GzV.0FO4IDOxwiNxIzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{4VWIp_rOl_UQ25YDf25U8p_3GzV.0FO4IDOxwiNxIzNzEzW}
```

### New Learnings
doing ctrl-A + number, we can switch to any window number in the session.

### References 
N.A.
