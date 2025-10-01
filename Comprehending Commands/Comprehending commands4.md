# Comprehending Commands

##Grepping for needle in a haystick

 the files that you might cat out are too big. Luckily, we have the grep command to search for the contents we need! We'll learn it in this challenge.

There are many ways to grep, and we'll learn one way here:

hacker@dojo:~$ grep SEARCH_STRING /path/to/file
Invoked like this, grep will search the file for lines of text containing SEARCH_STRING and print them to the console.

In this challenge, I've put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag!

HINT: The flag always starts with the text pwn.college.

### Solve
**Flag:** pwn.college{k0DjmqLiFMtGyFK_ut601EEDp11w.QX3EDO0wiNxIzNzEzW}

as every flag starts with pwn.college hence if we do grep pwn.college /challenge/data.txt
.Then we are searching for only that part of text which contains pwn.college that is the flag part.

```bash
grep pwn.college /challenge/data.txt
pwn.college{k0DjmqLiFMtGyFK_ut601EEDp11w.QX3EDO0wiNxIzNzEzW}
```

### New Learnings
We can search for some specific content in a file by using grep "content to be searched" "absolute address"

### References 
N.A.
