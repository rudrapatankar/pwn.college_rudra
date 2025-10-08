# Perceiving Permissions

## The Suid Bit

The easiest way to chain commands is ;. In most contexts, ; separates commands in a similar way to how Enter separates lines. So, this:

hacker@dojo:~$ echo COLLEGE > pwn
hacker@dojo:~$ cat pwn
COLLEGE
hacker@dojo:~$
Is roughly the same as this:

hacker@dojo:~$ echo COLLEGE > pwn; cat pwn
COLLEGE
hacker@dojo:~$
Basically, when you hit Enter, your shell executes your typed command and, after that command terminates, gives you the prompt to input another command. The semicolon is analogous, just without the prompt and with you entering both commands before anything is executed.

Give it a try now! In this level, you must run /challenge/pwn and then /challenge/college, chaining them with a semicolon.

### Solve
**Flag:** pwn.college{MklONl8IwkWjK7fV1YZOgRt8J_e.QXzEjN0wiNxIzNzEzW}

first changing permissions of /challenge/getroot doing suid using s operator and then run flag using cat /flag as suid bit gets set on the program

```bash
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root!
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{MklONl8IwkWjK7fV1YZOgRt8J_e.QXzEjN0wiNxIzNzEzW}
```

### New Learnings
first changing permissions of /challenge/getroot doing suid using s operator and then run flag using cat /flag as suid bit gets set on the program


### References 
N.A.
