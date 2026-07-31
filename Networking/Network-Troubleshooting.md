# 🛠️ Network Troubleshooting

> A beginner-friendly guide to troubleshooting common network issues using a structured approach, essential commands, and real-world scenarios for Networking, IT Support, and Cyber Security.

---

# 📌 Objective

This document explains a step-by-step methodology for diagnosing and resolving common network problems. It covers troubleshooting techniques, useful commands, and practical scenarios for Windows, Linux, and Cisco devices.

---

# 📚 Table of Contents

1. What is Network Troubleshooting?
2. Troubleshooting Methodology
3. OSI Model Approach
4. Common Network Issues
5. Essential Troubleshooting Commands
6. Windows Commands
7. Linux Commands
8. Cisco IOS Commands
9. Real-World Scenarios
10. Best Practices
11. Common Mistakes
12. Interview Questions

---

# 🧠 What is Network Troubleshooting?

Network troubleshooting is the process of identifying, diagnosing, and resolving network-related problems.

The goal is to restore normal network communication as quickly as possible.

---

# 🎯 Troubleshooting Methodology

A structured troubleshooting process helps solve problems efficiently.

### Step 1

Identify the problem.

Questions to ask:

- What is not working?
- When did the issue start?
- Is only one device affected?
- Are multiple users affected?

---

### Step 2

Gather information.

Check:

- IP Address
- Gateway
- DNS Server
- Network cable
- Wi-Fi connection

---

### Step 3

Identify the probable cause.

Possible causes include:

- Incorrect IP address
- DHCP failure
- DNS failure
- Gateway issue
- Cable problem
- Switch port disabled
- Routing issue

---

### Step 4

Test the solution.

Verify that the issue has been resolved.

---

### Step 5

Document the solution.

Record:

- Root cause
- Resolution
- Commands used
- Preventive measures

---

# 📚 OSI Model Troubleshooting

| Layer | What to Check |
|---------|---------------|
| Layer 1 | Cable, Power, NIC, Link LEDs |
| Layer 2 | Switch, VLAN, MAC Address |
| Layer 3 | IP Address, Gateway, Routing |
| Layer 4 | TCP/UDP Ports |
| Layer 5-7 | Applications, DNS, Browser, Services |

---

# 🚨 Common Network Issues

## No Internet Connection

Possible causes:

- Cable disconnected
- Wi-Fi disconnected
- Wrong Gateway
- DNS failure
- ISP outage

Check:

```bash
ping 8.8.8.8
```

---

## Incorrect IP Address

Verify:

Windows

```cmd
ipconfig
```

Linux

```bash
ip a
```

---

## IP Address Conflict

Symptoms:

- Network disconnects
- Duplicate IP warning

Solution:

- Use DHCP
- Assign a unique static IP

---

## APIPA Address

Example:

```
169.254.x.x
```

Meaning:

The device could not obtain an IP address from the DHCP server.

---

## DNS Failure

Symptoms:

```
Google.com doesn't open

↓

8.8.8.8 responds
```

Check:

```bash
nslookup google.com
```

---

## Default Gateway Issue

Verify:

Windows

```cmd
ipconfig /all
```

Linux

```bash
ip route
```

---

## VLAN Connectivity Issue

Check:

```bash
show vlan brief
```

Verify:

- Correct VLAN
- Access Port
- Trunk Port

---

## Routing Issue

Check:

```bash
show ip route
```

Linux:

```bash
ip route
```

---

## NAT Issue

Verify:

```bash
show ip nat translations
```

---

## ACL Issue

Verify:

```bash
show access-lists
```

---

# 🛠 Essential Troubleshooting Commands

## Ping

Tests network connectivity.

```bash
ping 8.8.8.8
```

---

## Traceroute

Shows the path packets take.

Linux

```bash
traceroute google.com
```

Windows

```cmd
tracert google.com
```

---

## nslookup

Tests DNS resolution.

```bash
nslookup google.com
```

---

## dig

Detailed DNS lookup.

```bash
dig google.com
```

---

# 🪟 Windows Commands

Display IP configuration

```cmd
ipconfig /all
```

Renew IP address

```cmd
ipconfig /renew
```

Flush DNS cache

```cmd
ipconfig /flushdns
```

Display routing table

```cmd
route print
```

View ARP table

```cmd
arp -a
```

---

# 🐧 Linux Commands

Display IP address

```bash
ip a
```

Display routing table

```bash
ip route
```

Display neighbor table

```bash
ip neigh
```

Display DNS configuration

```bash
cat /etc/resolv.conf
```

Restart NetworkManager

```bash
sudo systemctl restart NetworkManager
```

---

# 🌐 Cisco IOS Commands

Show interfaces

```bash
show ip interface brief
```

Show routing table

```bash
show ip route
```

Show VLANs

```bash
show vlan brief
```

Show MAC address table

```bash
show mac address-table
```

Show NAT translations

```bash
show ip nat translations
```

Show ACLs

```bash
show access-lists
```

Show running configuration

```bash
show running-config
```

---

# 💻 Real-World Scenarios

## Scenario 1

A user cannot access the Internet.

Steps:

1. Check physical connection.
2. Verify IP address.
3. Ping the default gateway.
4. Ping 8.8.8.8.
5. Test DNS using `nslookup`.
6. Verify browser access.

---

## Scenario 2

Two PCs cannot communicate.

Check:

- Same subnet
- Correct subnet mask
- VLAN assignment
- Switch port status
- Firewall rules

---

## Scenario 3

A website opens by IP address but not by domain name.

Likely cause:

DNS configuration issue.

Check:

```bash
nslookup
```

---

## Scenario 4

A PC receives a 169.254.x.x address.

Likely cause:

DHCP server unavailable.

Check:

- DHCP server status
- Switch connectivity
- DHCP relay
- Renew the DHCP lease

---

# 💡 Best Practices

- Follow a structured troubleshooting process.
- Start with simple checks before advanced diagnostics.
- Keep network documentation updated.
- Save device configurations after successful changes.
- Verify every change before moving to the next step.

---

# ⚠️ Common Mistakes

❌ Skipping Layer 1 checks.

❌ Assuming DNS is always the problem.

❌ Ignoring routing tables.

❌ Forgetting to save Cisco configurations.

❌ Changing multiple settings at the same time.

---

# 🎯 Interview Questions

1. What is network troubleshooting?
2. What is the first step in troubleshooting?
3. What does a 169.254.x.x IP address indicate?
4. Which command checks DNS resolution?
5. Which command displays the routing table?
6. How do you verify VLAN configuration?
7. What is the purpose of `ping`?
8. What is the purpose of `traceroute`?
9. How would you troubleshoot a user who cannot access the Internet?
10. Why is documentation important after troubleshooting?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- CompTIA Network+
- Microsoft Networking Documentation
- Linux Network Administration Guide

---

## 🔗 Related Documents

- [README](README.md)
- [OSI Model](OSI-Model.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [Subnetting](Subnetting.md)
- [VLAN](VLAN.md)
- [Switching](Switching.md)
- [Routing](Routing.md)
- [DNS](DNS.md)
- [DHCP](DHCP.md)
- [NAT](NAT.md)
- [ACL](ACL.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
