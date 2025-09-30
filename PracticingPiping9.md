# Practicing Piping 

## Filtering with grep -v

The grep command has a very useful option: -v (invert match). While normal grep shows lines that MATCH a pattern, grep -v shows lines that do NOT match a pattern:

hacker@dojo:~$ cat data.txt
hello hackers!
hello world!
hacker@dojo:~$ cat data.txt | grep -v world
hello hackers!
hacker@dojo:~$
Sometimes, the only way to filter to just the data you want is to filter out the data you don't want. In this challenge, /challenge/run will output the flag to stdout, but it will also output over 1000 decoy flags (containing the word DECOY somewhere in the flag) mixed in with the real flag. You'll need to filter out the decoys while keeping the real flag!

Use grep -v to filter out all the lines containing "DECOY" and reveal the real flag!

### Solve
**Flag:** pwn.college{k94HAi-i2D0lS0LNJ_WLl8ELR_n.0FOxEzNxwiNxIzNzEzW}
 
as -v filters out the specified word as argument. here we use it to filter out all DECOY flags and get real onw

```bash
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{helloworld}pwn.college{k94HAi-i2D0lS0LNJ_WLl8ELR_n.0FOxEzNxwiNxIzNzEzW}```

### New Learnings
using grep with -v filters out that word and gives the remaining file as output.

### References 
N.A.
