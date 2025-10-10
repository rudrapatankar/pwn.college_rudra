# Chaining Commands

## Scripting Arguments

You've learned how to make shell scripts, but so far they've just been lists of commands. Scripts become much more powerful when they can accept arguments! This might look like:

hacker@dojo:~$ bash myscript.sh hello world
The script can access these arguments using special variables:

$1 contains the first argument ("hello")
$2 contains the second argument ("world")
$3 would contain the third argument (if there had been one)
...and so on
Here's a simple example:

hacker@dojo:~$ cat myscript.sh
#!/bin/bash
echo "First argument: $1"
echo "Second argument: $2"
hacker@dojo:~$ bash myscript.sh hello world
First argument: hello
Second argument: world
hacker@dojo:~$
For this challenge, you need to write a script at /home/hacker/solve.sh that:

Takes two arguments
Outputs them in REVERSE order (second argument first, then the first argument)
For example:

hacker@dojo:~$ bash /home/hacker/solve.sh pwn college
college pwn
hacker@dojo:~$
Once your script works correctly, run /challenge/run to get your flag!

### Solve
**Flag:** : pwn.college{YFzrBMge5a4XhyKxHBQjdpCJ0PF.0VNzMDOxwiNxIzNzEzW}

taking arguments as input using $1 or $2 as per no of arguments for printing in bash


```bash
hacker@chaining~scripting-with-arguments:~$ cat > /home/hacker/solve.sh <<'EOF'
#!/bin/bash
printf '%s %s\n' "$2" "$1"
EOF
hacker@chaining~scripting-with-arguments:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~scripting-with-arguments:~$ /challenge/run
Correct! Your script properly reversed the arguments.
Here's your flag:
pwn.college{YFzrBMge5a4XhyKxHBQjdpCJ0PF.0VNzMDOxwiNxIzNzEzW}
```

### New Learnings
taking arguments as input using $1 or $2 as per no of arguments for printing in bash

### References 
N.A.
