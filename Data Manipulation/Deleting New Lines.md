# Module Name

## Deleting New Lines 

A common class of characters to remove is a line separator. This happens when you have a stream of data that you want to turn into a single line for further processing. You can specify newlines almost like any other character, by escaping them:

hacker@dojo:~$ echo "hello_world!" | tr _ "\n"
hello
world!
hacker@dojo:~$
Here, the backslash (\) signifies that the character that follows it is a standin for a character that's hard to input into the shell normally. The newline, of course, is hard to input because when you typically hit Enter, you'll run the command itself. \n is a standin for this newline, and it must be in quotes to prevent the shell interpreter itself from trying to interpret it and pass it to tr instead.

Now, let's combine this with deletion. In this challenge, we'll inject a bunch of newlines into the flag. Delete them with tr's -d flag and the escaped newline specification!

Fun fact! Want to actually replace a backslash (\) character? Because \ is the escape character, you gotta escape it! \\ will be treated as a backslash by tr. This isn't relevant to this challenge, but is a fun fact nonetheless!

### Solve
**Flag:** pwn.college{cvxqpKR-CK8frAovL5n4qHNvZMZ.0VNxEzNxwiNxIzNzEzW}

As we need to use both -d and "\n" with tr to delete the new line and get the flag

```bash
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{cvxqpKR-CK8frAovL5n4qHNvZMZ.0VNxEzNxwiNxIzNzEzW}
```

### New Learnings
As we need to use both -d and "\n" with tr to delete the new line and get the flag

### References 
N.A.
