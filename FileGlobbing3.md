# File Globbing

## Matching with []

Globbing happens on a path basis, so you can expand entire paths with your globbed arguments. For example:

hacker@dojo:~$ touch file_a
hacker@dojo:~$ touch file_b
hacker@dojo:~$ touch file_c
hacker@dojo:~$ ls
file_a	file_b	file_c
hacker@dojo:~$ echo Look: /home/hacker/file_[ab]
Look: /home/hacker/file_a /home/hacker/file_b
Now it's your turn. Once more, we've placed a bunch of files in /challenge/files. Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!

### Solve
**Flag:** `pwn.college{0Ga8lMj81yQG06-Cnq7dxWXBg3y.QXzIDO0wiNxIzNzEzW}`

change directory to /challenge/files then just run /challenge/run file_[name1name2....]

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ file_[bash]
bash: file_a: command not found
hacker@globbing~matching-with-:/challenge/files$ echo Look : file_[bash]
Look : file_a file_b file_h file_s
hacker@globbing~matching-with-:/challenge/files$ /challenge/run
Error: you did not use a square bracket glob...
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file[bash]
Your expansion did not expand to the requested files (file_a, file_b, file_h,
and file_s). Instead, it expanded to:
file[bash]
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
pwn.college{0Ga8lMj81yQG06-Cnq7dxWXBg3y.QXzIDO0wiNxIzNzEzW}
```

### New Learnings
we can search multiple files in a single command by just using their names in file_[name1name2...]

### References 
N.A
