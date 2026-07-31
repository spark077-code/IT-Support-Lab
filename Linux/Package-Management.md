# 📦 Linux Package Management

> A beginner-friendly guide to installing, updating, removing, and managing software packages in Linux using APT and DNF.

---

# 📌 Objective

This document explains how package management works in Linux and demonstrates how to install, update, search, and remove software using the most common package managers.

---

# 📚 Table of Contents

1. What is Package Management?
2. Common Package Managers
3. APT Commands (Ubuntu / Kali)
4. DNF Commands (Rocky Linux / RHEL)
5. Installing Software
6. Updating Packages
7. Removing Packages
8. Searching Packages
9. Practical Lab
10. Best Practices
11. Common Mistakes
12. Interview Questions

---

# 🧠 What is Package Management?

Package Management is the process of installing, updating, removing, and maintaining software in a Linux operating system.

Instead of downloading software from websites, Linux uses package managers to install applications from trusted repositories.

Benefits:

- Easy software installation
- Automatic dependency management
- Security updates
- Easy software removal
- Centralized software repositories

---

# 📦 Common Package Managers

| Distribution | Package Manager |
|--------------|-----------------|
| Ubuntu | APT |
| Debian | APT |
| Kali Linux | APT |
| Rocky Linux | DNF |
| RHEL | DNF |
| Fedora | DNF |

---

# 🟢 APT (Ubuntu / Kali Linux)

## Update Package List

```bash
sudo apt update
```

Downloads the latest package information from configured repositories.

---

## Upgrade Installed Packages

```bash
sudo apt upgrade
```

Installs the latest available versions of installed packages.

---

## Install a Package

Example:

```bash
sudo apt install nmap
```

---

## Remove a Package

```bash
sudo apt remove nmap
```

---

## Remove Package and Configuration Files

```bash
sudo apt purge nmap
```

---

## Remove Unused Dependencies

```bash
sudo apt autoremove
```

---

## Search for a Package

```bash
apt search wireshark
```

---

## Show Package Information

```bash
apt show wireshark
```

---

## List Installed Packages

```bash
apt list --installed
```

---

# 🔵 DNF (Rocky Linux / RHEL)

## Check for Updates

```bash
sudo dnf check-update
```

---

## Upgrade System

```bash
sudo dnf upgrade
```

---

## Install a Package

```bash
sudo dnf install nmap
```

---

## Remove a Package

```bash
sudo dnf remove nmap
```

---

## Search for a Package

```bash
dnf search wireshark
```

---

## Display Package Information

```bash
dnf info wireshark
```

---

## List Installed Packages

```bash
dnf list installed
```

---

## Clean Cached Files

```bash
sudo dnf clean all
```

---

# 📥 Installing Software

Example (Kali Linux)

```bash
sudo apt install wireshark
```

Example (Rocky Linux)

```bash
sudo dnf install wireshark
```

---

# 🔄 Updating the System

Kali Linux

```bash
sudo apt update

sudo apt upgrade
```

Rocky Linux

```bash
sudo dnf check-update

sudo dnf upgrade
```

---

# ❌ Removing Software

APT

```bash
sudo apt remove package-name
```

DNF

```bash
sudo dnf remove package-name
```

---

# 🔍 Searching for Software

APT

```bash
apt search package-name
```

DNF

```bash
dnf search package-name
```

---

# 💻 Practical Lab

## Task 1

Update package information.

```bash
sudo apt update
```

---

## Task 2

Install Nmap.

```bash
sudo apt install nmap
```

---

## Task 3

Verify installation.

```bash
nmap --version
```

---

## Task 4

Search for Wireshark.

```bash
apt search wireshark
```

---

## Task 5

Display package information.

```bash
apt show wireshark
```

---

## Task 6

Remove Nmap.

```bash
sudo apt remove nmap
```

---

# 💡 Best Practices

- Always run `apt update` before installing new software.
- Install software only from trusted repositories.
- Keep your system updated regularly.
- Remove unused packages using `autoremove`.
- Read package information before installation.

---

# ⚠ Common Mistakes

❌ Installing software without updating package lists.

❌ Removing important system packages.

❌ Ignoring dependency warnings.

❌ Mixing package managers unnecessarily.



---

# 📖 References

- Ubuntu Documentation
- Kali Linux Documentation
- Rocky Linux Documentation
- Red Hat Documentation

---

## 🔗 Related Documents

- [Linux README](README.md)
- [Basic Commands](Basic-Commands.md)
- [File System](File-System.md)
- [Users and Groups](Users-and-Groups.md)
- [File Permissions](File-Permissions.md)
- [Process Management](Process-Management.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
