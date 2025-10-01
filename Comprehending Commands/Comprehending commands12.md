# Comprehending Commands

##making directories

We can create files. How about directories? You make directories using the mkdir command. Then you can stick files in there!

Watch:

hacker@dojo:~$ cd /tmp
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ ls
hacker@dojo:/tmp$ mkdir my_directory
hacker@dojo:/tmp$ ls
my_directory
hacker@dojo:/tmp$ cd my_directory
hacker@dojo:/tmp/my_directory$ touch my_file
hacker@dojo:/tmp/my_directory$ ls
my_file
hacker@dojo:/tmp/my_directory$ ls /tmp/my_directory/my_file
/tmp/my_directory/my_file
hacker@dojo:/tmp/my_directory$
Now, go forth and create a /tmp/pwn directory and make a college file in it! Then run /challenge/run, which will check your solution and give you the flag!

**Flag:** pwn.college{cQ_hsIQ12_EaDFOQbKFz5xFgj04.QXxMDO0wiNxIzNzEzW}


to make directory /tmp/pwn then first cd /tmp then mkdir pwn and then cd pwn. for creating file now in /tmp/pwn touch filename


```bash
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch colleg
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{cQ_hsIQ12_EaDFOQbKFz5xFgj04.QXxMDO0wiNxIzNzEzW}
```

### New Learnings
mkdir used to make new directories in already existing directories

### References 
N.A.
