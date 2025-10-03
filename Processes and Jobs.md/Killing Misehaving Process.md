# Processes and jobs

##Killing Misehaving Process

Sometimes, misbehaving processes can interfere with your work. These processes might need to be killed...

In this challenge, there's a decoy process that's hogging a critical resource - a named pipe (FIFO) at /tmp/flag_fifo into which (like in the Practicing Piping FIFO challenge) /challenge/run wants to write your flag. You need to kill this process.

Your general workflow should be:

Check what processes are running.
Find /challenge/decoy in the list and figure out its process ID.
kill it.
Run /challenge/run to get the flag without being overwhelmed by decoys (you don't need to redirect its output; it'll write to the FIFO on its own).
Good luck!

NOTE: You might see a few decoy flags show up even after killing the decoy process. This happens because Linux pipes are buffered: conceptually, they have a sort of length through which data flows, and you might kill the decoy process while data is in the pipe. That data, having already entered the pipe, will proceed to the other end (your cat). If you wait a second, you'll see the decoys stop, and then you can /challenge/run and win!

### Solve
**Flag:** pwn.college{QBOGWuSbHM21eXu9nwdHKjbSieo.0FNzMDOxwiNxIzNzEzW}

list all processes then kill PID of decoy file. do /challenge/run output flag gets piped into fifo file then cat the fifo flag file from second terminal to get flag

```bash
Terminal 1 :
ps aux 
kill 142
/challenge/run

Terminal 2:
cat /tmp/flag_fifo hacker
pwn.college{QBOGWuSbHM21eXu9nwdHKjbSieo.0FNzMDOxwiNxIzNzEzW}
```

### New Learnings
using kill function to remove unwanted misbehaving processes

### References 
N.A.
