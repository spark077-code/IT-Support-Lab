# 🌐 OSI Model

> A beginner-friendly guide to understanding the Open Systems Interconnection (OSI) Model for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains the OSI (Open Systems Interconnection) Model, its seven layers, their functions, protocols, devices, and real-world examples.

---

# 📚 Table of Contents

1. What is the OSI Model?
2. Why is the OSI Model Important?
3. The Seven Layers
4. Data Flow
5. Devices at Each Layer
6. Protocols at Each Layer
7. Encapsulation & Decapsulation
8. Real-World Example
9. Mnemonics
10. Practical Lab
11. Best Practices
12. Common Mistakes
13. Interview Questions

---

# 🧠 What is the OSI Model?

The Open Systems Interconnection (OSI) Model is a conceptual framework that explains how data travels from one device to another across a network.

It divides network communication into seven logical layers.

Each layer performs a specific function and communicates with the layers directly above and below it.

---

# 🎯 Why is the OSI Model Important?

The OSI Model helps us:

- Understand how networks operate
- Troubleshoot network issues
- Learn networking in a structured way
- Understand communication between devices
- Identify where problems occur

---

# 🏗 The Seven Layers

| Layer | Name | Main Function |
|--------|----------------|-----------------------------|
| 7 | Application | Provides network services to applications |
| 6 | Presentation | Data translation and encryption |
| 5 | Session | Establishes and manages sessions |
| 4 | Transport | Reliable data delivery |
| 3 | Network | Routing and logical addressing |
| 2 | Data Link | Physical addressing and error detection |
| 1 | Physical | Transmission of bits over media |

---

# 📄 Layer 7 – Application

### Purpose

Provides network services directly to end-user applications.

### Common Protocols

- HTTP
- HTTPS
- FTP
- SMTP
- DNS

### Examples

- Google Chrome
- Microsoft Outlook
- Mozilla Firefox

---

# 📄 Layer 6 – Presentation

### Purpose

- Data formatting
- Encryption
- Compression
- Character encoding

### Examples

- SSL/TLS
- JPEG
- PNG
- MP4

---

# 📄 Layer 5 – Session

### Purpose

Creates, manages, and terminates communication sessions.

### Examples

- NetBIOS
- RPC

---

# 📄 Layer 4 – Transport

### Purpose

Provides reliable or fast end-to-end communication.

### Protocols

- TCP
- UDP

### Functions

- Segmentation
- Error recovery
- Flow control
- Reliability

---

# 📄 Layer 3 – Network

### Purpose

Moves packets between different networks.

### Protocols

- IP
- ICMP

### Devices

- Router
- Layer 3 Switch

---

# 📄 Layer 2 – Data Link

### Purpose

Transfers frames between devices on the same network.

### Functions

- MAC Addressing
- Error Detection
- Switching

### Devices

- Switch
- Bridge

---

# 📄 Layer 1 – Physical

### Purpose

Transmits raw binary data through physical media.

### Examples

- Ethernet Cable
- Fiber Optic Cable
- Wireless Signals
- Network Interface Card (NIC)

### Devices

- Hub
- Repeater
- Cables

---

# 📦 Data Flow

When sending data:

```text
Application
     ↓
Presentation
     ↓
Session
     ↓
Transport
     ↓
Network
     ↓
Data Link
     ↓
Physical
```

When receiving data:

```text
Physical
     ↑
Data Link
     ↑
Network
     ↑
Transport
     ↑
Session
     ↑
Presentation
     ↑
Application
```

---

# 🌍 Encapsulation

When data is sent:

```
Data
↓
Segment
↓
Packet
↓
Frame
↓
Bits
```

---

# 📥 Decapsulation

When data is received:

```
Bits
↑
Frame
↑
Packet
↑
Segment
↑
Data
```

---

# 🖥 Network Devices by Layer

| Device | OSI Layer |
|----------|-----------|
| Hub | Layer 1 |
| Repeater | Layer 1 |
| Switch | Layer 2 |
| Bridge | Layer 2 |
| Router | Layer 3 |
| Firewall | Layer 3 / 4 / 7 (depends on type) |

---

# 🌐 Common Protocols by Layer

| Layer | Protocols |
|---------|------------------------|
| Application | HTTP, HTTPS, FTP, SMTP, DNS |
| Presentation | SSL, TLS |
| Session | NetBIOS, RPC |
| Transport | TCP, UDP |
| Network | IP, ICMP |
| Data Link | Ethernet |
| Physical | Ethernet Cable, Fiber |

---

# 🌎 Real-World Example

When you open **https://www.google.com**:

1. Application → Browser sends an HTTPS request.
2. Presentation → Data is encrypted using TLS.
3. Session → A communication session is established.
4. Transport → TCP ensures reliable delivery.
5. Network → IP routes the packet.
6. Data Link → The frame is delivered using MAC addresses.
7. Physical → Bits travel through the network cable or Wi-Fi.

---

# 🧠 Easy Mnemonics

Top → Bottom

```
All
People
Seem
To
Need
Data
Processing
```

Bottom → Top

```
Please
Do
Not
Throw
Sausage
Pizza
Away
```

---

# 💻 Practical Lab

## Task 1

Open Cisco Packet Tracer.

Identify:

- PC
- Switch
- Router

Determine which OSI layer each device primarily operates on.

---

## Task 2

Run the following command on Linux:

```bash
ping 8.8.8.8
```

Think about which OSI layers are involved.

---

## Task 3

Open a website in your browser.

Identify the protocols used at each OSI layer.

---

# 💡 Best Practices

- Learn the function of each layer instead of memorizing only the names.
- Associate protocols with their respective layers.
- Understand how data is encapsulated and decapsulated.
- Use the OSI model during network troubleshooting.

---

# ⚠ Common Mistakes

❌ Confusing the OSI Model with the TCP/IP Model.

❌ Thinking every device operates at only one layer.

❌ Memorizing layer names without understanding their functions.

❌ Forgetting the order of the layers.


---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- CompTIA Network+
- RFC Documentation

---

## 🔗 Related Documents

- [Networking README](README.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [Subnetting](Subnetting.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
