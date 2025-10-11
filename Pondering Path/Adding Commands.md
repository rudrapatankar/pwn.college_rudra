# Pondering Path

## Adding Commands

Recall our example from the previous level:

hacker@dojo:~$ ls /home/hacker/scripts
goodscript	badscript	okayscript
hacker@dojo:~$ PATH=/home/hacker/scripts
hacker@dojo:~$ goodscript
YEAH! This is the best script!
hacker@dojo:~$
What we see here, of course, is the hacker making the shell more useful for themselves by bringing their own commands to the party. Over time, you might amass your own elegant tools. Let's start with win!

Previously, the win command that /challenge/run executed was stored in /challenge/more_commands. This time, win does not exist! Recall the final level of Chaining Commands, and make a shell script called win, add its location to the PATH, and enable /challenge/run to find it!

Hint: /challenge/run runs as root and will call win. Thus, win can simply cat the flag file. Again, the win command is the only thing that /challenge/run needs, so you can just overwrite PATH with that one directory. But remember, if you do that, your win command won't be able to find cat.

You have three options to avoid that:

Figure out where the cat program is on the filesystem. It must be in a directory that lives in the PATH variable, so you can print the variable out (refer to Shell Variables to remember how!), and go through the directories in it (recall that the different entries are separated by :), find which one has cat in it, and invoke cat by its absolute path.
Set a PATH that has the old directories plus a new entry for wherever you create win.
Use read (again, refer to Shell Variables) to read /flag. Since read is a builtin functionality of bash, it is unaffected by PATH shenanigans.
Now, go and win!

### Solve
**Flag:** pwn.college{0mBpVSs5hrJ2wqy25wShFZQ4m8o.QX2cjM1wiNxIzNzEzW}

make new directory inside /home/hacker directory then make shell called win which is used to read /flag file and execute it first by giving access using chmod +x and then using PATH = PATH=/home/hacker/bin/challenge/run
gives the flag

```bash
hacker@path~adding-commands:~$ mkdir -p /home/hacker/bin
hacker@path~adding-commands:~$ cat > /home/hacker/bin/win <<'EOF'
#!/bin/bash
read -r FLAG < /flag
printf '%s\n' "$FLAG"
EOF
hacker@path~adding-commands:~$ chmod +x /home/hacker/bin/win
hacker@path~adding-commands:~$ PATH=/home/hacker/bin /challenge/run
Invoking 'win'....
pwn.college{0mBpVSs5hrJ2wqy25wShFZQ4m8o.QX2cjM1wiNxIzNzEzW}
```

### New Learnings
applying concepts of both pondering path and shell modules and also read -r FLAG</flag stores flag into FLAG then output using echo or print

### References 
N.A.
