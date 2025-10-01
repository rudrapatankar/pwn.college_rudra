# Comprehending Commands

##Removing files
Files are all around you. Like candy wrappers, there'll eventually be too many of them. In this level, we'll learn to clean up!

In Linux, you remove files with the rm command, as so:

hacker@dojo:~$ touch PWN
hacker@dojo:~$ touch COLLEGE
hacker@dojo:~$ ls
COLLEGE     PWN
hacker@dojo:~$ rm PWN
hacker@dojo:~$ ls
COLLEGE
hacker@dojo:~$
Let's practice. This challenge will create a delete_me file in your home directory! Delete it, then run /challenge/check, which will make sure you've deleted it and then give you the flag!
### Solve
**Flag:** pwn.college{w7DCPzCKWVKsmTxaPvCAipLrvmy.QX2kDM1wiNxIzNzEzW}

To remove the file 'delete_me' from '~' directory which is the default directory. do rm delete_me



```bash
rm delete_me
/challenge/check
pwn.college{w7DCPzCKWVKsmTxaPvCAipLrvmy.QX2kDM1wiNxIzNzEzW}
```

### New Learnings
rm command used to remove files

### References 
N.A.
