# Chaining Commands

## Executable Shell Scripts

You have written your first shell script, but calling it via bash script.sh is a pain. Why do you need that bash?

When you invoke bash script.sh, you are, of course launching the bash command with the script.sh argument. This tells bash to read its commands from script.sh instead of standard input, and thus your shell script is executed.

It turns out that you can avoid the need to manually invoke bash. If your shell script file is executable (recall File Permissions), you can simply invoke it via its relative or absolute path! For example, if you create script.sh in your home directory and make it executable, you can invoke it via /home/hacker/script.sh or ~/script.sh or (if your working directory is /home/hacker) ./script.sh.

Try that here! Make a shellscript that will invoke /challenge/solve, make it executable, and run it without explicitly invoking bash!

### Solve
**Flag:** : pwn.college{QCegJUgv_a2jrUsluxy01On1HrU.QX0cjM1wiNxIzNzEzW}

nano script1.sh then in shell put command /challenge/solve then chmod +x script1.sh to give executable access then directly run /home/hacker/script1.sh

```bash
hacker@chaining~executable-shell-scripts:~$ nano script1.sh
hacker@chaining~executable-shell-scripts:~$ chmod +x script1.sh
hacker@chaining~executable-shell-scripts:~$ /home/hacker/script1.sh
Congratulations on your shell script execution! Your flag:
pwn.college{QCegJUgv_a2jrUsluxy01On1HrU.QX0cjM1wiNxIzNzEzW}
```

### New Learnings
after giving executive access we can directly run shell without using bash but the address of shell

### References 
N.A.
