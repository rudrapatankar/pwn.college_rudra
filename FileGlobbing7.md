# File Globbing

## Exclusionary Globbing

Sometimes, you want to filter out files in a glob! Luckily, [] helps you do just this. If the first character in the brackets is a ! or (in newer versions of bash) a ^, the glob inverts, and that bracket instance matches characters that aren't listed. For example:

hacker@dojo:~$ touch file_a
hacker@dojo:~$ touch file_b
hacker@dojo:~$ touch file_c
hacker@dojo:~$ ls
file_a	file_b	file_c
hacker@dojo:~$ echo Look: file_[!ab]
Look: file_c
hacker@dojo:~$ echo Look: file_[^ab]
Look: file_c
hacker@dojo:~$ echo Look: file_[ab]
Look: file_a file_b
Armed with this knowledge, go forth to /challenge/files and run /challenge/run with all files that don't start with p, w, or n!

NOTE: The ! character has a different special meaning in bash when it's not the first character of a [] glob, so keep that in mind if things stop making sense! ^ does not have this problem, but is also not compatible with older shells.

### Solve cd to /challenge/files then run /challenge/run [!pwn] to get flag


 
**Flag:** `pwn.college{Yvj5KMtdpPNkJXaZxvZgR6RP2WP.QX2IDO0wiNxIzNzEzW}`



```bash
rudra@RUDRA-BOOK5:~$ ssh -i key hacker@dojo.pwn.college
Connected!
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]
Your expansion did not expand to the requested files (amazing beautiful
challenging delightful educational fantastic great happy incredible jovial kind
laughing magical optimistic queenly radiant splendid thrilling uplifting
victorious xenial youthful zesty).
Instead, it expanded to:
[!pwn]
hacker@globbing~exclusionary-globbing:/challenge/files$  /challenge/run [!pwn]*
pwn.college{Yvj5KMtdpPNkJXaZxvZgR6RP2WP.QX2IDO0wiNxIzNzEzW}
```

### New Learnings
to search without certain files just use ! in the globbing

### References 
N.A.
