# Basic Linux Commands 🐧

<p align="center">
  <img src="./ChatGPT Image May 15, 2026, 03_36_55 PM.png" width="850"/>
</p>

## Introduction

Linux commands are used to interact with the operating system through the Command Line Interface (CLI).  
These commands help in:
- Navigating directories
- Managing files
- Monitoring systems
- Handling users
- Performing administrative tasks

Linux command-line skills are essential for DevOps and Cloud Engineers.

---

# 1. pwd Command

## Purpose
Displays the current working directory.

## Syntax

```bash
pwd
```

## Example

```bash
/home/siddharth
```

---

# 2. ls Command

## Purpose
Lists files and directories.

## Syntax

```bash
ls
```

## Common Options

```bash
ls -l
ls -la
ls -lh
```

| Option | Purpose |
|---|---|
| -l | Long listing format |
| -a | Show hidden files |
| -h | Human readable sizes |

---

# 3. cd Command

## Purpose
Changes directory.

## Syntax

```bash
cd directory_name
```

## Examples

```bash
cd /home
cd ..
cd ~
```

| Command | Meaning |
|---|---|
| cd .. | Move one directory back |
| cd ~ | Go to home directory |

---

# 4. mkdir Command

## Purpose
Creates a new directory.

## Syntax

```bash
mkdir foldername
```

## Example

```bash
mkdir devops
```

---

# 5. touch Command

## Purpose
Creates empty files.

## Syntax

```bash
touch filename
```

## Example

```bash
touch notes.txt
```

---

# 6. cp Command

## Purpose
Copies files and directories.

## Syntax

```bash
cp source destination
```

## Example

```bash
cp file1.txt file2.txt
```

## Copy Directory

```bash
cp -r folder1 folder2
```

---

# 7. mv Command

## Purpose
Moves or renames files/directories.

## Syntax

```bash
mv oldname newname
```

## Examples

```bash
mv test.txt demo.txt
mv file.txt /home/user/
```

---

# 8. rm Command

## Purpose
Deletes files and directories.

## Syntax

```bash
rm filename
```

## Examples

```bash
rm notes.txt
rm -r foldername
rm -rf project
```

⚠️ Be careful while using `rm -rf`.

---

# 9. cat Command

## Purpose
Displays file content.

## Syntax

```bash
cat filename
```

## Example

```bash
cat notes.txt
```

---

# 10. echo Command

## Purpose
Displays text output.

## Syntax

```bash
echo "message"
```

## Example

```bash
echo "Hello Linux"
```

---

# 11. clear Command

## Purpose
Clears terminal screen.

## Syntax

```bash
clear
```

---

# 12. man Command

## Purpose
Displays manual/help pages.

## Syntax

```bash
man commandname
```

## Example

```bash
man ls
```

---

# 13. history Command

## Purpose
Shows previously executed commands.

## Syntax

```bash
history
```

---

# 14. whoami Command

## Purpose
Displays current logged-in user.

## Syntax

```bash
whoami
```

---

# 15. uname Command

## Purpose
Displays system information.

## Syntax

```bash
uname
uname -a
```

---

# 16. date Command

## Purpose
Displays current date and time.

## Syntax

```bash
date
```

---

# 17. cal Command

## Purpose
Displays calendar.

## Syntax

```bash
cal
```

---

# 18. hostname Command

## Purpose
Displays system hostname.

## Syntax

```bash
hostname
```

---

# Hidden Files in Linux

Files starting with `.` are hidden files.

Examples:

```bash
.bashrc
.gitconfig
```

View hidden files:

```bash
ls -la
```

---

# Important Shortcuts

| Shortcut | Purpose |
|---|---|
| Ctrl + C | Stop running command |
| Ctrl + L | Clear terminal |
| Tab | Auto complete |
| Up Arrow | Previous commands |

---

# Real-World DevOps Usage 🚀

Linux commands are heavily used in:
- Server administration
- Docker containers
- Kubernetes
- CI/CD pipelines
- Cloud platforms
- Automation scripts

DevOps engineers work on Linux terminals daily.

---

# Quick Revision Table

| Command | Purpose |
|---|---|
| pwd | Current directory |
| ls | List files |
| cd | Change directory |
| mkdir | Create directory |
| touch | Create file |
| cp | Copy files |
| mv | Move/Rename |
| rm | Delete files |
| cat | Read file |
| history | Command history |

---

# Summary

Basic Linux commands are the foundation of system administration and DevOps engineering.  
Mastering these commands improves productivity, troubleshooting, and automation skills.

---

# Author

Siddharth Kanojia  
DevOps & Cloud Learning Journey 🚀
