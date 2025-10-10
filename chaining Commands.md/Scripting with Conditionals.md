# Chaining Commands

## Scripting with Conditionals

Now that you can use arguments in scripts, let's make them smarter with conditional logic!

In bash, you can use if statements to make decisions:

if [ "$1" == "ping" ]
then
    echo "pong"
fi
The above, in English, is if the first argument is "ping", print out "pong". The syntax is somewhat unforgiving for a few reasons. First, you must have spaces after if (if you're used to a language like C, this is different), after [, and before ]. Second, if, then, and fi must all be on different lines (or separated by semicolons); you can't lump them into the same statement. It's also a bit weird: instead of endif or end or something like that, the terminator of the if statement is fi (if backwards). Just something you have to remember.

For this challenge, write a script at /home/hacker/solve.sh that:

Takes one argument
If the argument is "pwn", output "college"
For any other input, output nothing
Example:

hacker@dojo:~$ bash /home/hacker/solve.sh pwn
college
hacker@dojo:~$ bash /home/hacker/solve.sh foo
hacker@dojo:~$
Once your script works correctly, run /challenge/run to get your flag!

NOTE: Interested in what else you can check in a condition, other than string equality? Read all about it with help test!

### Solve
**Flag:** pwn.college{wCIDPZMk8VwmIkt5fK_Kw2jMBKe.0lNzMDOxwiNxIzNzEzW}

using if [condition] we can print some desired output based on the arguments passed 

```bash
hacker@chaining~scripting-with-conditionals:~$ cat > /home/hacker/solve.sh <<'EOF'
#!/bin/bash
if [ "$1" = "pwn" ]; then
  printf '%s\n' "college"
fi
EOF
hacker@chaining~scripting-with-conditionals:~$ chmod +x /home/hacker/solve.sh
hacker@chaining~scripting-with-conditionals:~$ /challenge/run
Correct! Your script properly handles all the conditions.
Here's your flag:
pwn.college{wCIDPZMk8VwmIkt5fK_Kw2jMBKe.0lNzMDOxwiNxIzNzEzW}
```

### New Learnings
using if [condition] we can print some desired output based on the arguments passed

### References 
N.A.
