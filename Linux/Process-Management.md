# ⚙️ Linux Process Management

> A beginner-friendly guide to managing processes in Linux for IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document explains how Linux processes work and how to monitor, control, and manage them using common Linux commands.

---

# 📚 Table of Contents

1. What is a Process?
2. Process States
3. Viewing Processes
4. Monitoring Processes
5. Managing Processes
6. Background & Foreground Jobs
7. System Services
8. Practical Lab
9. Best Practices
10. Common Mistakes
11. Interview Questions

---

# 🧠 What is a Process?

A process is a running instance of a program.

Examples:

- Firefox
- Google Chrome
- Apache Server
- SSH Service
- Nmap Scan

Every process has a unique Process ID (PID).

---

# 📌 Process States

A Linux process can be in different states.

| State | Meaning |
|---------|----------|
| R | Running |
| S | Sleeping |
| T | Stopped |
| Z | Zombie |

---

# 👀 Viewing Processes

## ps

Displays currently running processes.

```bash
ps
```

---

## ps -ef

Displays all running processes.

```bash
ps -ef
```

---

## ps aux

Shows detailed process information.

```bash
ps aux
```

---

# 📊 Monitoring Processes

## top

Displays running processes in real time.

```bash
top
```

Quit:

```
q
```

---

## htop

An improved version of `top`.

```bash
htop
```

> Note: Install `htop` first if it is not available.

Ubuntu/Kali:

```bash
sudo apt install htop
```

Rocky Linux:

```bash
sudo dnf install htop
```

---

# ❌ Managing Processes

## kill

Terminates a process using its PID.

```bash
kill 1234
```

---

## kill -9

Forcefully terminates a process.

```bash
kill -9 1234
```

---

## killall

Terminates all processes with the same name.

```bash
killall firefox
```

---

## pkill

Terminates processes by name or pattern.

```bash
pkill chrome
```

---

# 🎯 Background & Foreground Jobs

## Run a process in the background

```bash
firefox &
```

---

## jobs

Displays background jobs.

```bash
jobs
```

---

## bg

Resume a stopped job in the background.

```bash
bg
```

---

## fg

Bring a background job to the foreground.

```bash
fg
```

---

# 🖥️ System Services

Linux services are managed using `systemctl`.

---

## Check Service Status

```bash
systemctl status ssh
```

---

## Start a Service

```bash
sudo systemctl start ssh
```

---

## Stop a Service

```bash
sudo systemctl stop ssh
```

---

## Restart a Service

```bash
sudo systemctl restart ssh
```

---

## Enable Service at Boot

```bash
sudo systemctl enable ssh
```

---

## Disable Service

```bash
sudo systemctl disable ssh
```

---

## List Running Services

```bash
systemctl list-units --type=service
```

---

# 💻 Practical Lab

## Task 1

Display all running processes.

```bash
ps aux
```

---

## Task 2

Monitor the system.

```bash
top
```

---

## Task 3

Install htop.

Kali Linux

```bash
sudo apt install htop
```

Rocky Linux

```bash
sudo dnf install htop
```

Launch it.

```bash
htop
```

---

## Task 4

Find the PID of Firefox.

```bash
ps aux | grep firefox
```

---

## Task 5

Terminate Firefox.

```bash
kill PID
```

Replace `PID` with the actual process ID.

---

## Task 6

Check the SSH service.

```bash
systemctl status ssh
```

---

## Task 7

Restart the SSH service.

```bash
sudo systemctl restart ssh
```

---

# 💡 Best Practices

- Verify the process before terminating it.
- Avoid using `kill -9` unless necessary.
- Monitor system resources regularly.
- Use `systemctl` to manage services instead of killing service processes directly.
- Investigate high CPU or memory usage before stopping processes.

---

# ⚠ Common Mistakes

❌ Killing critical system processes.

❌ Using `kill -9` without trying a normal `kill` first.

❌ Forgetting to check the correct PID.

❌ Stopping important services accidentally.

---



---

# 📖 References

- Linux Manual Pages (`man ps`, `man kill`, `man systemctl`)
- Ubuntu Documentation
- Red Hat Documentation
- Rocky Linux Documentation

---

## 🔗 Related Documents

- [Linux README](README.md)
- [Basic Commands](Basic-Commands.md)
- [File System](File-System.md)
- [Users and Groups](Users-and-Groups.md)
- [File Permissions](File-Permissions.md)
- [Package Management](Package-Management.md)
- [Networking](Networking.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
