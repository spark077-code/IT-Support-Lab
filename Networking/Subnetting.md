# 🌐 Subnetting

> A beginner-friendly guide to understanding IPv4 subnetting for Networking, IT Support, CCNA, and Cyber Security.

---

# 📌 Objective

This document explains the fundamentals of IPv4 subnetting, including subnet masks, CIDR notation, network IDs, broadcast addresses, valid host ranges, and practical subnetting examples.

---

# 📚 Table of Contents

1. What is Subnetting?
2. Why is Subnetting Important?
3. Binary Basics
4. Subnet Mask
5. CIDR Notation
6. Network ID
7. Broadcast Address
8. Valid Host Range
9. Hosts Per Subnet
10. Common Subnets
11. Solved Examples
12. VLSM Introduction
13. Practical Lab
14. Best Practices
15. Common Mistakes
16. Interview Questions

---

# 🧠 What is Subnetting?

Subnetting is the process of dividing one large IP network into multiple smaller networks (subnets).

Instead of having one large broadcast domain, subnetting creates smaller and more efficient networks.

---

# 🎯 Why is Subnetting Important?

Subnetting helps to:

- Reduce network congestion
- Improve performance
- Improve security
- Reduce broadcast traffic
- Use IP addresses efficiently
- Simplify network management

---

# 🔢 Binary Basics

Each IPv4 address contains **32 bits**.

Example:

```
192.168.1.10
```

Binary:

```
11000000.10101000.00000001.00001010
```

Each octet contains **8 bits**.

---

# 🛡 Subnet Mask

A subnet mask separates the network portion from the host portion of an IP address.

Example:

```
IP Address

192.168.1.25

Subnet Mask

255.255.255.0
```

This means:

Network Portion

```
192.168.1
```

Host Portion

```
25
```

---

# 📏 CIDR Notation

CIDR is a shorter way of writing subnet masks.

| CIDR | Subnet Mask |
|------|----------------|
| /24 | 255.255.255.0 |
| /25 | 255.255.255.128 |
| /26 | 255.255.255.192 |
| /27 | 255.255.255.224 |
| /28 | 255.255.255.240 |
| /29 | 255.255.255.248 |
| /30 | 255.255.255.252 |

---

# 🌍 Network ID

The Network ID identifies the subnet.

Example:

```
IP Address

192.168.1.100

Mask

255.255.255.0
```

Network ID

```
192.168.1.0
```

---

# 📢 Broadcast Address

The Broadcast Address is used to send data to all devices in the subnet.

Example:

```
Network

192.168.1.0/24
```

Broadcast Address

```
192.168.1.255
```

---

# 👥 Valid Host Range

For:

```
192.168.1.0/24
```

Network ID

```
192.168.1.0
```

Broadcast

```
192.168.1.255
```

Usable Hosts

```
192.168.1.1

↓

192.168.1.254
```

---

# 🧮 Hosts Per Subnet

Formula:

```
2^Host Bits - 2
```

Example:

```
/24
```

Host Bits

```
8
```

Calculation

```
2^8 - 2

256 - 2

254 Hosts
```

---

# 📊 Common Subnets

| CIDR | Mask | Hosts |
|------|----------------|------:|
| /24 | 255.255.255.0 | 254 |
| /25 | 255.255.255.128 | 126 |
| /26 | 255.255.255.192 | 62 |
| /27 | 255.255.255.224 | 30 |
| /28 | 255.255.255.240 | 14 |
| /29 | 255.255.255.248 | 6 |
| /30 | 255.255.255.252 | 2 |

---

# 📝 Solved Example 1

Network:

```
192.168.10.0/24
```

| Item | Value |
|------|-------|
| Network ID | 192.168.10.0 |
| First Host | 192.168.10.1 |
| Last Host | 192.168.10.254 |
| Broadcast | 192.168.10.255 |
| Hosts | 254 |

---

# 📝 Solved Example 2

Network:

```
192.168.20.0/26
```

| Item | Value |
|------|-------|
| Network ID | 192.168.20.0 |
| First Host | 192.168.20.1 |
| Last Host | 192.168.20.62 |
| Broadcast | 192.168.20.63 |
| Hosts | 62 |

---

# 📝 Solved Example 3

Network:

```
10.10.10.64/27
```

| Item | Value |
|------|-------|
| Network ID | 10.10.10.64 |
| First Host | 10.10.10.65 |
| Last Host | 10.10.10.94 |
| Broadcast | 10.10.10.95 |
| Hosts | 30 |

---

# 🚀 Introduction to VLSM

VLSM (Variable Length Subnet Mask) allows different subnet sizes within the same network.

Advantages:

- Efficient IP address utilization
- Supports networks of different sizes
- Reduces address wastage

---

# 💻 Practical Lab

## Task 1

Find the following for:

```
192.168.5.0/24
```

- Network ID
- Broadcast Address
- First Host
- Last Host

---

## Task 2

Calculate usable hosts for:

```
/26
```

---

## Task 3

Create two subnets from:

```
192.168.1.0/24
```

using:

```
/25
```

---

## Task 4

In Cisco Packet Tracer:

- Add 2 Routers
- Add 2 Switches
- Add 4 PCs
- Assign IP addresses from different subnets
- Verify connectivity using `ping`

---

# 💡 Best Practices

- Plan IP addressing before deployment.
- Avoid overlapping subnets.
- Document subnet allocations.
- Reserve IP addresses for infrastructure devices.
- Verify subnet calculations before configuration.

---

# ⚠ Common Mistakes

❌ Using the Network ID as a host address.

❌ Using the Broadcast Address as a host address.

❌ Incorrect subnet mask configuration.

❌ Overlapping subnets.

❌ Forgetting to update routing after subnetting.

---

# 🎯 Interview Questions

1. What is subnetting?
2. Why is subnetting used?
3. What is CIDR notation?
4. What is a subnet mask?
5. What is the Network ID?
6. What is the Broadcast Address?
7. How do you calculate usable hosts?
8. What is the formula for hosts per subnet?
9. What is VLSM?
10. What is the difference between a /24 and a /26 network?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- CompTIA Network+
- RFC 950
- RFC 4632

---

## 🔗 Related Documents

- [Networking README](README.md)
- [OSI Model](OSI-Model.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [VLAN](VLAN.md)
- [Routing](Routing.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
