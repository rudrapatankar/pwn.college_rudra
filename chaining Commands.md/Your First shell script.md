# Chaining Commands

## Your First Shell Script 

As you combine more and more commands to achieve complex effects, the length of the combined prompt quickly gets really annoying to deal with. When this happens, you can put these commands in a file, called a shell script, and run them by executing the file! For example, consider our semicolon technique:

hacker@dojo:~$ echo COLLEGE > pwn; cat pwn
COLLEGE
hacker@dojo:~$
We can create a shell script called pwn.sh (by convention, shell scripts are frequently named with a sh suffix):

echo COLLEGE > pwn
cat pwn
And then we can execute by passing it as an argument to a new instance of our shell (bash)! When a shell is invoked like this, rather than taking commands from the user, it reads commands from the file.

hacker@dojo:~$ ls
hacker@dojo:~$ bash pwn.sh
COLLEGE
hacker@dojo:~$ ls
pwn
hacker@dojo:~$
You can see that the shell script executed both commands, creating and printing the pwn file.

Now, it's your turn! Same as last level, run /challenge/pwn and then /challenge/college, but this time in a shell script called x.sh, then run it with bash!

NOTE: We haven't yet talked about Linux's amazing array of competent command line file editors. For now, feel free to use the Text Editor application in Desktop mode (Applications->Accessories->Text Editor) or the default editor in the VSCode Workspace!

### Solve
**Flag:** pwn.college{AgfdkLGq020a2T6nAl6bcR_sXNI.QXxcDO0wiNxIzNzEzW}

cat > used  to create x shell and specify end of shell with <<'EOF'. The commands contained in the shell will be /challenge/pwn & /challenge/college.

```bash
hacker@chaining~your-first-shell-script:~$ cat > x.sh <<'EOF'
/challenge/pwn
/challenge/college
EOF
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{AgfdkLGq020a2T6nAl6bcR_sXNI.QXxcDO0wiNxIzNzEzW}
```

### New Learnings
cat > used  to create x shell and specify end of shell with <<'EOF'. The commands contained in the shell will be /challenge/pwn & /challenge/college.

### References 
N.A.
