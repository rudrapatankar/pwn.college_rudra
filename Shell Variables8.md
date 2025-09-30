# Shell Variables

## Reading Files

Often, when shell users want to read a file into an environment variable, they do something like:

hacker@dojo:~$ echo "test" > some_file
hacker@dojo:~$ VAR=$(cat some_file)
hacker@dojo:~$ echo $VAR
test
This works, but it represents what grouchy hackers call a "Useless Use of Cat". That is, running a whole other program just to read the file is a waste. It turns out that you can just use the powers of the shell!

Previously, you read user input into a variable. You've also previously redirected files into command input! Put them together, and you can read files with the shell.

hacker@dojo:~$ echo "test" > some_file
hacker@dojo:~$ read VAR < some_file
hacker@dojo:~$ echo $VAR
test
What happened there? The example redirects some_file into the standard input of read, and so when read reads into VAR, it reads from the file! Now, use that to read /challenge/read_me into the PWN environment variable, and we'll give you the flag! The /challenge/read_me will keep changing, so you'll need to read it right into the PWN variable with one command!

### Solve
**Flag:** `pwn.college{helloworld}`

doing read file < command directly sends the output of command to the file then executes it.

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
pwn.college{MD-FLM9OvgOtNE9DZ71nYmCnnWr.QXwIDO0wiNxIzNzEzW}
```

### New Learnings
doing read file < command directly sends the output of command to the file then executes it.

### References 
N.A.
