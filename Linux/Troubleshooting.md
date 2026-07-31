# 🛠 Linux Troubleshooting Guide

> A practical guide to diagnosing and resolving common Linux issues for IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document explains common Linux problems, their possible causes, troubleshooting techniques, useful commands, and best practices for resolving issues efficiently.

---

# 📚 Table of Contents

1. Troubleshooting Methodology
2. System Won't Boot
3. No Internet Connection
4. DNS Problems
5. SSH Connection Failed
6. Permission Denied
7. Disk Full
8. High CPU / Memory Usage
9. Service Not Running
10. Package Installation Failed
11. File Not Found
12. Useful Troubleshooting Commands
13. Best Practices
14. Common Mistakes
15. Interview Questions

---

# 🧠 Troubleshooting Methodology

Always follow a structured approach.

```

Identify the Problem
│
▼
Collect Information
│
▼
Check Logs
│
▼
Identify Possible Cause
│
▼
Test the Solution
│
▼
Verify the Fix
│
▼
Document the Resolution

```

---

# 🚀 1. System Won't Boot

## Possible Causes

- Corrupted bootloader
- Disk failure
- File system corruption
- Incorrect GRUB configuration

## Useful Commands

```bash
journalctl -xb
```

```bash
lsblk
```

```bash
fsck /dev/sda1
```

---

# 🌐 2. No Internet Connection

## Check IP Address

```bash
ip a
```

---

## Check Routing Table

```bash
ip route
```

---

## Test Gateway

```bash
ping 192.168.1.1
```

---

## Test Internet

```bash
ping 8.8.8.8
```

---

## Test DNS

```bash
ping google.com
```

If IP works but domain names don't, the issue is usually DNS.

---

# 🌍 3. DNS Problems

Check DNS configuration.

```bash
cat /etc/resolv.conf
```

DNS Lookup.

```bash
nslookup google.com
```

Detailed DNS Query.

```bash
dig google.com
```

---

# 🔐 4. SSH Connection Failed

Check SSH service.

```bash
systemctl status ssh
```

Restart SSH.

```bash
sudo systemctl restart ssh
```

Check listening ports.

```bash
ss -tuln
```

---

# 🔑 5. Permission Denied

Check permissions.

```bash
ls -l
```

Change permissions.

```bash
chmod 755 script.sh
```

Change owner.

```bash
sudo chown user:user script.sh
```

---

# 💾 6. Disk Full

Check disk usage.

```bash
df -h
```

Find large directories.

```bash
du -sh *
```

Delete unnecessary files.

---

# ⚡ 7. High CPU / Memory Usage

Display running processes.

```bash
top
```

or

```bash
htop
```

Find specific process.

```bash
ps aux
```

Terminate process.

```bash
kill PID
```

---

# ⚙ 8. Service Not Running

Check service.

```bash
systemctl status apache2
```

Start service.

```bash
sudo systemctl start apache2
```

Restart service.

```bash
sudo systemctl restart apache2
```

Enable at boot.

```bash
sudo systemctl enable apache2
```

---

# 📦 9. Package Installation Failed

Update package lists.

Ubuntu / Kali

```bash
sudo apt update
```

Rocky Linux

```bash
sudo dnf check-update
```

Check internet connectivity.

```bash
ping 8.8.8.8
```

---

# 📂 10. File Not Found

Check current directory.

```bash
pwd
```

List files.

```bash
ls -la
```

Search file.

```bash
find . -name filename.txt
```

---

# 💻 Useful Troubleshooting Commands

| Command | Purpose |
|----------|----------|
| pwd | Show current directory |
| ls -la | List files |
| ip a | Display IP address |
| ip route | Display routing table |
| ping | Test connectivity |
| nslookup | DNS lookup |
| dig | Detailed DNS query |
| ss -tuln | View listening ports |
| systemctl | Manage services |
| journalctl | View system logs |
| df -h | Check disk usage |
| du -sh | Check folder size |
| top | Monitor CPU & Memory |
| htop | Advanced system monitor |
| ps aux | List processes |
| kill | Stop a process |
| find | Search files |

---

# 💡 Best Practices

- Read error messages carefully.
- Check logs before making changes.
- Verify network connectivity step by step.
- Keep the system updated.
- Create backups before major changes.
- Document every solution.

---

# ⚠ Common Mistakes

❌ Deleting system files without understanding their purpose.

❌ Running every command as the root user.

❌ Ignoring log files.

❌ Killing important system processes.

❌ Forgetting to verify the solution.

---


---

# 📖 References

- Linux Manual Pages
- Ubuntu Documentation
- Kali Linux Documentation
- Rocky Linux Documentation

---

## 🔗 Related Documents

- [Linux README](README.md)
- [Basic Commands](Basic-Commands.md)
- [File System](File-System.md)
- [Users and Groups](Users-and-Groups.md)
- [File Permissions](File-Permissions.md)
- [Package Management](Package-Management.md)
- [Process Management](Process-Management.md)
- [Networking](Networking.md)
- [Bash Scripting](Bash-Scripting.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
