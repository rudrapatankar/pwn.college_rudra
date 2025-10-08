# Chaining Commands

## Building on Success

You learned about exit codes in the Processes module. Now let's use them to chain commands together!

The && operator allows you to run a second command only if the first command succeeds (in Linux convention, this means it exited with code 0). This is called the "AND" operator because both conditions must be true: the first command must succeed AND then the second command will run. That's super useful for complex commandline workflows where certain actions depend on the success of other actions.

Here's the syntax:

hacker@dojo:~$ command1 && command2
This means: "Run command1, and IF it succeeds, then run command2."

Some examples:

hacker@dojo:~$ touch /home/hacker/file && echo "this will run"
success
this will run
hacker@dojo:~$ touch /file && echo "this will NOT run"
touch: cannot touch '/file': Permission denied
hacker@dojo:~$
That second invocation of touch failed because the hacker user does not have write access to /file, so the echo did not run.

In this challenge, you need to chain the programs /challenge/first-success and /challenge/second using the && operator. Try running each command separately first to see what happens (which is that you will not get the flag). But if you chain them with &&, the flag will appear!

### Solve
**Flag:** `pwn.college{helloworld}`

As /challenge/first-success should run first then only /challenge/second will execute therefore, we chain them using &&.

```bash
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second
Nice chaining! Flag: pwn.college{wY_CL7oycaILzDPhekmcCq44e0G.0lM0MDOxwiNxIzNzEzW}
```

### New Learnings
chaining using && in which command 2 runs only and only if command 1 runs.

### References 
N.A.
