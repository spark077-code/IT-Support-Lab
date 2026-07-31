# 🐧 Linux Basic Commands

> A beginner-friendly guide to essential Linux commands used in IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document introduces the most commonly used Linux commands. It is designed to help beginners understand how to navigate the Linux operating system, manage files and directories, monitor system resources, and perform basic administrative tasks.

---

# 📚 Table of Contents

1. Navigation Commands
2. File & Directory Commands
3. File Viewing Commands
4. Search Commands
5. User Commands
6. File Permission Commands
7. Process Management
8. Networking Commands
9. Disk Management Commands
10. System Information Commands
11. Archive & Compression
12. Useful Shortcuts
13. Best Practices
14. Interview Questions

---

# 📂 1. Navigation Commands

## pwd

### 📌 Purpose

Displays the current working directory.

### 🖥 Syntax

```bash
pwd
```

### 📋 Example

```bash
pwd
```

Output

```text
/home/faisal
```

---

## ls

### 📌 Purpose

Lists files and directories.

### 🖥 Syntax

```bash
ls
```

### Common Options

```bash
ls -l
ls -a
ls -lh
ls -la
```

| Option | Description |
|---------|-------------|
| -l | Long listing format |
| -a | Show hidden files |
| -h | Human-readable file sizes |

---

## cd

### 📌 Purpose

Changes the current directory.

### Examples

```bash
cd Documents
cd ..
cd /
cd ~
```

---

# 📁 2. File & Directory Commands

## mkdir

Create a new directory.

```bash
mkdir Projects
```

---

## rmdir

Remove an empty directory.

```bash
rmdir Test
```

---

## touch

Create an empty file.

```bash
touch notes.txt
```

---

## cp

Copy files.

```bash
cp file.txt backup.txt
```

Copy folders.

```bash
cp -r Folder Backup
```

---

## mv

Move or rename files.

```bash
mv file.txt Documents/
mv old.txt new.txt
```

---

## rm

Delete files.

```bash
rm file.txt
```

Delete directories.

```bash
rm -r Folder
```

⚠ Be careful.

`rm` permanently deletes files.

---

# 📄 3. File Viewing Commands

## cat

Display file contents.

```bash
cat file.txt
```

---

## less

Read large files.

```bash
less file.txt
```

Quit using

```
q
```

---

## head

Display first 10 lines.

```bash
head file.txt
```

---

## tail

Display last 10 lines.

```bash
tail file.txt
```

Live monitoring

```bash
tail -f logfile.log
```

---

# 🔍 4. Search Commands

## find

Search files.

```bash
find . -name "*.txt"
```

---

## grep

Search text inside files.

```bash
grep "admin" users.txt
```

Ignore case

```bash
grep -i admin users.txt
```

---

# 👤 5. User Commands

## whoami

Display current user.

```bash
whoami
```

---

## id

Display user ID.

```bash
id
```

---

## passwd

Change password.

```bash
passwd
```

---

# 🔐 6. File Permission Commands

## chmod

Change file permissions.

```bash
chmod 755 script.sh
```

---

## chown

Change file owner.

```bash
sudo chown user:user file.txt
```

---

# ⚙ 7. Process Management

## ps

Display running processes.

```bash
ps
```

All processes

```bash
ps aux
```

---

## top

Real-time process monitor.

```bash
top
```

---

## kill

Terminate a process.

```bash
kill PID
```

---

# 🌐 8. Networking Commands

## ip

Display network configuration.

```bash
ip a
```

Routing table

```bash
ip route
```

---

## ping

Test connectivity.

```bash
ping google.com
```

---

## ss

Display network sockets.

```bash
ss -tuln
```

---

## hostname

Display system hostname.

```bash
hostname
```

---

# 💾 9. Disk Management Commands

## df

Display disk usage.

```bash
df -h
```

---

## du

Display folder size.

```bash
du -sh Documents
```

---

## mount

Display mounted drives.

```bash
mount
```

---

# 🖥 10. System Information Commands

## uname

Display kernel information.

```bash
uname -a
```

---

## hostnamectl

Display system information.

```bash
hostnamectl
```

---

## uptime

Display system uptime.

```bash
uptime
```

---

## free

Display memory usage.

```bash
free -h
```

---

# 📦 11. Archive & Compression

Create archive

```bash
tar -cvf backup.tar Folder
```

Extract archive

```bash
tar -xvf backup.tar
```

Create ZIP

```bash
zip files.zip file.txt
```

Extract ZIP

```bash
unzip files.zip
```

---

# ⌨ Useful Shortcuts

| Shortcut | Description |
|----------|-------------|
| Ctrl + C | Stop current process |
| Ctrl + Z | Suspend process |
| Ctrl + D | Logout / End input |
| Ctrl + L | Clear terminal |
| Tab | Auto-complete |
| ↑ | Previous command |
| ↓ | Next command |
| history | Show command history |

---

# ✅ Best Practices

- Always verify commands before running them.
- Avoid using `rm -rf` unless you fully understand its impact.
- Use `sudo` only when necessary.
- Keep backups before making important changes.
- Use descriptive file and directory names.


---

# 📖 References

- Linux Manual Pages (`man`)
- Ubuntu Documentation
- Red Hat Documentation

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
