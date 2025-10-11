# Terminal Multiplexing

## Switching Windows

Let's learn to navigate windows in tmux!

Just like screen, tmux has windows. The key combos are different, but the concept is the same:

Ctrl-B c - Create a new window
Ctrl-B n - Next window
Ctrl-B p - Previous window
Ctrl-B 0 through Ctrl-B 9 - Jump to window 0-9
Ctrl-B w - See a nice window picker
Tmux shows your windows at the bottom in a status bar that looks like:

[0] 0:bash* 1:bash
The * shows your current window, and each entry also shows the process that the window was created to run.

We've created a tmux session with two windows:

Window 0 has the flag!
Window 1 has your warm welcome.
Go get that flag!

### Solve
**Flag:** pwn.college{0WMWXwIUVm3WkIXRIcW1GpMdN7a.0FM5IDOxwiNxIzNzEzW}

tmux a then do ctrlB+0 to go to window 0 as it is told in the welcome message that flag is in window 0.

```bash
tmux a
ctrlB +0
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG
> Excellent work! You found window 0!
> Here is your flag: pwn.college{0WMWXwIUVm3WkIXRIcW1GpMdN7a.0FM5IDOxwiNxIzNzEzW}
> MSG
Excellent work! You found window 0!
Here is your flag: pwn.college{0WMWXwIUVm3WkIXRIcW1GpMdN7a.0FM5IDOxwiNxIzNzEzW}
```

### New Learnings
ctrlB + number we can switch to that particular window 

### References 
N.A.
