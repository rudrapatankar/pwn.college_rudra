# Shell Variables

## Printing Variables

Let's start with printing variables out. The /challenge/run program will not, and cannot, give you the flag, but that's okay, because the flag has been put into the variable called "FLAG"! Just have your shell print it out!

You can accomplish this using a number of ways, but we'll start with echo. This command just prints stuff. For example:

hacker@dojo:~$ echo Hello Hackers!
Hello Hackers!
You can also print out variables with echo, by prepending the variable name with a $. For example, there is a variable, PWD, that always holds the current working directory of the current shell. You print it out as so:

hacker@dojo:~$ echo $PWD
/home/hacker
Now it's your turn. Have your shell print out the FLAG variable and solve this challenge!

### Solve
**Flag:** pwn.college{c_NWranM9A01F44uD1kA7q0J_Xf.QX3UTN0wiNxIzNzEzW}

to print value from file use $ operator with echo command echo $variablename

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{c_NWranM9A01F44uD1kA7q0J_Xf.QX3UTN0wiNxIzNzEzW}
```

### New Learnings
to print value from file use $ operator with echo command echo $variablename


### References 
N.A.
