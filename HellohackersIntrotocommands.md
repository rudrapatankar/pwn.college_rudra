# Hello Hackers

## Intro to commands
invoke your first command as :
hacker@dojo : -$ whoami
hacker


### Solve
**Flag:** pwn.college{wt55cWIk13xGo3HE-Q1KYLK_uap.QX3YjM1wiNxIzNzEzW}

type in your solve and your thought process behind solving the challenge. Include as much as info as possible. Use triple ticks for any bash commands and output you type on the terminal.

```bash
cd~
ssh-keygen -t ed25519 -f./key -N''
cat key.pub
ssh -i key hacker@dojo.pwn.college
whoami
hello
pwn.college{wt55cWIk13xGo3HE-Q1KYLK_uap.QX3YjM1wiNxIzNzEzW} - flag

### New Learnings
I learned how to get the ssh key and also how to invoke the first command in the Linux terminal of windows.

### References 
Reference video used to generate the ssh key was provided in the jtp8 group
