# 🛣️ Routing

> A beginner-friendly guide to understanding routing, routers, routing tables, and routing protocols for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains how routers forward packets between networks, how routing tables work, the difference between static and dynamic routing, and introduces common routing protocols.

---

# 📚 Table of Contents

1. What is Routing?
2. Why is Routing Important?
3. Router vs Switch
4. How Routing Works
5. Routing Table
6. Static Routing
7. Dynamic Routing
8. Routing Protocols
9. Default Route
10. Administrative Distance
11. Common Router Commands
12. Practical Lab
13. Best Practices
14. Common Mistakes
15. Interview Questions

---

# 🧠 What is Routing?

Routing is the process of forwarding packets from one network to another using a router.

Routers examine the destination IP address and decide the best path for the packet.

Example:

```
PC1
 │
Switch
 │
Router
 │
Switch
 │
PC2
```

Without routing, devices on different networks cannot communicate.

---

# 🎯 Why is Routing Important?

Routing helps to:

- Connect different networks
- Provide Internet access
- Select the best path for data
- Reduce unnecessary traffic
- Enable communication between VLANs

---

# 🔀 Router vs Switch

| Feature | Router | Switch |
|----------|---------|---------|
| OSI Layer | Layer 3 | Layer 2 |
| Uses | IP Address | MAC Address |
| Connects | Different Networks | Same Network |
| Routing | Yes | No (Basic Layer 2 Switch) |

---

# ⚙️ How Routing Works

When a router receives a packet:

1. Reads the destination IP address.
2. Checks its routing table.
3. Finds the best matching route.
4. Forwards the packet through the correct interface.

---

# 📋 Routing Table

A routing table contains all known routes.

Example:

```text
Destination        Gateway        Interface
192.168.10.0/24    Directly Connected   G0/0
192.168.20.0/24    192.168.1.2          G0/1
0.0.0.0/0          192.168.1.1          G0/1
```

View the routing table:

Cisco IOS

```bash
show ip route
```

Linux

```bash
ip route
```

Windows

```cmd
route print
```

---

# 📌 Static Routing

A Static Route is manually configured by the administrator.

Example:

```bash
ip route 192.168.20.0 255.255.255.0 192.168.1.2
```

Advantages:

- Simple
- Secure
- Predictable

Disadvantages:

- Manual configuration
- Difficult to manage in large networks

---

# 🔄 Dynamic Routing

Dynamic routing automatically learns and updates routes.

Advantages:

- Automatic updates
- Better scalability
- Easier management

Disadvantages:

- More CPU and memory usage
- More complex configuration

---

# 🌐 Common Routing Protocols

## RIP (Routing Information Protocol)

- Distance Vector
- Metric: Hop Count
- Maximum: 15 Hops

---

## OSPF (Open Shortest Path First)

- Link State
- Fast convergence
- Commonly used in enterprise networks

---

## EIGRP (Enhanced Interior Gateway Routing Protocol)

- Advanced Distance Vector
- Cisco proprietary (historically)
- Fast convergence

---

## BGP (Border Gateway Protocol)

- Used between Internet Service Providers (ISPs)
- Runs the Internet backbone

---

# 🚪 Default Route

A Default Route is used when no specific route exists.

Network:

```
0.0.0.0/0
```

Cisco Example:

```bash
ip route 0.0.0.0 0.0.0.0 192.168.1.1
```

---

# 📏 Administrative Distance

Administrative Distance (AD) determines the trustworthiness of a route.

| Route Type | AD |
|------------|---:|
| Connected | 0 |
| Static | 1 |
| EIGRP | 90 |
| OSPF | 110 |
| RIP | 120 |

Lower AD is preferred.

---

# 🛠 Common Router Commands

Display Routing Table

```bash
show ip route
```

Display Interface Status

```bash
show ip interface brief
```

Display Running Configuration

```bash
show running-config
```

Save Configuration

```bash
copy running-config startup-config
```

Display Connected Interfaces

```bash
show interfaces
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

Assign IP addresses to all devices.

Example:

Router 1

```
192.168.10.1/24
```

Router 2

```
192.168.20.1/24
```

---

## Task 3

Configure a static route.

Example:

```bash
ip route 192.168.20.0 255.255.255.0 10.0.0.2
```

---

## Task 4

Verify routing.

```bash
show ip route
```

---

## Task 5

Ping from PC1 to PC4.

```bash
ping 192.168.20.10
```

Verify successful communication.

---

# 💡 Best Practices

- Plan your IP addressing scheme before configuring routes.
- Use dynamic routing protocols for large networks.
- Document routing configurations.
- Verify routing tables after making changes.
- Save router configurations after successful testing.

---

# ⚠️ Common Mistakes

❌ Forgetting to configure a return route.

❌ Incorrect subnet mask in a static route.

❌ Wrong next-hop IP address.

❌ Forgetting to save the configuration.

❌ Ignoring routing table verification.

---

# 🎯 Interview Questions

1. What is routing?
2. What is the difference between a router and a switch?
3. What is a routing table?
4. What is a static route?
5. What is a dynamic route?
6. What is a default route?
7. What is Administrative Distance?
8. Which routing protocol uses hop count?
9. Which routing protocol is link-state?
10. Which command displays the routing table on a Cisco router?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- RFC 1812 (Requirements for IP Routers)
- CompTIA Network+

---

## 🔗 Related Documents

- [Networking README](README.md)
- [OSI Model](OSI-Model.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [Subnetting](Subnetting.md)
- [VLAN](VLAN.md)
- [Switching](Switching.md)
- [DHCP](DHCP.md)
- [NAT](NAT.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
