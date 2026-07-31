# 🌐 Linux Networking

> A beginner-friendly guide to Linux networking commands and troubleshooting for IT Support, System Administration, Networking, and Cyber Security.

---

# 📌 Objective

This document explains the most commonly used Linux networking commands for viewing network configuration, testing connectivity, troubleshooting network issues, and gathering network information.

---

# 📚 Table of Contents

1. What is Linux Networking?
2. Network Configuration
3. Connectivity Testing
4. DNS Commands
5. Routing Commands
6. Network Connections
7. Download & Transfer Commands
8. Troubleshooting Commands
9. Practical Lab
10. Best Practices
11. Common Mistakes
12. Interview Questions

---

# 🧠 What is Linux Networking?

Linux networking allows computers to communicate with each other using network interfaces, IP addresses, routing tables, and DNS servers.

A Network Administrator or IT Support Engineer uses networking commands to:

- Check IP addresses
- Test internet connectivity
- Verify DNS resolution
- Display routing tables
- Monitor network connections
- Troubleshoot network problems

---

# 🌍 Network Configuration

## ip

Displays and manages network interfaces.

```bash
ip a
```

or

```bash
ip addr
```

Example Output

```text
eth0    192.168.1.100/24
```

---

## Display Routing Table

```bash
ip route
```

Example

```text
default via 192.168.1.1 dev eth0
```

---

## Display Network Interfaces

```bash
ip link
```

---

## Show MAC Address

```bash
ip link show
```

---

# 📡 Connectivity Testing

## ping

Tests connectivity to another host.

```bash
ping google.com
```

Test using an IP address.

```bash
ping 8.8.8.8
```

Stop the command with:

```
Ctrl + C
```

---

## traceroute

Shows the path packets take to reach a destination.

```bash
traceroute google.com
```

If not installed:

Ubuntu / Kali

```bash
sudo apt install traceroute
```

Rocky Linux

```bash
sudo dnf install traceroute
```

---

# 🌐 DNS Commands

## nslookup

Looks up DNS information.

```bash
nslookup google.com
```

---

## dig

Provides detailed DNS information.

```bash
dig google.com
```

If not installed:

Ubuntu / Kali

```bash
sudo apt install dnsutils
```

Rocky Linux

```bash
sudo dnf install bind-utils
```

---

## hostname

Displays the system hostname.

```bash
hostname
```

---

## hostnamectl

Displays detailed hostname information.

```bash
hostnamectl
```

---

# 🛣 Routing Commands

## View Routing Table

```bash
ip route
```

---

## Add a Route

```bash
sudo ip route add 192.168.2.0/24 via 192.168.1.1
```

---

## Delete a Route

```bash
sudo ip route del 192.168.2.0/24
```

---

# 🔌 Network Connections

## ss

Displays active network sockets.

```bash
ss -tuln
```

---

## netstat

Displays network connections.

```bash
netstat -tuln
```

> Note: On modern Linux systems, `ss` is preferred over `netstat`.

---

# 📥 Download & Transfer Commands

## curl

Retrieve data from a URL.

```bash
curl https://example.com
```

---

## wget

Download files from the internet.

```bash
wget https://example.com/file.zip
```

---

# 🛠 Troubleshooting Commands

## Check IP Address

```bash
ip a
```

---

## Check Default Gateway

```bash
ip route
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

If `ping 8.8.8.8` works but `ping google.com` does not, the issue is likely DNS-related.

---

## Check Open Ports

```bash
ss -tuln
```

---

## Display Hostname

```bash
hostnamectl
```

---

# 💻 Practical Lab

## Task 1

Display IP configuration.

```bash
ip a
```

---

## Task 2

Display the routing table.

```bash
ip route
```

---

## Task 3

Ping Google's DNS server.

```bash
ping 8.8.8.8
```

---

## Task 4

Test DNS resolution.

```bash
nslookup google.com
```

---

## Task 5

View active network connections.

```bash
ss -tuln
```

---

## Task 6

Download a sample file.

```bash
wget https://example.com/file.zip
```

---

## Task 7

Display hostname information.

```bash
hostnamectl
```

---

# 💡 Best Practices

- Verify your IP address before troubleshooting.
- Test connectivity using both an IP address and a domain name.
- Keep network configuration documented.
- Use `ss` instead of `netstat` on modern Linux systems.
- Avoid changing routing tables unless you understand the impact.

---

# ⚠ Common Mistakes

❌ Assuming the internet is down without checking the IP configuration.

❌ Ignoring DNS when a website cannot be reached.

❌ Deleting the default route accidentally.

❌ Testing only with domain names instead of testing IP connectivity first.

---


---

# 📖 References

- Linux Manual Pages (`man ip`, `man ping`, `man ss`)
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

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
