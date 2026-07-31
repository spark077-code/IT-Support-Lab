# 🔀 Network Switching

> A beginner-friendly guide to understanding network switching, MAC addresses, frame forwarding, and Layer 2 switching for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains how network switches operate, how frames are forwarded, how MAC address tables work, and introduces essential Layer 2 concepts used in modern networks.

---

# 📚 Table of Contents

1. What is a Switch?
2. Why Use a Switch?
3. How a Switch Works
4. MAC Address Table
5. Frame Forwarding
6. Collision Domain vs Broadcast Domain
7. Types of Traffic
8. Spanning Tree Protocol (STP)
9. Port Security
10. Common Switch Commands
11. Practical Lab
12. Best Practices
13. Common Mistakes
14. Interview Questions

---

# 🧠 What is a Switch?

A network switch is a Layer 2 networking device that connects multiple devices within a Local Area Network (LAN).

Unlike a hub, a switch intelligently forwards data only to the intended destination using MAC addresses.

---

# 🎯 Why Use a Switch?

Switches provide several advantages:

- Faster communication
- Reduced collisions
- Better bandwidth utilization
- Improved network performance
- Supports VLANs
- Enhanced security with features like Port Security

---

# ⚙️ How a Switch Works

When a frame arrives at a switch:

1. The switch learns the source MAC address.
2. It stores the MAC address in its MAC Address Table.
3. It checks the destination MAC address.
4. If known, the frame is forwarded to the correct port.
5. If unknown, the frame is flooded to all ports except the incoming port.

---

# 📋 MAC Address Table

A switch maintains a table of learned MAC addresses.

Example:

| MAC Address | Port |
|-------------|------|
| AA:AA:AA:AA:AA:01 | Fa0/1 |
| BB:BB:BB:BB:BB:02 | Fa0/2 |
| CC:CC:CC:CC:CC:03 | Fa0/3 |

View the MAC address table:

```bash
show mac address-table
```

---

# 📦 Frame Forwarding

Switches forward Ethernet frames based on the destination MAC address.

Types of forwarding:

- Known Unicast
- Unknown Unicast
- Broadcast
- Multicast

---

# 🌐 Collision Domain vs Broadcast Domain

| Feature | Collision Domain | Broadcast Domain |
|---------|------------------|------------------|
| Controlled By | Switch Port | Router or VLAN |
| Purpose | Prevents data collisions | Limits broadcast traffic |

Each switch port creates its own collision domain.

A VLAN creates a separate broadcast domain.

---

# 📡 Types of Network Traffic

## Unicast

Communication between one sender and one receiver.

Example:

```
PC1 → PC2
```

---

## Broadcast

Communication from one device to all devices in the same broadcast domain.

Example:

```
ARP Request
```

---

## Multicast

Communication from one sender to a selected group of receivers.

Example:

```
Video Streaming
```

---

# 🌳 Spanning Tree Protocol (STP)

STP prevents Layer 2 loops by blocking redundant paths.

Benefits:

- Prevents broadcast storms
- Prevents switching loops
- Provides network redundancy

Common STP States:

- Blocking
- Listening
- Learning
- Forwarding
- Disabled

---

# 🔒 Port Security

Port Security restricts which devices can connect to a switch port.

Example Configuration:

```bash
interface FastEthernet0/1

switchport mode access

switchport port-security

switchport port-security maximum 1

switchport port-security violation shutdown

switchport port-security mac-address sticky
```

Verify Port Security:

```bash
show port-security
```

---

# 🛠 Common Switch Commands

Display VLANs:

```bash
show vlan brief
```

Display MAC Address Table:

```bash
show mac address-table
```

Display Interface Status:

```bash
show interfaces status
```

Display Running Configuration:

```bash
show running-config
```

Display Port Security:

```bash
show port-security
```

Display STP Information:

```bash
show spanning-tree
```

---

# 💻 Practical Lab

## Task 1

Open Cisco Packet Tracer.

Add:

- 1 Switch
- 4 PCs

---

## Task 2

Assign IP addresses to all PCs.

Example:

```
192.168.1.10
192.168.1.11
192.168.1.12
192.168.1.13
```

---

## Task 3

Connect all PCs to the switch using Copper Straight-Through cables.

---

## Task 4

Ping between all devices.

Verify connectivity.

---

## Task 5

Display the MAC Address Table.

```bash
show mac address-table
```

Observe how the switch learns MAC addresses automatically.

---

## Task 6

Enable Port Security on one interface.

Verify the configuration:

```bash
show port-security
```

---

# 💡 Best Practices

- Enable Port Security on access ports.
- Disable unused switch ports.
- Use descriptive interface descriptions.
- Document VLAN assignments.
- Monitor the MAC Address Table regularly.
- Keep switch firmware updated.

---

# ⚠️ Common Mistakes

❌ Connecting switches in a loop without STP.

❌ Leaving unused ports enabled.

❌ Forgetting to save the configuration.

❌ Assuming hubs and switches work the same way.

❌ Ignoring Port Security.

---

# 🎯 Interview Questions

1. What is a network switch?
2. At which OSI layer does a switch operate?
3. What is a MAC Address Table?
4. How does a switch forward frames?
5. What is the difference between a hub and a switch?
6. What is a collision domain?
7. What is a broadcast domain?
8. What is Spanning Tree Protocol (STP)?
9. What is Port Security?
10. Which command displays the MAC Address Table?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- IEEE 802.1D (Spanning Tree Protocol)
- IEEE 802.1Q (VLAN)
- CompTIA Network+

---

## 🔗 Related Documents

- [Networking README](README.md)
- [OSI Model](OSI-Model.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [Subnetting](Subnetting.md)
- [VLAN](VLAN.md)
- [Routing](Routing.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
