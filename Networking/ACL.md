# 🔒 Access Control Lists (ACL)

> A beginner-friendly guide to understanding Access Control Lists (ACLs), their types, configuration concepts, and troubleshooting for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains what ACLs are, why they are used, the different types of ACLs, wildcard masks, inbound and outbound filtering, basic Cisco configuration examples, and troubleshooting techniques.

---

# 📚 Table of Contents

1. What is an ACL?
2. Why Use ACLs?
3. How ACLs Work
4. Types of ACLs
5. Numbered vs Named ACLs
6. Wildcard Masks
7. Inbound vs Outbound ACLs
8. Basic Cisco ACL Configuration
9. Common ACL Commands
10. ACL Troubleshooting
11. Practical Lab
12. Best Practices
13. Common Mistakes
14. Interview Questions

---

# 🧠 What is an ACL?

An Access Control List (ACL) is a set of rules that controls network traffic.

ACLs determine whether packets are allowed or denied based on criteria such as:

- Source IP Address
- Destination IP Address
- Protocol (TCP, UDP, ICMP)
- Port Number (Extended ACLs)

ACLs are commonly configured on routers and Layer 3 switches.

---

# 🎯 Why Use ACLs?

ACLs help to:

- Improve network security
- Restrict unauthorized access
- Control traffic flow
- Protect servers
- Reduce unnecessary network traffic

---

# ⚙️ How ACLs Work

When a packet reaches a router interface:

1. The router checks ACL rules from top to bottom.
2. The first matching rule is applied.
3. If no rule matches, the packet is denied by the **implicit deny** rule.

Example:

```
permit 192.168.1.0/24

↓

deny all others
```

---

# 📂 Types of ACLs

## Standard ACL

Filters traffic based only on the **source IP address**.

Example:

```
Permit 192.168.1.0/24
```

---

## Extended ACL

Filters traffic using:

- Source IP
- Destination IP
- Protocol
- Port Number

Example:

```
Allow HTTP

Source

192.168.1.0/24

↓

Destination

Web Server

↓

Port 80
```

---

# 🏷 Numbered vs Named ACLs

## Numbered ACL

Uses numbers.

Examples:

```
1–99

1300–1999
```

---

## Named ACL

Uses descriptive names.

Example:

```
WEB_ACCESS
```

Named ACLs are easier to manage and modify.

---

# 🎭 Wildcard Masks

A wildcard mask tells Cisco IOS which bits to ignore when matching IP addresses.

Example:

```
Subnet Mask

255.255.255.0
```

Wildcard Mask:

```
0.0.0.255
```

Examples:

| Subnet Mask | Wildcard Mask |
|--------------|---------------|
| 255.255.255.0 | 0.0.0.255 |
| 255.255.255.128 | 0.0.0.127 |
| 255.255.255.192 | 0.0.0.63 |
| 255.255.255.224 | 0.0.0.31 |

---

# 🔄 Inbound vs Outbound ACLs

## Inbound ACL

Filters traffic as it enters an interface.

```
Incoming Packet

↓

ACL Check

↓

Router
```

---

## Outbound ACL

Filters traffic before it leaves an interface.

```
Router

↓

ACL Check

↓

Outgoing Packet
```

---

# 🛠 Basic Cisco ACL Configuration

## Standard ACL

```bash
access-list 10 permit 192.168.1.0 0.0.0.255
```

Apply to an interface:

```bash
interface GigabitEthernet0/0

ip access-group 10 in
```

---

## Extended ACL

```bash
access-list 100 permit tcp 192.168.1.0 0.0.0.255 any eq 80
```

Apply to an interface:

```bash
interface GigabitEthernet0/1

ip access-group 100 out
```

---

## Named ACL

```bash
ip access-list extended WEB_ACCESS

permit tcp any any eq 80

deny ip any any
```

---

# 📋 Common ACL Commands

Display ACLs:

```bash
show access-lists
```

Display Interface Configuration:

```bash
show running-config
```

Display Interface Status:

```bash
show ip interface
```

---

# 🔍 ACL Troubleshooting

### Verify ACL Configuration

```bash
show access-lists
```

---

### Verify ACL Placement

```bash
show running-config
```

---

### Check Interface Assignment

```bash
show ip interface
```

---

### Test Connectivity

```bash
ping
```

or

```bash
traceroute
```

---

### Review Rule Order

Remember:

```
ACLs are processed from top to bottom.

First match wins.
```

---

# 💻 Practical Lab

## Task 1

Open Cisco Packet Tracer.

Add:

- 2 Routers
- 2 Switches
- 4 PCs

---

## Task 2

Configure IP addresses and verify connectivity.

---

## Task 3

Create a Standard ACL to allow only the `192.168.1.0/24` network.

---

## Task 4

Apply the ACL to the appropriate router interface.

---

## Task 5

Test connectivity using:

```bash
ping
```

Verify that permitted traffic succeeds and denied traffic is blocked.

---

## Task 6

Create an Extended ACL to allow only HTTP traffic (TCP port 80) from a specific network.

Verify the behavior.

---

# 💡 Best Practices

- Use descriptive names for Named ACLs.
- Place Standard ACLs close to the destination.
- Place Extended ACLs close to the source.
- Document ACL rules.
- Review ACLs regularly.
- Remove unused ACL entries.

---

# ⚠️ Common Mistakes

❌ Forgetting the implicit deny rule.

❌ Applying an ACL to the wrong interface.

❌ Applying the ACL in the wrong direction (in/out).

❌ Incorrect wildcard mask.

❌ Incorrect rule order.

---

# 🎯 Interview Questions

1. What is an ACL?
2. Why are ACLs used?
3. What is the difference between Standard and Extended ACLs?
4. What is a wildcard mask?
5. What is the difference between a subnet mask and a wildcard mask?
6. What is the implicit deny rule?
7. What is the difference between inbound and outbound ACLs?
8. What is the advantage of Named ACLs?
9. Which command displays configured ACLs?
10. Where should Standard and Extended ACLs be placed?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- Cisco IOS Security Configuration Guide
- CompTIA Network+

---

## 🔗 Related Documents

- [Networking README](README.md)
- [Routing](Routing.md)
- [NAT](NAT.md)
- [VLAN](VLAN.md)
- [Switching](Switching.md)
- [Network Troubleshooting](Network-Troubleshooting.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
