# 👥 Linux Users and Groups

> A beginner-friendly guide to managing users and groups in Linux for IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document explains how Linux manages users and groups, the difference between normal users and the root user, and how to create, modify, and manage user accounts securely.

---

# 📚 Table of Contents

1. What are Users and Groups?
2. Types of Users
3. Important Files
4. User Management Commands
5. Group Management Commands
6. Sudo and Root Access
7. Best Practices
8. Practical Lab
9. Interview Questions

---

# 🧠 What are Users and Groups?

Linux is a multi-user operating system, which means multiple users can use the same system independently.

Users are assigned to groups to simplify permission management and improve security.

---

# 👤 Types of Users

## Root User

The root user is the administrator of the Linux system.

Characteristics:

- Has full control over the system
- Can modify any file
- Can install or remove software
- Can manage all users

Check the current user:

```bash
whoami
```

Example Output

```text
root
```

---

## Normal User

A normal user has limited permissions.

Example

```text
faisal
```

Normal users cannot perform administrative tasks unless they use `sudo`.

---

## System Users

System users are created automatically for running services and applications.

Examples

```text
www-data
mysql
nobody
```

---

# 📂 Important Files

## /etc/passwd

Stores basic information about all users.

View the file:

```bash
cat /etc/passwd
```

---

## /etc/shadow

Stores encrypted user passwords.

```bash
sudo cat /etc/shadow
```

⚠ Only the root user can access this file.

---

## /etc/group

Stores group information.

```bash
cat /etc/group
```

---

# 👤 User Management Commands

## whoami

Displays the current logged-in user.

```bash
whoami
```

---

## id

Displays user ID (UID), group ID (GID), and group memberships.

```bash
id
```

---

## users

Shows users currently logged in.

```bash
users
```

---

## adduser

Creates a new user (user-friendly command).

```bash
sudo adduser ali
```

---

## useradd

Creates a new user (low-level command).

```bash
sudo useradd ahmed
```

---

## passwd

Sets or changes a user's password.

```bash
sudo passwd ali
```

---

## usermod

Modify an existing user.

Add user to the sudo group:

```bash
sudo usermod -aG sudo ali
```

---

## userdel

Delete a user account.

```bash
sudo userdel ali
```

Delete the user's home directory as well:

```bash
sudo userdel -r ali
```

---

# 👥 Group Management Commands

## groups

Shows the groups a user belongs to.

```bash
groups
```

---

## groupadd

Create a new group.

```bash
sudo groupadd developers
```

---

## groupdel

Delete a group.

```bash
sudo groupdel developers
```

---

## gpasswd

Add a user to a group.

```bash
sudo gpasswd -a ali developers
```

---

# 🔐 Sudo and Root Access

## sudo

Run a command with administrative privileges.

```bash
sudo apt update
```

---

## su

Switch to another user.

Become the root user:

```bash
su -
```

---

# 💻 Practical Lab

### Task 1

Check the current user.

```bash
whoami
```

---

### Task 2

Display your user ID.

```bash
id
```

---

### Task 3

Create a new user.

```bash
sudo adduser testuser
```

---

### Task 4

Create a new group.

```bash
sudo groupadd support
```

---

### Task 5

Add the user to the group.

```bash
sudo usermod -aG support testuser
```

---

### Task 6

Verify the user's groups.

```bash
groups testuser
```

---

# 💡 Best Practices

- Use a normal user for daily work.
- Use `sudo` only when administrative privileges are required.
- Assign users to groups instead of giving direct permissions.
- Remove unused user accounts.
- Use strong passwords.
- Avoid logging in directly as the root user.

---

# ⚠ Common Mistakes

❌ Working as the root user all the time.

❌ Forgetting the `-a` option when using `usermod -aG`.

❌ Giving unnecessary sudo access.

❌ Deleting user accounts without checking their data.

---

---

# 📖 References

- Linux Manual Pages (`man`)
- Ubuntu Documentation
- Red Hat Documentation

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
