# File Globbing 

## Tab completion on commands

Tab completion is for more than files! You can also tab-complete commands. This level has a command that starts with pwncollege, and it'll give you the flag. Type pwncollege and hit the tab key to auto-complete it!

NOTE: You can auto-complete any command, but be careful: callous auto-completes without double-checking the result can wreak havoc in your shell if you accidentally run the wrong commands!

### Solve
**Flag:** pwn.college{8MS8xzML1lAFk7sDA6EkXNiFUfB.0VN0EzNxwiNxIzNzEzW}

type in pwncollege and then tab key to get full command then enter and get flag

```bash
hacker@globbing~tab-completion-on-commands:~$ pwn
pwn               pwncollege-16141  pwndbg            pwnstrip          pwntools-gdb
hacker@globbing~tab-completion-on-commands:~$ pwncolleg-16141
bash: pwncolleg-16141: command not found
hacker@globbing~tab-completion-on-commands:~$ cat /pwncolleg-16141
cat: /pwncolleg-16141: No such file or directory
hacker@globbing~tab-completion-on-commands:~$ cat /pwncollege
cat: /pwncollege: No such file or directory
hacker@globbing~tab-completion-on-commands:~$ pwncollege-16141
pwn.college{8MS8xzML1lAFk7sDA6EkXNiFUfB.0VN0EzNxwiNxIzNzEzW}
```

### New Learnings
we can not only use to complete file names but also command names


### References 
N.A.
