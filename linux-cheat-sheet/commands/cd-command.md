# Linux `cd` Command with Practical Examples

## Introduction

Here, we learn about the Linux `cd` command and how to navigate the file system using it. We'll cover the purpose and syntax of `cd`, explore relative and absolute paths, and practice common shortcuts.


## 1. Purpose and Syntax

The `cd` command is used to change the current working directory.

Basic syntax:

```bash
cd [directory]
```

Here, `[directory]` is the path you want to change to. The path can be absolute or relative.

Examples:

- Absolute path:

```bash
cd /home/myname/project
```

- Relative path (from current directory):

```bash
cd directory_name
```

Common shortcuts:

- `cd` or `cd ~` — go to your home directory (e.g. `/home/myname`)
- `cd -` — go to the previous working directory
- `cd ..` — go to the parent directory of the current working directory

Example session:

```bash
myname@ubuntu:~/project$ cd /home/myname/project
myname@ubuntu:/home/myname/project$ cd ..
myname@ubuntu:/home/myname$ cd -
/home/myname/project
myname@ubuntu:/home/myname/project$
```

---

## 2. Navigate the File System Using `cd`

Let's create some directories and files in `~/project` and navigate them:

Commands to set up:

```bash
cd ~/project
mkdir dir1 dir2 dir3
touch file1.txt file2.txt
```

Navigate between directories:

```bash
cd dir1
# Now in ~/project/dir1

cd ../dir2
# Now in ~/project/dir2

cd ../../dir3
# Now in ~/project/dir3
```

Notes on the above:

- `cd dir1` moves into a subdirectory of the current directory.
- `cd ../dir2` moves to a sibling directory (`..` refers to parent).
- `cd ../../dir3` moves two levels up and then into `dir3`.

You can also use absolute paths at any time:

```bash
cd /home/myname/project/dir1
# Now in /home/myname/project/dir1
```

Example session:

```bash
myname@ubuntu:~/project$ mkdir dir1 dir2 dir3
myname@ubuntu:~/project$ touch file1.txt file2.txt
myname@ubuntu:~/project$ cd dir1
myname@ubuntu:~/project/dir1$ cd ../dir2
myname@ubuntu:~/project/dir2$ cd ../../dir3
myname@ubuntu:~/project/dir3$ cd /home/myname/project/dir1
myname@ubuntu:/home/myname/project/dir1$
```

---

## 3. Relative vs Absolute Paths

### Relative Paths
Relative paths are interpreted from the current working directory.

Example (current directory is `/home/myname/project`):

```bash
cd dir1
# Now in /home/myname/project/dir1
```

### Absolute Paths
Absolute paths start at the root `/`.

Example:

```bash
cd /home/myname/project/dir1
# Now in /home/myname/project/dir1
```

Combined example:

```bash
# Current working directory: /home/myname/project
cd dir1
# -> /home/myname/project/dir1

cd ..
# -> /home/myname/project

cd /home/myname/project/dir2
# -> /home/myname/project/dir2
```

Example session:

```bash
myname@ubuntu:~/project$ cd dir1
myname@ubuntu:~/project/dir1$ cd ..
myname@ubuntu:~/project$ cd /home/myname/project/dir2
myname@ubuntu:~/project/dir2$
```

---

## 4. Linux Commands Cheat Sheet (cd)

- `cd` or `cd ~` — go to home directory
- `cd /path/to/dir` — go to absolute path
- `cd relative/path` — go to relative path
- `cd ..` — go to parent directory
- `cd -` — go to previous directory
- `cd ../sibling` — go to a sibling directory
- `cd ../../path` — move up two levels then into `path`
