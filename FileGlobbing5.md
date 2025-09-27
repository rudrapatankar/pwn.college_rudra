# File Globbing

## Multiple globs

So far, you've specified one glob at a time, but you can do more! Bash supports the expansion of multiple globs in a single word. For example:

hacker@dojo:~$ cat /*fl*
pwn.college{YEAH}
hacker@dojo:~$
What happens above is that the shell looks for all files in / that start with anything (including nothing), then have an f and an l, and end in anything (including ag, which makes flag).

Now you try it. We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.

### Solve
**Flag:** pwn.college{EFEVFmblm3Q_Chdco0eUear5y6O.0lM3kjNxwiNxIzNzEzW}

as required argument should have 3 characters and have p and two globs so we get argument as *p* or we can do **p as well. now pass it onto /challenge/run after 'cd'ing into /challenge/files

```bash
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run /*p*
Error: your argument is too long! It must be 3 characters or less.
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
pwn.college{EFEVFmblm3Q_Chdco0eUear5y6O.0lM3kjNxwiNxIzNzEzW}
```

### New Learnings
we can better name the file using ** globs

### References 
Add any references or videos you used while solving the challenge.
