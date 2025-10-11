# Pondering Paths

## Adding Commands
Add challenge description here

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
