# Linux `pwd` Command with Practical Examples

## Introduction

Here, you will learn how to use the `pwd` command in Linux, which stands for "Print Working Directory".

## 1. Understand the Purpose of the `pwd` Command

The `pwd` command stands for "Print Working Directory" and is used to display the current working directory.

To use the `pwd` command, simply type:

```bash
pwd
```

Example output:

```
/home/myname/project
```

The output shows that the current working directory is `/home/myname/project`. This is the directory where the user is currently located.

The `pwd` command is useful when you need to know your current location in the file system. It can be used in combination with other commands to perform various tasks, such as navigating to a specific directory or executing commands in the current directory.

## 2. Explore the `pwd` Command in Different Directories

Create a new directory and navigate to it:

```bash
mkdir ~/project/subdirectory
cd ~/project/subdirectory
```

Now run the `pwd` command:

```bash
pwd
```

Example output:

```
/home/myname/project/subdirectory
```

As you can see, the output of `pwd` has changed to reflect the new current working directory.

Go back to the parent directory:

```bash
cd ..
pwd
```

Example output:

```
/home/myname/project
```

The `pwd` command now shows that we are back in the parent directory, `/home/myname/project`.

Navigate to the root directory:

```bash
cd /
pwd
```

Example output:

```
/
```

The `pwd` command always displays the full path of the current working directory, regardless of where you are in the file system. This makes it a useful tool for keeping track of your location and navigating the file system.


## 3. Combine `pwd` with Other Linux Commands

You can use `pwd` to specify the current working directory when executing other commands.

Create a new file in the current directory using `pwd` to build the path:

```bash
touch $(pwd)/new_file.txt
```

This creates a new file named `new_file.txt` in the current working directory (for example, `/home/myname/project`).

You can also navigate to a specific directory and then execute a command using `pwd`. For instance, navigate to the root directory and list its contents:

```bash
cd /
ls -l $(pwd)
```

Example output (truncated):

```
total 60
drwxr-xr-x   2 root root  4096 Apr 28 06:54 bin
drwxr-xr-x   3 root root  4096 Apr 28 06:54 boot
drwxr-xr-x   5 root root  4096 May  2 06:16 dev
drwxr-xr-x  92 root root  4096 May  2 06:16 etc
drwxr-xr-x   3 root root  4096 Apr 28 06:54 home
lrwxrwxrwx   1 root root    33 Apr 28 06:54 initrd.img -> /boot/initrd.img-5.15.0-60-generic
drwxr-xr-x  20 root root  4096 Apr 28 06:54 lib
...
```

Combining `pwd` with other commands can be a powerful way to automate tasks and work more efficiently in the Linux command line.


## 4. Linux Commands Cheat Sheet (pwd)

- `pwd` — print the full path of the current working directory
- `pwd -L` — print the value of $PWD (may show logical path with symlinks)
- `pwd -P` — print the physical directory, resolving symlinks
- Use `$(pwd)` to embed the current working directory into other commands, e.g. `touch $(pwd)/file.txt`
