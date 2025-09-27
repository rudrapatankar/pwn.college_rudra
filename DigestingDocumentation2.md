# Digesting Documentation

## Learning Complex Usage

While using most commands is straightforward, the usage of some commands can get quite complex. For example, the arguments to commands like sed and awk, which we're definitely not getting into right now, are entire programs in an esoteric programming language! Somewhere on the spectrum between cd and awk are commands that take arguments to their arguments...

This sounds crazy, but you've already encountered this with the find level in Basic Commands. find has a -name argument, and the -name argument itself takes an argument specifying the name to search for. Many other commands are analogous.

Here is this level's documentation for /challenge/challenge:

Welcome to the documentation for /challenge/challenge! This program allows you to print arbitrary files to the terminal, when given the --printfile argument. The argument to the --printfile argument is the path of the flag to read. For example, /challenge/challenge --printfile /challenge/DESCRIPTION.md will print out the description of the level!

Given that documentation, go get the flag!

### Solve
**Flag:**pwn.college{EzYASHfCSrNLCSD21DnN6zymmnB.QX1ITO0wiNxIzNzEzW}

here to print a file from /challenge/challenge directory instead of cat we do /challenge/challenge --printfile /flag

```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{EzYASHfCSrNLCSD21DnN6zymmnB.QX1ITO0wiNxIzNzEzW}
pwn.college{EzYASHfCSrNLCSD21DnN6zymmnB.QX1ITO0wiNxIzNzEzW}

```

### New Learnings
we can also print the content of file without using cat using --printfile function

### References 
N.A.
