# Linux Process Management ⚙️🐧

<p align="center">
  <img src="./e6sNtpkE8cUfbeXJjHwjoTqwYDs5f_HcCeWeHXOP7ZF_4xyjPT_Z8H-0VGTHiUHE5P7-rS6ezE05ocsE34GQO4GTOBi4C1j4XHBe5r0x-D_uJ9fh6GyJVuPb-kcV8Ii4vE4oYSPfy6zJn.jfif" width="950"/>
</p>

## Introduction

A process in Linux is a running instance of a program.

Whenever a command or application runs in Linux, the operating system creates a process for it.

Process management is an essential skill for:
- Linux Administration
- DevOps Engineering
- Cloud Computing
- Server Monitoring
- Troubleshooting

---

# What is a Process?

A process is simply a program that is currently executing.

Examples:
- Running Google Chrome
- Running nginx server
- Running a Bash script

Each process has:
- PID (Process ID)
- Memory allocation
- CPU usage
- State

---

# Types of Processes

| Type | Description |
|---|---|
| Foreground Process | Runs directly in terminal |
| Background Process | Runs behind the terminal |
| Daemon Process | System/service process |

---

# Foreground Process

Foreground processes interact directly with the user.

Example:

```bash
ping google.com
```

Stop foreground process:

```bash
CTRL + C
```

---

# Background Process

Background processes run independently of the terminal.

## Run Process in Background

```bash
sleep 100 &
```

The `&` symbol sends the process to background.

---

# Process ID (PID)

Each process gets a unique Process ID.

Check current shell PID:

```bash
echo $$
```

---

# ps Command

## Purpose
Displays running processes.

## Syntax

```bash
ps
```

---

# Common ps Commands

## Show All Processes

```bash
ps -e
```

---

## Detailed Process Information

```bash
ps -ef
```

---

## Process for Specific User

```bash
ps -u username
```

---

# top Command

## Purpose
Displays real-time system and process monitoring.

## Syntax

```bash
top
```

Information shown:
- CPU usage
- Memory usage
- Running tasks
- Active processes

Exit top:

```bash
q
```

---

# htop Command

## Purpose
Interactive process monitoring tool.

## Install

### Ubuntu/Debian

```bash
sudo apt install htop
```

## Run

```bash
htop
```

Features:
- Better UI
- Interactive controls
- Colorful display

---

# kill Command

## Purpose
Terminates a process.

## Syntax

```bash
kill PID
```

## Example

```bash
kill 1234
```

---

# Force Kill Process

```bash
kill -9 PID
```

⚠️ Forcefully terminates process.

---

# pkill Command

## Purpose
Kills process using process name.

## Example

```bash
pkill nginx
```

---

# jobs Command

## Purpose
Displays background jobs.

## Syntax

```bash
jobs
```

---

# fg Command

## Purpose
Brings background process to foreground.

## Example

```bash
fg %1
```

---

# bg Command

## Purpose
Resumes stopped background process.

## Example

```bash
bg %1
```

---

# nohup Command

## Purpose
Runs process even after terminal closes.

## Example

```bash
nohup python app.py &
```

Output gets stored in:

```bash
nohup.out
```

---

# nice Command

## Purpose
Starts process with priority.

## Example

```bash
nice -n 10 process_name
```

---

# renice Command

## Purpose
Changes priority of running process.

## Example

```bash
renice 5 PID
```

---

# Process States in Linux

| State | Meaning |
|---|---|
| R | Running |
| S | Sleeping |
| Z | Zombie |
| T | Stopped |

---

# Important Process Monitoring Commands

| Command | Purpose |
|---|---|
| ps | View processes |
| top | Live monitoring |
| htop | Interactive monitoring |
| kill | Stop process |
| pkill | Kill by name |
| jobs | Show background jobs |
| nohup | Run after logout |

---

# Real-World DevOps Usage 🚀

Process management is heavily used in:
- Linux servers
- Docker containers
- Kubernetes nodes
- CI/CD runners
- Monitoring systems
- Application troubleshooting

DevOps engineers monitor and manage processes daily in production environments.

---

# Common Troubleshooting Example

## Find High CPU Process

```bash
top
```

---

## Kill Problematic Process

```bash
kill -9 PID
```

---

# Best Practices 🔥

✅ Avoid unnecessary force kills  
✅ Monitor CPU & memory regularly  
✅ Use nohup for long-running tasks  
✅ Understand process priority  
✅ Use htop for better visibility  

---

# Summary

Linux process management helps monitor, control, and troubleshoot running applications and services.  
Understanding process handling is essential for Linux administration, DevOps engineering, and cloud operations.

---

# Author

Siddharth Kanojia  
DevOps & Cloud Learning Journey 🚀
