# Linux Users & Permissions 👥🔐

<p align="center">
  <img src="./Rip1BLJtmJpWgQMMG0-5XTSa97p9NMgaIhuoGRdseROo5AM6KQjZb6AEAdDV640zF9nzvUy06nXHK2iB6CaS2Gg-cw-OI3FwKn8LoE-fG0EbNWYsrVO3I8LKzEZ2IRJk7jWGKZCNNU2D.jfif" width="900"/>
</p>

## Introduction

Linux is a multi-user operating system where multiple users can access and work on the same system securely.

To maintain security and control access, Linux uses:
- Users
- Groups
- File Permissions

Understanding users and permissions is essential for:
- System Administration
- DevOps
- Cloud Engineering
- Server Security

---

# Types of Users in Linux

| User Type | Description |
|---|---|
| Root User | Administrator with full access |
| Normal User | Regular user with limited permissions |
| System User | Used by services and applications |

---

# 1. Root User

The root user is the superuser in Linux.

Features:
- Full system access
- Can modify any file
- Can create/delete users
- Can install packages

Root prompt usually appears as:

```bash
root@server:#
```

Check current user:

```bash
whoami
```

---

# 2. Normal User

Regular users have limited access for security purposes.

Example:

```bash
/home/siddharth
```

Normal users cannot:
- Modify critical system files
- Install packages without sudo
- Access restricted directories

---

# 3. System Users

System users are created for services and applications.

Examples:
- nginx
- mysql
- docker

Check users list:

```bash
cat /etc/passwd
```

---

# Important User Files

| File | Purpose |
|---|---|
| /etc/passwd | User account information |
| /etc/shadow | Encrypted passwords |
| /etc/group | Group information |

---

# User Management Commands

# 1. useradd Command

## Purpose
Creates a new user.

## Syntax

```bash
sudo useradd username
```

## Example

```bash
sudo useradd devopsuser
```

---

# 2. passwd Command

## Purpose
Sets password for user.

## Syntax

```bash
sudo passwd username
```

## Example

```bash
sudo passwd devopsuser
```

---

# 3. userdel Command

## Purpose
Deletes a user.

## Syntax

```bash
sudo userdel username
```

## Example

```bash
sudo userdel devopsuser
```

---

# 4. id Command

## Purpose
Displays user and group IDs.

## Syntax

```bash
id username
```

## Example

```bash
id siddharth
```

---

# 5. whoami Command

## Purpose
Shows current logged-in user.

```bash
whoami
```

---

# Linux Groups

Groups help manage permissions for multiple users.

Example:
- Developers group
- Admin group
- Docker group

---

# Group Management Commands

# 1. groupadd Command

## Purpose
Creates a new group.

## Syntax

```bash
sudo groupadd groupname
```

## Example

```bash
sudo groupadd devops
```

---

# 2. usermod Command

## Purpose
Adds user to group.

## Syntax

```bash
sudo usermod -aG groupname username
```

## Example

```bash
sudo usermod -aG devops siddharth
```

---

# File Ownership in Linux

Each file has:
- Owner
- Group
- Permissions

Check ownership:

```bash
ls -l
```

Example output:

```bash
-rw-r--r-- 1 siddharth devops 0 May 16 notes.txt
```

---

# Understanding Permissions

```bash
-rwxr-xr--
```

Breakdown:

| Symbol | Meaning |
|---|---|
| r | Read |
| w | Write |
| x | Execute |

---

# Permission Categories

| Category | Meaning |
|---|---|
| User (u) | File owner |
| Group (g) | Group members |
| Others (o) | Everyone else |

---

# Permission Structure

```text
-rwxr-xr--
```

| Section | Meaning |
|---|---|
| rwx | User permissions |
| r-x | Group permissions |
| r-- | Others permissions |

---

# chmod Command

## Purpose
Changes file permissions.

## Syntax

```bash
chmod permissions filename
```

---

# Symbolic Method

## Example

```bash
chmod u+x script.sh
```

| Symbol | Meaning |
|---|---|
| u | User |
| g | Group |
| o | Others |
| + | Add permission |
| - | Remove permission |

---

# Numeric Method

| Number | Permission |
|---|---|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |

---

# Examples

## Full Permission

```bash
chmod 777 file.txt
```

⚠️ Not recommended in production.

---

## Common Secure Permission

```bash
chmod 755 script.sh
```

Meaning:
- Owner → rwx
- Group → r-x
- Others → r-x

---

# chown Command

## Purpose
Changes file ownership.

## Syntax

```bash
sudo chown owner filename
```

## Example

```bash
sudo chown siddharth notes.txt
```

---

# Change Owner and Group

```bash
sudo chown siddharth:devops notes.txt
```

---

# sudo Command

## Purpose
Runs commands with administrative privileges.

## Example

```bash
sudo apt update
```

---

# Important Permission Examples

## Give Execute Permission

```bash
chmod +x script.sh
```

---

## Remove Write Permission

```bash
chmod -w file.txt
```

---

# Special Permissions (Introduction)

| Permission | Purpose |
|---|---|
| SUID | Run as file owner |
| SGID | Run as group owner |
| Sticky Bit | Restricted deletion |

---

# Real-World DevOps Usage 🚀

Linux users and permissions are important for:
- Server security
- CI/CD pipelines
- Docker containers
- Kubernetes clusters
- SSH access control
- Automation scripts

DevOps engineers manage permissions daily in production environments.

---

# Quick Revision Table

| Command | Purpose |
|---|---|
| useradd | Create user |
| passwd | Set password |
| userdel | Delete user |
| groupadd | Create group |
| usermod | Add user to group |
| chmod | Change permissions |
| chown | Change ownership |
| sudo | Run admin commands |

---

# Best Practices 🔥

✅ Follow least privilege principle  
✅ Avoid using 777 permissions  
✅ Use groups for permission management  
✅ Restrict root access  
✅ Use sudo carefully

---

# Summary

Linux users and permissions provide security and controlled access to files, directories, and system resources.  
Understanding permission management is essential for Linux administration, DevOps engineering, and cloud infrastructure management.

---

# Author

Siddharth Kanojia  
DevOps & Cloud Learning Journey 🚀