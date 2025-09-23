# Pondering Paths

## Position Elsewhere

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program.

### Solve
**Flag:** pwn.college{EsWBogYDQlFW3nGYnnlMowj5FjI.QX3QTN0wiNxIzNzEzW}

typing in /challenge/run gives error as we are not in directory /var. type in cd /var, this command takes us to var directory and hence now typing in /challenge/run gives us the desired output 

```bash
/challenge/run
cd /var
/challenge/run
pwn.college{EsWBogYDQlFW3nGYnnlMowj5FjI.QX3QTN0wiNxIzNzEzW}```

### New Learnings
Commands typed in wrong directory gives the position of the command elsewhere. cd /positionelesewhere and then typing the earlier command gives desired output

### References 
N.A.
