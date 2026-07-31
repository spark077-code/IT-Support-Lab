# 🌐 Dynamic Host Configuration Protocol (DHCP)

> A beginner-friendly guide to understanding Dynamic Host Configuration Protocol (DHCP), IP address assignment, the DORA process, troubleshooting, and practical networking examples.

---

# 📌 Objective

This document explains how DHCP automatically assigns IP addresses to devices, how the DHCP process works, common DHCP concepts, troubleshooting techniques, and essential commands for Networking, IT Support, and Cyber Security.

---

# 📚 Table of Contents

1. What is DHCP?
2. Why is DHCP Important?
3. How DHCP Works
4. The DORA Process
5. DHCP Components
6. DHCP Lease
7. DHCP Reservation
8. DHCP Relay
9. Common DHCP Commands
10. DHCP Troubleshooting
11. Practical Lab
12. Best Practices
13. Common Mistakes
14. Interview Questions

---

# 🧠 What is DHCP?

DHCP (Dynamic Host Configuration Protocol) is a network protocol that automatically assigns IP addresses and other network settings to devices.

Instead of manually configuring every device, DHCP performs the configuration automatically.

---

# 🎯 Why is DHCP Important?

DHCP provides several benefits:

- Automatically assigns IP addresses
- Prevents duplicate IP addresses
- Saves administration time
- Simplifies network management
- Reduces configuration errors

Without DHCP, every device would require manual IP configuration.

---

# ⚙️ How DHCP Works

When a new device connects to a network:

```
Client

↓

DHCP Server

↓

IP Address Assigned
```

The DHCP server provides:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server
- Lease Time

---

# 🔄 The DORA Process

DHCP follows a four-step process known as **DORA**.

```
Client

↓

Discover

↓

Offer

↓

Request

↓

Acknowledge (ACK)
```

### 1. Discover

The client broadcasts a request to locate a DHCP server.

---

### 2. Offer

The DHCP server offers an available IP address.

---

### 3. Request

The client requests the offered IP address.

---

### 4. Acknowledge (ACK)

The DHCP server confirms the assignment and sends the configuration.

---

# 🖥 DHCP Components

| Component | Purpose |
|------------|-----------------------------|
| DHCP Client | Requests an IP address |
| DHCP Server | Assigns IP addresses |
| DHCP Scope | Range of available IP addresses |
| Lease | Time the IP address is assigned |
| Reservation | Permanent IP assignment for a specific device |

---

# ⏳ DHCP Lease

A lease defines how long a device can use an assigned IP address.

Example:

```
Lease Time

24 Hours
```

When the lease expires, the client attempts to renew it automatically.

---

# 📌 DHCP Reservation

A DHCP Reservation ensures that a specific device always receives the same IP address.

Reservations are commonly used for:

- Printers
- Servers
- Network Cameras
- IP Phones

The reservation is based on the device's **MAC Address**.

---

# 🌐 DHCP Relay

A DHCP Relay forwards DHCP requests between different networks when the DHCP server is located on another subnet.

Without a relay, DHCP broadcasts cannot cross routers.

Example:

```
PC

↓

Switch

↓

Router (DHCP Relay)

↓

DHCP Server
```

---

# 🛠 Common DHCP Commands

## Linux

Release the current lease:

```bash
sudo dhclient -r
```

Request a new lease:

```bash
sudo dhclient
```

View IP Address:

```bash
ip a
```

View Routing Table:

```bash
ip route
```

---

## Windows

Display IP Configuration:

```cmd
ipconfig /all
```

Release IP Address:

```cmd
ipconfig /release
```

Request New IP Address:

```cmd
ipconfig /renew
```

Display Routing Table:

```cmd
route print
```

---

# 🔍 DHCP Troubleshooting

### Check the Assigned IP Address

Linux:

```bash
ip a
```

Windows:

```cmd
ipconfig
```

---

### Look for an APIPA Address

If you see an address like:

```
169.254.x.x
```

it usually indicates that the device could not contact a DHCP server.

---

### Verify Network Connectivity

```bash
ping 8.8.8.8
```

---

### Verify the Default Gateway

Linux:

```bash
ip route
```

Windows:

```cmd
ipconfig /all
```

---

### Renew the DHCP Lease

Windows:

```cmd
ipconfig /renew
```

Linux:

```bash
sudo dhclient
```

---

# 💻 Practical Lab

## Task 1

Open Cisco Packet Tracer.

Add:

- 1 Router
- 1 Switch
- 3 PCs

---

## Task 2

Configure the router as a DHCP Server.

---

## Task 3

Create a DHCP Pool.

Example:

```
Network

192.168.10.0/24

Default Gateway

192.168.10.1

DNS

8.8.8.8
```

---

## Task 4

Configure each PC to obtain an IP address automatically (DHCP).

---

## Task 5

Verify that each PC receives:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

---

## Task 6

Test connectivity.

```bash
ping
```

Verify successful communication between devices.

---

# 💡 Best Practices

- Use DHCP for end-user devices.
- Reserve static IPs for servers and network infrastructure.
- Create appropriate DHCP scopes.
- Monitor DHCP lease utilization.
- Document DHCP configurations.

---

# ⚠️ Common Mistakes

❌ Creating overlapping DHCP scopes.

❌ Forgetting to configure the default gateway.

❌ Not configuring DNS server addresses.

❌ Using static IP addresses inside the DHCP pool.

❌ Ignoring DHCP lease expiration.

---

# 🎯 Interview Questions

1. What is DHCP?
2. Why is DHCP used?
3. What does DORA stand for?
4. What is a DHCP Lease?
5. What is a DHCP Scope?
6. What is a DHCP Reservation?
7. What is an APIPA address?
8. Why is DHCP Relay required?
9. Which command renews a DHCP lease in Windows?
10. How would you troubleshoot a DHCP issue?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- RFC 2131 (DHCP)
- RFC 2132 (DHCP Options)
- CompTIA Network+

---

## 🔗 Related Documents

- [Networking README](README.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [DNS](DNS.md)
- [Routing](Routing.md)
- [Network Troubleshooting](Network-Troubleshooting.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
