# 01. Course overview + the shell - note

## Basic command

- `echo` print result
- `pwd` print current working directory
- `cd` change working directory
- `ls` list
- `mv` move/ rename file
- `cp` copy
- `rm` remove file
- `rmdir` remove directory
- `touch` add new file
- `mkdir` add new directory
- `cat` print the file content
- `sudo` do as super user
- `sudo su` switch super user to root user

```bash
# both print the same result: Hello World

echo "Hello World"
echo Hello\ World


mkdir "My Photo"  #add a directory named "My Photo"
mkdir My Photo    # add 2 directories, one named "My", the other one named "Photo"
```

### `cd` ways to change directory

- `cd .` to parent directory
- `cd ..` to root directory
- `cd ~` to home directory
- `cd ./home` to the directory name "home" which is under current directory
- `cd -` switch between home directory and current working directory

## Permission

How to know whether permission I have to the file?

`ls -l` will list detailed file permission information:

```bash
drwxr-xr-x  11 laiyenju  staff        352 Mar 18 01:06 data-ppf
-rw-r--r--   1 laiyenju  staff        465 Aug  6 21:37 data.php
-rw-r--r--   1 laiyenju  staff        523 Aug 30 08:43 demo.html
```

- **d** means this file is a directory. And the following 9 charactor `rwxr-xr-x` represent the 3 groups of permissions.
- **w** means having the permission to write/ overwrite file
- **x** means having the permission to execute file
- **r** means havving the permission to read file
- **-** means having no permission

**==rwx== r-xr-x**, the 1st group represents the right of file owner. 
In this case, file owner has the permission to write, read and execute the file.

**rwx ==r-x== r-x**, the 2nd group represents the right of Users.
In this case, Users has the permission to read and execute the file. But the Users has no permission to write the file.

**rwxr-x ==r-x==**, the 3rd group represents the right of the others.

## Stream `>`, `<`, `>>`

There are 2 types of stream: input stream, output stream.
The default input stream is keyboard, the default output stream is terminal.

**>** output
**<** input
**>>** append

- `echo hello > hello.txt` write "hello" word in hello.txt
- `cat hello.txt` print the content in hello.txt
- `cat < hello.txt` print the content in hello.txt
- `cat < hello.txt > hello2.txt` copy the hello.txt content to hello2.txt
- `cat < hello.txt >> hello2.txt` append hello.txt content to hello2.txt

## Pipe `|`

Pipe's function is to connect or chain commands.

`ls -l/ | tail -n1 > ls.txt`

1. print the detailed information in this directory
2. and then only show the last one row
3. put the last one row into ls.txt
