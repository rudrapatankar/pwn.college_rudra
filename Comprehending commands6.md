# Comprehending Commands

## Listing files

So far, we've told you which files to interact with. But directories can have lots of files (and other directories) inside them, and we won't always be here to tell you their names. You'll need to learn to list their contents using the ls command!

ls will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided. Observe:

hacker@dojo:~$ ls /challenge
run
hacker@dojo:~$ ls
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$ ls /home/hacker
Desktop    Downloads  Pictures  Templates
Documents  Music      Public    Videos
hacker@dojo:~$
In this challenge, we've named /challenge/run with some random name! List the files in /challenge to find it.

### Solve
**Flag:** pwn.college{MFTEW8lgaGjgSbNRNuyDW0-P-uH.QX4IDO0wiNxIzNzEzW}

list all files in /challenge directory then run the file without .md .

```bash
hacker@commands~listing-files:~$ ls /challenge
14286-renamed-run-27317  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/14286-renamed-run-27317
Yahaha, you found me! Here is your flag:
pwn.college{MFTEW8lgaGjgSbNRNuyDW0-P-uH.QX4IDO0wiNxIzNzEzW}
```

### New Learnings
We can have a whole list of non hidden files using ls /directoryname

### References 
N.A.
