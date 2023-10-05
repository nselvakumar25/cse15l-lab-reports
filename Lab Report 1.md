**cd with no arguments**
```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```
Working directory when command was run: /home  
Explanation: This command did not do anything because we did not specify what directory it should change to. As a result, it remained in the root directory.

**cd with directory**
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
Working directory when command was run: /home  
Explanation: Since a directory was given after the cd command, it changed directories from /home to lecture1. This is further shown in the next line which indicates lecture1 as the current directory.

**cd with file**
```
[user@sahara ~]$ cd lecture1/messages/en-us.txt
bash: cd: lecture1/messages/en-us.txt: Not a directory
```
Working directory when command was run: /home  
Explanation: The cd command is used to change into a directory, not a file. As a result, it informs the user that the path did not lead to a directory so it cannot be used.


**ls with no arguments**
```
[user@sahara ~]$ ls
lecture1
```
Working directory when command was run: /home  
Explanation: Without any arguments, it is assumed that we are asking for a list of contents in the current directory which is /home. This is why ls with no arguments prints out lecture1 which is the only item in the current directory.

**ls with directory**
```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```
Working directory when command was run: /home  
Explanation: With lecture 1 as the argument, ls prints out a list of all the contents in the lecture1 directory.  

**ls with file**
```
[user@sahara ~]$ ls lecture1/messages/en-us.txt
lecture1/messages/en-us.txt
```
Working directory when command was run: /home  
Explanation: Since the file path that was given leads to en-us.txt which is not a directory and does not have any items that can be listed, the ls command just prints out the path to the file instead.

**cat with no argument**
```
[user@sahara ~]$ cat


```
Working directory when command was run: /home  
Explanation: Since the cat command does not include a path to a file, it creates an error where it prints out a blank line and does not allow any further input in the terminal.

**cat with directory**
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
Working directory when command was run: /home  
Explanation: The command cat cannot print the contents of a directory. It can only print the contents of a file. Thus, it informs the user that the given path leads to a directory which cannot be used in this situation.

**cat with file**
```
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
```
Working directory when command was run: /home  
Explanation: This command is able to print the contents of a file. Since we gave the path to en-us.txt, it printed out everything written inside that file.
