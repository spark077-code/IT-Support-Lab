# 🌐 Network Address Translation (NAT)

> A beginner-friendly guide to understanding Network Address Translation (NAT), its types, working process, configuration concepts, and troubleshooting for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains what NAT is, why it is used, the different types of NAT, how address translation works, and how to troubleshoot common NAT issues.

---

# 📚 Table of Contents

1. What is NAT?
2. Why is NAT Needed?
3. How NAT Works
4. Types of NAT
5. Inside Local vs Inside Global
6. NAT Translation Process
7. Basic Cisco NAT Configuration
8. Common NAT Commands
9. NAT Troubleshooting
10. Practical Lab
11. Best Practices
12. Common Mistakes
13. Interview Questions

---

# 🧠 What is NAT?

Network Address Translation (NAT) is a process that translates private IP addresses into public IP addresses (and vice versa).

It allows devices using private IP addresses to communicate with the Internet through one or more public IP addresses.

---

# 🎯 Why is NAT Needed?

NAT provides several benefits:

- Conserves public IPv4 addresses
- Allows private networks to access the Internet
- Hides internal IP addresses
- Improves network security
- Simplifies network administration

Without NAT, every device would require its own public IP address.

---

# ⚙️ How NAT Works

Example:

```
PC

192.168.1.10

↓

Router (NAT)

↓

Public IP

203.0.113.10

↓

Internet
```

The router replaces the private source IP with its public IP before forwarding packets to the Internet.

When the reply returns, the router translates the public IP back to the original private IP.

---

# 📂 Types of NAT

## 1. Static NAT

One private IP maps to one public IP.

Example:

```
192.168.1.10

↓

203.0.113.10
```

Used for:

- Web Servers
- Mail Servers
- Public Services

---

## 2. Dynamic NAT

Maps private IP addresses to a pool of public IP addresses.

Example:

```
Private IP Pool

↓

Public IP Pool
```

Advantages:

- Automatic translation
- Efficient for medium-sized networks

---

## 3. PAT (Port Address Translation)

Also called **NAT Overload**.

Multiple private IP addresses share a single public IP using different port numbers.

Example:

```
192.168.1.10

↓

203.0.113.10:5001

192.168.1.20

↓

203.0.113.10:5002
```

PAT is the most commonly used type of NAT in home and enterprise networks.

---

# 🌍 Inside Local vs Inside Global

| Term | Description |
|------|-------------|
| Inside Local | Private IP address inside the local network |
| Inside Global | Public IP address seen on the Internet |
| Outside Local | External address as seen from the internal network |
| Outside Global | Actual public IP address of the external host |

Example:

| Device | Address |
|---------|---------|
| PC | 192.168.1.10 (Inside Local) |
| Router | 203.0.113.10 (Inside Global) |

---

# 🔄 NAT Translation Process

```
Private Host

↓

Router

↓

Translate Private IP

↓

Replace Source Address

↓

Send Packet

↓

Internet

↓

Reply Returns

↓

Reverse Translation

↓

Private Host
```

---

# 🛠 Basic Cisco NAT Configuration

Configure the inside interface:

```bash
interface GigabitEthernet0/0
ip nat inside
```

Configure the outside interface:

```bash
interface GigabitEthernet0/1
ip nat outside
```

Configure PAT (NAT Overload):

```bash
access-list 1 permit 192.168.1.0 0.0.0.255

ip nat inside source list 1 interface GigabitEthernet0/1 overload
```

---

# 📋 Common NAT Commands

Display NAT translations:

```bash
show ip nat translations
```

Display NAT statistics:

```bash
show ip nat statistics
```

Display the routing table:

```bash
show ip route
```

Display interface status:

```bash
show ip interface brief
```

---

# 🔍 NAT Troubleshooting

### Verify Interface Configuration

```bash
show ip interface brief
```

---

### Verify NAT Translation

```bash
show ip nat translations
```

---

### Verify NAT Statistics

```bash
show ip nat statistics
```

---

### Verify Routing

```bash
show ip route
```

---

### Test Internet Connectivity

```bash
ping 8.8.8.8
```

---

# 💻 Practical Lab

## Task 1

Open Cisco Packet Tracer.

Add:

- 1 Router
- 1 Switch
- 2 PCs
- 1 Cloud (Internet)

---

## Task 2

Assign private IP addresses.

Example:

```
PC1

192.168.1.10

PC2

192.168.1.20
```

---

## Task 3

Configure PAT (NAT Overload) on the router.

---

## Task 4

Verify NAT translations.

```bash
show ip nat translations
```

---

## Task 5

Ping an external IP address.

Example:

```bash
ping 8.8.8.8
```

Observe the NAT translation table.

---

# 💡 Best Practices

- Use PAT for Internet access in most environments.
- Reserve Static NAT for public-facing servers.
- Monitor NAT translation tables regularly.
- Document NAT configurations.
- Verify routing before troubleshooting NAT.

---

# ⚠️ Common Mistakes

❌ Forgetting to configure inside and outside interfaces.

❌ Missing access-list for NAT.

❌ Incorrect default route.

❌ Using the wrong interface for PAT.

❌ Ignoring routing table verification.

---

# 🎯 Interview Questions

1. What is NAT?
2. Why is NAT used?
3. What is the difference between Static NAT and Dynamic NAT?
4. What is PAT?
5. What is NAT Overload?
6. What is the difference between Inside Local and Inside Global addresses?
7. Which command displays NAT translations?
8. Why is NAT important for IPv4?
9. Can multiple devices share one public IP address?
10. How would you troubleshoot a NAT issue?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- RFC 3022 (Traditional NAT)
- CompTIA Network+

---

## 🔗 Related Documents

- [Networking README](README.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [Routing](Routing.md)
- [DHCP](DHCP.md)
- [Network Troubleshooting](Network-Troubleshooting.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
