# File Globbing

## Matching paths with []

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
**Flag:** pwn.college{03CowKf7d8opZf0zBwpm1MPXpQa.QX0IDO0wiNxIzNzEzW}

put file_ command in the address of the /challenge/files then run using /challenge/run

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
pwn.college{03CowKf7d8opZf0zBwpm1MPXpQa.QX0IDO0wiNxIzNzEzW}
```

### New Learnings
You can use search of file that is file_ in address as well

### References 
Add any references or videos you used while solving the challenge.
