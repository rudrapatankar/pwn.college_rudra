# Untangling Users

## Other users with su

With no arguments, su will start a root shell (after authenticating with root's password). However, you can also give a username as an argument to switch to that user instead of root. For example:

hacker@dojo:~$ su some-user
Password:
some-user@dojo:~$
Awesome! In this level, you must switch to the zardus user and then run /challenge/run. Zardus' password is dont-hack-me. Good luck!

### Solve
**Flag:** pwn.college{UkLaZe8r7loD2tAv6djnXiTaN7q.QX2UDN1wiNxIzNzEzW}

su zardus changes root to zardus user then entering password we become zardus user then /challenge/run gives us flag.

```bash
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{UkLaZe8r7loD2tAv6djnXiTaN7q.QX2UDN1wiNxIzNzEzW}
```

### New Learnings
su zardus changes root to zardus user
### References 
N.A.
