cd with no arguments
```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```

cd with directory
```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```

cd with file
```
[user@sahara ~]$ cd en-us.txt
bash: cd: en-us.txt: No such file or directory
```

ls with no arguments
```
[user@sahara ~]$ ls
lecture1
```

ls with directory
```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```

ls with file
```
[user@sahara ~]$ ls en-us.txt
ls: cannot access 'en-us.txt': No such file or directory
```

cat with no argument
```
[user@sahara ~]$ cat

control C to get out of error
```

cat with directory
```
[user@sahara ~]$ cat lecture1
cat: lecture1: Is a directory
```

cat with file
```
[user@sahara ~]$ cat en-us.txt
cat: en-us.txt: No such file or directory
```


