# Pondering Paths

## Position Thy Self

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. 

### Solve
**Flag:** pwn.college{47yLaXP70Pck6t0KwFikTRAJ5mX.QX2QTN0wiNxlzNzEzW} 

typing in just /challenge/run gives error as we are not running it from required directory. It gives us the path of required directory.
Doing cd /address we are now into the required directory, now typing in /challenge/run gives the required flag

```hacker@paths~position-thy-self :~ $ /challenge/run  
hacker@paths~position-thy-self :~ $ cd /usr/share/zoneinfo/posix/Asia 
hacker@paths~position-thy-self:/usr/share/zoneinfo/posix/Asia$ /challenge/run
pwn.college{47yLaXP70Pck6t0KwFikTRAJ5mX.QX2QTN0wiNxlzNzEzW} ```

### New Learnings
Learned how to change directories. If we know the address of required library then just type in cd/add . Then type the program name you want to run

### References 
N.A.
