# 🔐 Linux File Permissions

> A beginner-friendly guide to understanding Linux file permissions, ownership, and access control for IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document explains how Linux controls access to files and directories using permissions and ownership. It covers symbolic and numeric permissions, file ownership, and the most commonly used permission-related commands.

---

# 📚 Table of Contents

1. What are File Permissions?
2. Permission Types
3. Understanding `ls -l` Output
4. Symbolic Permissions
5. Numeric Permissions
6. Ownership
7. Permission Commands
8. Practical Lab
9. Best Practices
10. Common Mistakes
11. Interview Questions

---

# 🧠 What are File Permissions?

Linux uses permissions to control who can read, write, or execute files and directories.

Every file and directory has:

- Owner (User)
- Group
- Others

Example:

```bash
ls -l
```

Output:

```text
-rwxr-xr-- 1 faisal developers 2048 Jul 31 script.sh
```

---

# 📖 Understanding `ls -l`

```
-rwxr-xr--
│ │ │
│ │ └── Others
│ └──── Group
└────── Owner
```

| Symbol | Meaning |
|---------|---------|
| `-` | Regular file |
| `d` | Directory |
| `l` | Symbolic link |

---

# 🔑 Permission Types

| Permission | Symbol | Value | Description |
|------------|--------|------:|-------------|
| Read | r | 4 | View the contents of a file |
| Write | w | 2 | Modify a file |
| Execute | x | 1 | Run a file or enter a directory |

---

# 👤 Permission Categories

| Category | Description |
|----------|-------------|
| Owner (u) | The user who owns the file |
| Group (g) | Users in the assigned group |
| Others (o) | Everyone else |
| All (a) | Owner, Group, and Others |

---

# ✍ Symbolic Permissions

Grant execute permission to the owner:

```bash
chmod u+x script.sh
```

Remove write permission from the group:

```bash
chmod g-w script.sh
```

Give read permission to others:

```bash
chmod o+r script.sh
```

Give read permission to everyone:

```bash
chmod a+r script.sh
```

---

# 🔢 Numeric Permissions

Linux also supports numeric (octal) permissions.

| Number | Permission |
|--------:|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 3 | -wx |
| 2 | -w- |
| 1 | --x |
| 0 | --- |

### Common Examples

| Permission | Meaning |
|------------|---------|
| 777 | Full access for everyone (Not Recommended) |
| 755 | Owner: Full, Group: Read & Execute, Others: Read & Execute |
| 700 | Only the owner has full access |
| 644 | Owner can read/write, others can only read |
| 600 | Only the owner can read and write |

Example:

```bash
chmod 755 script.sh
```

---

# 👥 File Ownership

Check ownership:

```bash
ls -l
```

Change the file owner:

```bash
sudo chown faisal file.txt
```

Change owner and group:

```bash
sudo chown faisal:developers file.txt
```

Change group only:

```bash
sudo chgrp developers file.txt
```

---

# 🛠 Permission Commands

## chmod

Change file permissions.

```bash
chmod 644 notes.txt
```

```bash
chmod u+x script.sh
```

---

## chown

Change file owner.

```bash
sudo chown faisal file.txt
```

---

## chgrp

Change file group.

```bash
sudo chgrp developers file.txt
```

---

# 💻 Practical Lab

### Task 1

Create a file.

```bash
touch notes.txt
```

---

### Task 2

Check permissions.

```bash
ls -l
```

---

### Task 3

Give execute permission.

```bash
chmod +x notes.txt
```

---

### Task 4

Assign permission 755.

```bash
chmod 755 notes.txt
```

---

### Task 5

Assign permission 644.

```bash
chmod 644 notes.txt
```

---

### Task 6

Create a new directory.

```bash
mkdir Projects
```

Give full access to the owner only.

```bash
chmod 700 Projects
```

---

# 💡 Best Practices

- Follow the principle of least privilege.
- Avoid using `777` unless absolutely necessary.
- Give users only the permissions they require.
- Regularly review file permissions.
- Use groups to manage access efficiently.

---

# ⚠ Common Mistakes

❌ Using `chmod 777` on important files.

❌ Giving write access to everyone.

❌ Running everything as the root user.

❌ Forgetting to verify permissions after changes.



---

# 📖 References

- Linux Manual Pages (`man chmod`, `man chown`)
- Ubuntu Documentation
- Red Hat Documentation

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
