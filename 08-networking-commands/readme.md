# Linux Networking Basics 🌐🐧

<p align="center">
  <img src="./ChatGPT Image Jun 13, 2026, 08_31_28 PM.png" width="950"/>
</p>

## Introduction

Networking is the foundation of communication between computers, servers, applications, and cloud services.

In Linux, networking allows systems to exchange data over local networks and the internet.

Understanding networking is essential for:

* Linux Administration
* DevOps Engineering
* Cloud Computing
* Kubernetes
* System Troubleshooting

---

# What is Networking?

Networking is the process of connecting multiple devices to communicate and share resources.

Examples:

* Accessing a website
* Connecting to a database
* Using SSH to access a server
* Downloading packages using APT

---

# Key Networking Components

| Component   | Description                           |
| ----------- | ------------------------------------- |
| IP Address  | Unique address of a device            |
| Subnet Mask | Defines network boundaries            |
| Gateway     | Connects networks                     |
| DNS         | Converts domain names to IP addresses |
| Port        | Communication endpoint                |
| Protocol    | Rules for communication               |

---

# IP Address

An IP Address uniquely identifies a device on a network.

Example:

```text
192.168.1.10
```

Types:

### Private IP

```text
192.168.x.x
10.x.x.x
172.16.x.x - 172.31.x.x
```

### Public IP

Used on the internet and globally reachable.

---

# Check IP Address

## Modern Command

```bash
ip addr
```

---

## Short Form

```bash
ip a
```

---

# Hostname

Hostname is the name assigned to a Linux machine.

Check hostname:

```bash
hostname
```

Example:

```text
web-server-01
```

---

# DNS (Domain Name System)

DNS converts human-readable names into IP addresses.

Example:

```text
google.com → 142.250.x.x
```

Check DNS configuration:

```bash
cat /etc/resolv.conf
```

---

# Ping Command

Used to test network connectivity.

Example:

```bash
ping google.com
```

Output:

```text
64 bytes from ...
```

Stop:

```bash
CTRL + C
```

---

# Traceroute

Shows the path packets take to reach a destination.

Install:

```bash
sudo apt install traceroute
```

Run:

```bash
traceroute google.com
```

---

# Netstat Command

Displays network connections and listening ports.

Example:

```bash
netstat -tuln
```

Options:

| Option | Meaning   |
| ------ | --------- |
| -t     | TCP       |
| -u     | UDP       |
| -l     | Listening |
| -n     | Numeric   |

---

# ss Command

Modern replacement for netstat.

Example:

```bash
ss -tuln
```

---

# Check Open Ports

```bash
ss -tulpn
```

Useful for troubleshooting services.

---

# Curl Command

Used to transfer data from servers.

Example:

```bash
curl google.com
```

Check public IP:

```bash
curl ifconfig.me
```

---

# Wget Command

Download files from the internet.

Example:

```bash
wget https://example.com/file.zip
```

---

# Network Interfaces

Network interfaces connect Linux systems to networks.

View interfaces:

```bash
ip link show
```

Common Interface Names:

```text
eth0
ens33
enp0s3
wlan0
```

---

# Routing Table

Shows how packets travel across networks.

View routing table:

```bash
ip route
```

Example:

```text
default via 192.168.1.1
```

---

# SSH (Secure Shell)

Used for secure remote access.

Connect:

```bash
ssh user@server-ip
```

Example:

```bash
ssh ubuntu@192.168.1.20
```

---

# Common Networking Commands

| Command    | Purpose              |
| ---------- | -------------------- |
| ip a       | View IP Address      |
| hostname   | View hostname        |
| ping       | Test connectivity    |
| traceroute | Trace network path   |
| ss         | View ports           |
| curl       | Access web resources |
| wget       | Download files       |
| ip route   | View routing table   |
| ssh        | Remote access        |

---

# OSI Model Overview

| Layer | Function     |
| ----- | ------------ |
| 7     | Application  |
| 6     | Presentation |
| 5     | Session      |
| 4     | Transport    |
| 3     | Network      |
| 2     | Data Link    |
| 1     | Physical     |

Networking troubleshooting often relies on understanding OSI layers.

---

# Real-World DevOps Usage 🚀

Networking is used daily in:

* Cloud Infrastructure
* Kubernetes Clusters
* Docker Networking
* Load Balancers
* Application Deployment
* Monitoring Systems
* CI/CD Pipelines

Examples:

* Accessing remote servers via SSH
* Checking open ports
* Troubleshooting connectivity issues
* Configuring DNS
* Managing cloud networks

---

# Basic Troubleshooting Workflow

## Check IP Address

```bash
ip a
```

---

## Verify Connectivity

```bash
ping google.com
```

---

## Check Open Ports

```bash
ss -tulpn
```

---

## Verify Routes

```bash
ip route
```

---

## Test DNS Resolution

```bash
nslookup google.com
```

---

# Best Practices 🔥

✅ Use SSH instead of Telnet

✅ Keep ports secured

✅ Verify DNS configuration

✅ Monitor open network ports

✅ Understand routing basics

✅ Troubleshoot step-by-step

---

# Summary

Linux Networking Basics provide the foundation for communication between systems, servers, and cloud services.

A strong understanding of networking is essential for Linux Administration, DevOps Engineering, Cloud Computing, and Infrastructure Management.

---

# Author

Siddharth Kanojia

Building my DevOps journey through Linux, Automation, Cloud, and Real-World Projects 🚀
