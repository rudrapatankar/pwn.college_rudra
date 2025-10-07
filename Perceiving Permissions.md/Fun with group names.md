# Perceiving Permissions

## Fun with group names

In the previous levels, you may have noticed that your hacker user is a member of the hacker group, and that zardus is a member of the zardus group. There is a convention in Linux that every user has their own group, but this does not have to be the case. For example, many computer labs will put all of their users into a single, shared users group.

The point is, you've used hacker for the group before, but in this level, that is not going to work. I'll still allow you to use chgrp, but I have randomized the name of the group that your user is in. You will need to use the id command to figure that name out, then chgrp to victory!

### Solve
**Flag:**  pwn.college{kVQMwZJe2bOoJZeUClPbuU17jb3.QXycjM1wiNxIzNzEzW}

using id identify the group in which user is placed then use chgrp to change grp of /flag to specified group name and then read /flag using cat

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp27668) groups=1000(grp27668)
hacker@permissions~fun-with-groups-names:~$ chgrp grp27668 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{kVQMwZJe2bOoJZeUClPbuU17jb3.QXycjM1wiNxIzNzEzW}
```

### New Learnings
using id identify the group in which user is placed then use chgrp to change grp of /flag to specified group name and then read /flag using cat

### References 
N.A.
