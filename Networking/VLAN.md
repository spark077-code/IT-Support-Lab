# 🖧 Virtual LAN (VLAN)

> A beginner-friendly guide to understanding Virtual LANs (VLANs), their purpose, configuration concepts, and troubleshooting for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains what VLANs are, why they are used, how they work, common VLAN types, trunking concepts, and basic configuration examples.

---

# 📚 Table of Contents

1. What is a VLAN?
2. Why Use VLANs?
3. How VLANs Work
4. VLAN Types
5. Access Port vs Trunk Port
6. Native VLAN
7. Inter-VLAN Communication
8. VLAN Configuration Example
9. Practical Lab
10. Best Practices
11. Common Mistakes
12. Interview Questions

---

# 🧠 What is a VLAN?

A Virtual Local Area Network (VLAN) is a logical division of a physical network.

Instead of placing all devices in one broadcast domain, VLANs divide a switch into multiple separate broadcast domains.

Devices in different VLANs cannot communicate directly without a Layer 3 device (Router or Layer 3 Switch).

---

# 🎯 Why Use VLANs?

VLANs provide several benefits:

- Improve network security
- Reduce broadcast traffic
- Better network organization
- Easier network management
- Improved performance
- Separate departments without additional switches

Example:

```
Company Network

HR Department
     │
   VLAN 10

Finance Department
     │
   VLAN 20

IT Department
     │
   VLAN 30
```

---

# ⚙️ How VLANs Work

Each switch port can be assigned to a VLAN.

Example:

| Port | VLAN |
|------|------|
| Fa0/1 | VLAN 10 |
| Fa0/2 | VLAN 10 |
| Fa0/3 | VLAN 20 |
| Fa0/4 | VLAN 30 |

Devices connected to the same VLAN can communicate directly.

Devices in different VLANs require routing.

---

# 📂 VLAN Types

| VLAN Type | Purpose |
|------------|------------------------------|
| Default VLAN | VLAN 1 (exists by default) |
| Data VLAN | Carries user traffic |
| Management VLAN | Used for switch management |
| Voice VLAN | Used for IP Phones |
| Native VLAN | Carries untagged traffic |

---

# 🔌 Access Port

An Access Port belongs to only one VLAN.

Example:

```
PC
 │
Access Port
 │
Switch
```

Cisco Configuration

```bash
interface FastEthernet0/1

switchport mode access

switchport access vlan 10
```

---

# 🌐 Trunk Port

A Trunk Port carries traffic for multiple VLANs.

It is commonly used between:

- Switch ↔ Switch
- Switch ↔ Router
- Switch ↔ Layer 3 Switch

Example:

```
Switch -------- Switch

      Trunk Link
```

Cisco Configuration

```bash
interface GigabitEthernet0/1

switchport mode trunk
```

---

# 🏷 Native VLAN

The Native VLAN carries untagged traffic on a trunk link.

Default Native VLAN:

```
VLAN 1
```

It is recommended to change the default native VLAN for better security.

---

# 🔀 Inter-VLAN Communication

Devices in different VLANs cannot communicate directly.

A Layer 3 device is required.

Options:

- Router-on-a-Stick
- Layer 3 Switch

Example:

```
PC (VLAN10)

↓

Switch

↓

Router

↓

Switch

↓

PC (VLAN20)
```

---

# 💻 Basic VLAN Configuration

Create VLANs

```bash
enable

configure terminal

vlan 10

name HR

vlan 20

name Finance

vlan 30

name IT
```

Assign Port to VLAN

```bash
interface FastEthernet0/1

switchport mode access

switchport access vlan 10
```

Display VLAN Information

```bash
show vlan brief
```

Display Trunk Information

```bash
show interfaces trunk
```

---

# 🧪 Practical Lab

## Task 1

Open Cisco Packet Tracer.

Add:

- 1 Switch
- 3 PCs

---

## Task 2

Create VLANs:

- VLAN 10
- VLAN 20
- VLAN 30

---

## Task 3

Assign:

| PC | VLAN |
|----|------|
| PC1 | VLAN 10 |
| PC2 | VLAN 20 |
| PC3 | VLAN 30 |

---

## Task 4

Assign IP Addresses

Example:

```
PC1

192.168.10.10/24

PC2

192.168.20.10/24

PC3

192.168.30.10/24
```

---

## Task 5

Verify VLANs

```bash
show vlan brief
```

---

## Task 6

Test connectivity using:

```bash
ping
```

Observe that devices in different VLANs cannot communicate until Inter-VLAN Routing is configured.

---

# 💡 Best Practices

- Use descriptive VLAN names.
- Create separate VLANs for different departments.
- Avoid using VLAN 1 for user devices.
- Document VLAN assignments.
- Restrict unused switch ports.

---

# ⚠️ Common Mistakes

❌ Forgetting to assign ports to the correct VLAN.

❌ Configuring both ends of a trunk incorrectly.

❌ Leaving all devices in VLAN 1.

❌ Forgetting that different VLANs require Layer 3 routing.

---

# 🎯 Interview Questions

1. What is a VLAN?
2. Why are VLANs used?
3. What is the default VLAN?
4. What is the difference between an Access Port and a Trunk Port?
5. What is a Native VLAN?
6. Can devices in different VLANs communicate directly?
7. What device is required for Inter-VLAN Routing?
8. What command displays VLAN information?
9. What command displays trunk information?
10. What are the benefits of VLANs?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- IEEE 802.1Q Standard
- CompTIA Network+

---

## 🔗 Related Documents

- [Networking README](README.md)
- [OSI Model](OSI-Model.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [Subnetting](Subnetting.md)
- [Switching](Switching.md)
- [Routing](Routing.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
