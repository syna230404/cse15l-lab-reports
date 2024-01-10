# cd command

1. *No* arguments

```
[user@sahara ~/lecture1]$ cd
[user@sahara ~]$
```
Using `cd` with no arguments takes us back to the `~` directory
Working directory: ~/lecture1
This is not an error

2. With a Path to a Directory

```
[user@sahara ~]$ cd lecture1
[user@sahara ~/lecture1]$
```
Using cd with a folder path changes our current working directory to that folder
Working directory: ~/
This is not an error

3. With a Path to a File

```
[user@sahara ~]$ cd Hello.java
bash: cd: Hello.java: No such file or directory
[user@sahara ~]$
```
This prints an error message as the `cd` command only works with folders/directories
Working directory: ~/
This is an error as the command did not make us change directories (which is it's purpose)

# ls command

1. *No* arguments

```
[user@sahara ~]$ ls
lecture1
```
This command prints all the files and folders in the current working directory
Working directory: ~/
Not an error

2. With a Path to a Directory

```
[user@sahara ~]$ ls lecture1
Hello.class  Hello.java  messages  README
```
This command prints all the files in the path we specified
Working directory: ~/
Not an error

3. With a Path to a File

```
[user@sahara ~]$ ls lecture1/Hello.java
lecture1/Hello.java
```
This command prints file path
Working directory: ~/
Not an error

# cat command

1. *No* arguments

```
[user@sahara ~]$ cat
^C
```
It basically gets stuck as there is nothing to concatenate
Working directory: ~/
This is an error

2. With a Path to a Directory

```
[user@sahara ~]$ cat lecture1/
cat: lecture1/: Is a directory
```
The command doesn't do anything as cat isn't supposed to work with directories as input
Working directory: ~/
This is an error as cat didn't print any content

3. With a Path to a File

```
[user@sahara ~]$ cat lecture1/messages/en-us.txt lecture1/messages/new.txt 
Hello World!
हैलो वर्ल्ड!
[user@sahara ~]$ cat lecture1/messages/en-us.txt
Hello World!
```
The cat command prints the content of the file(s) as shown
Working directory: ~/
Not an error
