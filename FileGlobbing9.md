# File Globbing

## Multiple options for Tab completion

Consider the following situation:

hacker@dojo:~$ ls
flag  flamingo  flowers
hacker@dojo:~$ cat f<TAB>
There are multiple options! What happens?

What happens varies based on the specific shell and its options. By default bash will auto-expand until the first point when there are multiple options (in this case, fl). When you hit tab a second time, it'll print out those options. Other shells and configurations, instead, will cycle through the options.

This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. Tab-complete from /challenge/files/p or so, and make your way to the flag!

### Solve
**Flag:** pwn.college{ktmpjQt_y1xJmLz3K-RRYkBfOCW.0lN0EzNxwiNxIzNzEzW}

if we have multiple files with same name just do tab twice it lists down options of names

```bash
hacker@globbing~multiple-options-for-tab-completion:~$ cd /challenge/files
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:/challenge/files$ cat /challenge/files/pwncollege-flag
pwn.college{ktmpjQt_y1xJmLz3K-RRYkBfOCW.0lN0EzNxwiNxIzNzEzW}
```

### New Learnings
if we have multiple files with same name just do tab twice it lists down options of names


### References 
N.A.
