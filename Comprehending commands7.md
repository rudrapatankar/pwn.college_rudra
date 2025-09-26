# Comprehending Commands

##Touching files

Of course, you can also create files! There are several ways to do this, but we'll look at a simple command here. You can create a new, blank file by touching it with the touch command:

hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ touch pwnfile
hacker@dojo:/tmp$ ls
pwnfile
hacker@dojo:/tmp$
It's that simple! In this level, please create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get your flag!

### Solve
**Flag:** pwn.college{w_6aVcATPuJObI9QMX3hcXVCziP.QXwMDO0wiNxIzNzEzW}

To create two files in /tmp directory using touch command, first change directory from '~' to '/tmp' using cd command. Then use touch command for pwn and college and then running /challenge/run gives required flag


```bash
cd /tmp
touch pwn
touch college
/challenge/run
pwn.college{w_6aVcATPuJObI9QMX3hcXVCziP.QXwMDO0wiNxIzNzEzW}
```

### New Learnings
touch command is used to create new blank files

### References 
N.A.
