# Pondering Paths

## PositionPositionyetElsewhere

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. 

### Solve
**Flag:** pwn.college{cgRfEOUQxSB1O1sRflqfZXISHDW.QX4QTN0wiNxIzNzEzW}

typing in /challenge/run gives error as we are not in directory /var. type in cd /var, this command takes us to / directory and hence now typing in /challenge/run gives us the desired output 
```bash
~$ : /challenge/run
~$ : cd /
/$ : /challenge/run
pwn.college{cgRfEOUQxSB1O1sRflqfZXISHDW.QX4QTN0wiNxIzNzEzW}
```

### New Learnings
initial directory was ~ which was changed to /using cd command. Invoking the required the directory while executing command gives the desired flag.

### References 
N.A