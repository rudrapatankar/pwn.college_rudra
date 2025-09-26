# Comprehending Commands

##hidden files

Interestingly, ls doesn't list all the files by default. Linux has a convention where files that start with a . don't show up by default in ls and in a few other contexts. To view them with ls, you need to invoke ls with the -a flag, as so:

hacker@dojo:~$ touch pwn
hacker@dojo:~$ touch .college
hacker@dojo:~$ ls
pwn
hacker@dojo:~$ ls -a
.college	pwn
hacker@dojo:~$
Now, it's your turn! Go find the flag, hidden as a dot-prepended file in /.

**Flag:** pwn.college{YrYH6rVhevN6TaUFggHqz0i95R_.QXwUDO0wiNxIzNzEzW}

To fetch list of files including the hidden ones do ls -a and then open the flag file using cat



```bash
ls -a
cat /.flag-26845651413294
pwn.college{YrYH6rVhevN6TaUFggHqz0i95R_.QXwUDO0wiNxIzNzEzW}
```

### New Learnings
ls -a command used to display all hidden and non-hidden files

### References 
N.A.
