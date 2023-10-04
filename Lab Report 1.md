**cd with no arguments**
```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```
Working directory when command was run: /home
Explanation: 

**cd with directory**
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
Working directory when command was run: /home


**cd with file**
```
[user@sahara ~]$ cd en-us.txt
bash: cd: en-us.txt: No such file or directory
```
Working directory when command was run: /home


**ls with no arguments**
```
[user@sahara ~]$ ls
lecture1
```
Working directory when command was run: /home


**ls with directory**
```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```
Working directory when command was run: /home


**ls with file**
```
[user@sahara ~]$ ls en-us.txt
ls: cannot access 'en-us.txt': No such file or directory
```
Working directory when command was run: /home


**cat with no argument**
```
[user@sahara ~]$ cat

control C to get out of error
```
Working directory when command was run: /home


**cat with directory**
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```
Working directory when command was run: /home


**cat with file**
```
[user@sahara ~]$ cat en-us.txt
cat: en-us.txt: No such file or directory
```
Working directory when command was run: /home



