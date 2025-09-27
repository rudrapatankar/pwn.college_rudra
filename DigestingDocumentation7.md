# Digesting Documentation

## Help for bulletins

Some commands, rather than being programs with man pages and help options, are built into the shell itself. These are called builtins. Builtins are invoked just like commands, but the shell handles them internally instead of launching other programs. You can get a list of shell builtins by running the builtin help, as so:

hacker@dojo:~$ help
You can get help on a specific one by passing it to the help builtin. Let's look at a builtin that we've already used earlier, cd!

hacker@dojo:~$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.
    
    Change the current directory to DIR.  The default DIR is the value of the
    HOME shell variable.
...
Some good information! In this challenge, we'll practice using help to look up help for builtins. This challenge's challenge command is a shell builtin, rather than a program. Like before, you need to lookup its help to figure out the secret value to pass to it!

### Solve
**Flag:** pwn.college{w7f_TPxt4-7zuL7Loi1D7r5_67W.QX0ETO0wiNxIzNzEzW}

help challenge gives required list of commands. then doing challenge --secret VALUE and put VALUE as w7f_TPxt gives necessary flag

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "w7f_TPxt".
hacker@man~help-for-builtins:~$ /challenge/challenge  --secret^C
hacker@man~help-for-builtins:~$ /challenge/challenge  --secret w7f_TPxt
bash: /challenge/challenge: No such file or directory
hacker@man~help-for-builtins:~$ /challenge --secret w7f_TPxt
bash: /challenge: Is a directory
hacker@man~help-for-builtins:~$ challenge --secret w7f_TPxt
Correct! Here is your flag!
pwn.college{w7f_TPxt4-7zuL7Loi1D7r5_67W.QX0ETO0wiNxIzNzEzW}
pwn.college{w7f_TPxt4-7zuL7Loi1D7r5_67W.QX0ETO0wiNxIzNzEzW}
```

### New Learnings
Brief note on what you learned from the challenge

### References 
Add any references or videos you used while solving the challenge.
