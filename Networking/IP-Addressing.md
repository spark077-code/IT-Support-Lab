# 🌍 IP Addressing

> A beginner-friendly guide to understanding IPv4 addressing, address classes, private/public IPs, subnet masks, and IP configuration for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains the fundamentals of IP addressing, including IPv4 structure, address classes, subnet masks, public and private IP addresses, and common IP configuration commands.

---

# 📚 Table of Contents

1. What is an IP Address?
2. Why is IP Addressing Important?
3. IPv4 Address Structure
4. IP Address Classes
5. Public vs Private IP Addresses
6. Special IP Addresses
7. Subnet Mask
8. CIDR Notation
9. Static vs Dynamic IP
10. Common Networking Commands
11. Practical Lab
12. Best Practices
13. Common Mistakes
14. Interview Questions

---

# 🧠 What is an IP Address?

An IP (Internet Protocol) Address is a unique logical address assigned to every device connected to a network.

It allows devices to identify and communicate with each other.

Examples:

```
192.168.1.10
10.0.0.5
172.16.1.100
8.8.8.8
```

---

# 🎯 Why is IP Addressing Important?

IP addressing helps devices:

- Communicate over a network
- Send and receive data
- Identify source and destination devices
- Access the Internet
- Route packets correctly

---

# 🏗 IPv4 Address Structure

An IPv4 address consists of:

- 32 bits
- 4 Octets
- Each octet contains 8 bits

Example:

```
192.168.1.10
```

Binary Representation:

```
11000000.10101000.00000001.00001010
```

---

# 📋 IP Address Classes

| Class | Range | Default Subnet Mask | Typical Use |
|--------|-----------------|-----------------|----------------|
| A | 1.0.0.0 - 126.255.255.255 | 255.0.0.0 | Large Networks |
| B | 128.0.0.0 - 191.255.255.255 | 255.255.0.0 | Medium Networks |
| C | 192.0.0.0 - 223.255.255.255 | 255.255.255.0 | Small Networks |
| D | 224.0.0.0 - 239.255.255.255 | N/A | Multicast |
| E | 240.0.0.0 - 255.255.255.255 | N/A | Experimental |

---

# 🌐 Public vs Private IP Addresses

## Public IP Address

- Assigned by an Internet Service Provider (ISP)
- Globally unique
- Accessible over the Internet

Example:

```
8.8.8.8
```

---

## Private IP Address

Used within local networks.

### Class A

```
10.0.0.0 – 10.255.255.255
```

### Class B

```
172.16.0.0 – 172.31.255.255
```

### Class C

```
192.168.0.0 – 192.168.255.255
```

Private IP addresses are not routable on the public Internet.

---

# ⭐ Special IP Addresses

| Address | Purpose |
|----------|----------|
| 127.0.0.1 | Loopback |
| 0.0.0.0 | Default Route / Unspecified |
| 255.255.255.255 | Broadcast |
| APIPA (169.254.x.x) | Automatic Private IP Addressing |

---

# 🛡 Subnet Mask

A subnet mask separates the network portion from the host portion of an IP address.

Example:

```
IP Address : 192.168.1.25

Subnet Mask: 255.255.255.0
```

This means:

Network:

```
192.168.1.0
```

Host:

```
25
```

---

# 📏 CIDR Notation

CIDR (Classless Inter-Domain Routing) is a compact way to represent subnet masks.

| CIDR | Subnet Mask |
|------|----------------|
| /8 | 255.0.0.0 |
| /16 | 255.255.0.0 |
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |
| /30 | 255.255.255.252 |

---

# 🔄 Static vs Dynamic IP

## Static IP

- Manually configured
- Does not change automatically
- Commonly used for servers, routers, printers

---

## Dynamic IP

- Assigned automatically by DHCP
- Can change over time
- Commonly used for end-user devices

---

# 💻 Common Networking Commands

## Linux

Display IP Address

```bash
ip a
```

Display Routing Table

```bash
ip route
```

Display Hostname

```bash
hostname
```

---

## Windows

Display IP Configuration

```cmd
ipconfig
```

Detailed Configuration

```cmd
ipconfig /all
```

Display Routing Table

```cmd
route print
```

---

# 🧪 Practical Lab

## Task 1

Display your IP address.

Linux

```bash
ip a
```

Windows

```cmd
ipconfig
```

---

## Task 2

Identify:

- IP Address
- Subnet Mask
- Default Gateway

---

## Task 3

Ping another device on the same network.

```bash
ping 192.168.1.1
```

---

## Task 4

Ping Google's DNS server.

```bash
ping 8.8.8.8
```

---

## Task 5

Find your routing table.

Linux

```bash
ip route
```

Windows

```cmd
route print
```

---

# 💡 Best Practices

- Use private IP addresses inside local networks.
- Avoid duplicate IP addresses.
- Document static IP assignments.
- Verify subnet masks during configuration.
- Reserve static IPs for infrastructure devices.

---

# ⚠ Common Mistakes

❌ Configuring duplicate IP addresses.

❌ Using the wrong subnet mask.

❌ Incorrect default gateway configuration.

❌ Confusing public and private IP addresses.

❌ Forgetting to verify network settings after configuration.

---

# 🎯 Interview Questions

1. What is an IP address?
2. What is the difference between IPv4 and IPv6?
3. What is the difference between a public and private IP address?
4. What is a subnet mask?
5. What is CIDR notation?
6. What is the purpose of the default gateway?
7. What is the loopback address?
8. What is APIPA?
9. What is the difference between a static IP and a dynamic IP?
10. Which private IP ranges are defined by RFC 1918?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- CompTIA Network+
- RFC 791 (Internet Protocol)
- RFC 1918 (Private Addressing)

---

## 🔗 Related Documents

- [Networking README](README.md)
- [OSI Model](OSI-Model.md)
- [TCP-IP](TCP-IP.md)
- [Subnetting](Subnetting.md)
- [DHCP](DHCP.md)
- [Routing](Routing.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
