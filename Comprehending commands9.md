# Comprehending Commands

##moving files
You can also move files around with the mv command. The usage is simple:

hacker@dojo:~$ ls
my-file
hacker@dojo:~$ cat my-file
PWN!
hacker@dojo:~$ mv my-file your-file
hacker@dojo:~$ ls
your-file
hacker@dojo:~$ cat your-file
PWN!
hacker@dojo:~$
This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.You can also move files around with the mv command. The usage is simple:

hacker@dojo:~$ ls
my-file
hacker@dojo:~$ cat my-file
PWN!
hacker@dojo:~$ mv my-file your-file
hacker@dojo:~$ ls
your-file
hacker@dojo:~$ cat your-file
PWN!
hacker@dojo:~$
This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.

**Flag:** pwn.college{cS0F6nUY_QfaD6a15yn_Bdnu7wa.0VOxEzNxwiNxIzNzEzW}

To move a file to a certain address do mv filename address



```bash
mv  /flag /tmp/hack-the-planet
/challenge/check
pwn.college{cS0F6nUY_QfaD6a15yn_Bdnu7wa.0VOxEzNxwiNxIzNzEzW}
```

### New Learnings
mv command is used to move files to a specific address

### References 
N.A.
