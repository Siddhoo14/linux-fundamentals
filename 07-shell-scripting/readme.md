# Shell Scripting 🖥️🐧

<p align="center">
  <img src="../images/shell-scripting-banner.png" width="950"/>
</p>

## Introduction

Shell Scripting is the process of writing a sequence of Linux commands in a file and executing them automatically.

Instead of running commands one by one, Shell Scripts help automate repetitive tasks, making system administration faster and more efficient.

Shell scripting is one of the most important skills for:

* Linux Administrators
* DevOps Engineers
* Cloud Engineers
* System Engineers

---

# What is a Shell?

A Shell is a command-line interpreter that acts as an interface between the user and the Linux operating system.

Popular Linux Shells:

| Shell | Description                       |
| ----- | --------------------------------- |
| Bash  | Bourne Again Shell (Most Popular) |
| Sh    | Bourne Shell                      |
| Zsh   | Z Shell                           |
| Ksh   | Korn Shell                        |

---

# What is a Shell Script?

A Shell Script is a text file containing Linux commands.

Example:

```bash
#!/bin/bash

echo "Hello DevOps!"
```

Save as:

```bash
hello.sh
```

Run:

```bash
chmod +x hello.sh
./hello.sh
```

---

# Why Use Shell Scripting?

Without Automation:

❌ Repetitive manual tasks
❌ Human errors
❌ Slow administration

With Shell Scripting:

✅ Task automation
✅ Faster execution
✅ Consistent operations
✅ Improved productivity

---

# Shebang (#!)

The first line of a shell script is called a Shebang.

Example:

```bash
#!/bin/bash
```

Purpose:

* Specifies the interpreter
* Tells Linux how to execute the script

---

# Variables

Variables store values.

Example:

```bash
name="Siddharth"

echo $name
```

Output:

```text
Siddharth
```

---

# User Input

Example:

```bash
read -p "Enter your name: " name

echo "Welcome $name"
```

---

# Conditional Statements

## If Statement

```bash
if [ $age -ge 18 ]
then
    echo "Adult"
fi
```

---

## If-Else Statement

```bash
if [ $age -ge 18 ]
then
    echo "Adult"
else
    echo "Minor"
fi
```

---

# Loops

## For Loop

```bash
for i in {1..5}
do
    echo $i
done
```

---

## While Loop

```bash
count=1

while [ $count -le 5 ]
do
    echo $count
    ((count++))
done
```

---

# Functions

Functions help organize reusable code.

Example:

```bash
greet() {
    echo "Welcome to DevOps"
}

greet
```

---

# Command-Line Arguments

Example:

```bash
echo $1
```

Run:

```bash
./script.sh Siddharth
```

Output:

```text
Siddharth
```

---

# Common Operators

## Numeric Operators

| Operator | Meaning            |
| -------- | ------------------ |
| -eq      | Equal              |
| -ne      | Not Equal          |
| -gt      | Greater Than       |
| -lt      | Less Than          |
| -ge      | Greater Than Equal |
| -le      | Less Than Equal    |

---

# Important Shell Commands

| Command | Purpose            |
| ------- | ------------------ |
| echo    | Print output       |
| read    | Take user input    |
| chmod   | Change permissions |
| pwd     | Current directory  |
| ls      | List files         |
| mkdir   | Create directory   |
| rm      | Remove files       |

---

# Error Handling Example

```bash
if [ -f file.txt ]
then
    echo "File exists"
else
    echo "File not found"
fi
```

---

# Real-World DevOps Usage 🚀

Shell scripting is widely used for:

* Backup automation
* User management
* Server monitoring
* Log rotation
* Deployment automation
* CI/CD pipelines
* Infrastructure management

Examples:

* Linux Backup Automation
* User Management Automation
* Health Check Scripts
* Deployment Scripts

---

# Best Practices 🔥

✅ Use meaningful variable names

✅ Add comments in scripts

✅ Handle errors properly

✅ Test scripts before production

✅ Keep scripts modular

✅ Follow consistent formatting

---

# Summary

Shell Scripting is one of the most powerful Linux automation tools. It helps automate administrative tasks, improve efficiency, and forms the foundation for DevOps and Cloud Automation workflows.

Mastering Shell Scripting is essential for every DevOps Engineer.

---

# Author

Siddharth Kanojia

Building my DevOps journey through Linux, Automation, Cloud, and Real-World Projects 🚀
