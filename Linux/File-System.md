# 📂 Linux File System

> A beginner-friendly guide to understanding the Linux directory structure used in IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document explains the Linux file system hierarchy, the purpose of each major directory, and how they are used in real-world Linux administration.

---

# 📚 Table of Contents

1. What is the Linux File System?
2. Linux Directory Structure
3. Important Directories
4. Useful Commands
5. Best Practices
6. Interview Questions

---

# 🧠 What is the Linux File System?

The Linux file system is a hierarchical structure that organizes files and directories starting from a single root directory (`/`).

Unlike Windows, Linux does not use drive letters such as **C:** or **D:**. Everything in Linux starts from the root directory.

Example:

```

/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var

```

---

# 📁 Important Directories

## /

### 📌 Root Directory

The top-level directory of the Linux file system.

Everything begins here.

Example:

```bash
cd /
```

---

## /home

### 📌 User Home Directories

Stores personal files of normal users.

Example

```text
/home/faisal
```

Command

```bash
cd /home
```

---

## /root

### 📌 Root User Home

Home directory of the root (administrator) user.

```bash
cd /root
```

---

## /bin

### 📌 Essential User Commands

Contains important executable commands.

Examples

```text
ls
cp
mv
cat
pwd
```

---

## /sbin

### 📌 System Administration Commands

Contains commands mainly used by the system administrator.

Examples

```text
reboot
shutdown
fsck
```

---

## /etc

### 📌 Configuration Files

Stores system configuration files.

Examples

```text
/etc/passwd
/etc/hosts
/etc/fstab
```

Command

```bash
cd /etc
```

---

## /var

### 📌 Variable Data

Stores files that change frequently.

Examples

- Logs
- Cache
- Mail
- Print Queue

Important directory

```text
/var/log
```

---

## /tmp

### 📌 Temporary Files

Stores temporary files created by users and applications.

Example

```bash
cd /tmp
```

---

## /usr

### 📌 User Programs

Contains installed software and libraries.

Examples

```text
/usr/bin
/usr/lib
/usr/share
```

---

## /opt

### 📌 Optional Software

Stores third-party applications.

Example

```text
/opt/google
```

---

## /boot

### 📌 Boot Files

Contains files required to boot Linux.

Includes

- Kernel
- GRUB Boot Loader

---

## /dev

### 📌 Device Files

Represents hardware devices.

Examples

```text
/dev/sda
/dev/sdb
/dev/null
```

---

## /proc

### 📌 Process Information

Virtual directory containing information about running processes.

Example

```bash
cat /proc/cpuinfo
```

---

## /media

### 📌 Removable Devices

Automatically mounts USB drives and DVDs.

---

## /mnt

### 📌 Temporary Mount Point

Used for manually mounting file systems.

---

# 💻 Useful Commands

Display current directory

```bash
pwd
```

List files

```bash
ls -la
```

Change directory

```bash
cd
```

Display directory tree

```bash
tree
```

Show disk usage

```bash
df -h
```

Show folder size

```bash
du -sh
```

---

# 💡 Best Practices

- Never delete system directories.
- Avoid modifying `/etc` without understanding the configuration.
- Use `/home` for personal files.
- Store logs inside `/var/log`.
- Keep temporary files inside `/tmp`.

---

---

# 📖 References

- Linux Filesystem Hierarchy Standard (FHS)
- Ubuntu Documentation
- Red Hat Documentation

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
