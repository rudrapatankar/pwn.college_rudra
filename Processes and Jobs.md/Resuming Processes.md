# Processes and Jobs

## Resuming Processes

Usually, when you suspend processes, you'll want to resume them at some point. Otherwise, why not just terminate them? To resume processes, your shell provides the fg command, a builtin that takes the suspended process, resumes it, and puts it back in the foreground of your terminal.

Go try it out! This challenge's run needs you to suspend it, then resume it. Good luck!

### Solve
**Flag:** pwn.college{kQnYuA_NG1kHGTihPL80ML5-6pO.QX2QDO0wiNxIzNzEzW}

After suspending /challenge/run using ctrl+z, we have to resume it using **fg** command

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{kQnYuA_NG1kHGTihPL80ML5-6pO.QX2QDO0wiNxIzNzEzW}
Don't forget to press Enter to quit me!
```

### New Learnings
Resume a suspended process using **fg** command.

### References 
N.A.
