# 🧪 Cisco Packet Tracer Labs

> A collection of beginner-to-intermediate Cisco Packet Tracer labs designed to practice networking concepts for CCNA, IT Support, and Cyber Security.

---

# 📌 Objective

This document contains hands-on networking labs using Cisco Packet Tracer. These labs reinforce networking concepts through practical exercises and troubleshooting.

---

# 📚 Table of Contents

1. Lab 1 – Basic Network Connectivity
2. Lab 2 – Switch Configuration
3. Lab 3 – VLAN Configuration
4. Lab 4 – Inter-VLAN Routing
5. Lab 5 – Static Routing
6. Lab 6 – RIP Routing
7. Lab 7 – OSPF Routing
8. Lab 8 – DHCP Configuration
9. Lab 9 – NAT Configuration
10. Lab 10 – ACL Configuration
11. Lab 11 – DNS Simulation
12. Lab 12 – Network Troubleshooting
13. Best Practices
14. Suggested Challenges

---

# 🖥 Lab 1 – Basic Network Connectivity

## Objective

Connect two PCs through a switch and verify communication.

### Devices

- 1 Switch
- 2 PCs

### Tasks

- Connect PCs using Copper Straight-Through cables.
- Assign IP addresses:
  - PC1 → 192.168.1.10/24
  - PC2 → 192.168.1.20/24
- Verify connectivity using:

```bash
ping 192.168.1.20
```

### Expected Result

Both PCs should successfully communicate.

---

# 🔀 Lab 2 – Switch Configuration

## Objective

Configure a Cisco switch.

### Tasks

- Change hostname.
- Configure console password.
- Configure enable secret.
- Save configuration.

Useful commands:

```bash
hostname Switch1

enable secret Cisco123

service password-encryption

copy running-config startup-config
```

---

# 🌐 Lab 3 – VLAN Configuration

## Objective

Create VLANs and assign ports.

### Devices

- 1 Switch
- 3 PCs

### Tasks

Create:

- VLAN 10 (HR)
- VLAN 20 (Finance)
- VLAN 30 (IT)

Assign ports to VLANs.

Verify:

```bash
show vlan brief
```

Expected Result:

Devices in different VLANs should not communicate.

---

# 🔁 Lab 4 – Inter-VLAN Routing

## Objective

Enable communication between VLANs.

### Devices

- Router
- Switch
- 3 PCs

### Tasks

- Configure trunk port.
- Configure Router-on-a-Stick.
- Create subinterfaces.
- Assign gateways.

Verify:

```bash
ping
```

Expected Result:

All VLANs should communicate.

---

# 🛣 Lab 5 – Static Routing

## Objective

Configure communication between two networks.

### Devices

- 2 Routers
- 2 Switches
- 4 PCs

### Tasks

- Configure interfaces.
- Assign IP addresses.
- Configure static routes.

Example:

```bash
ip route 192.168.20.0 255.255.255.0 10.0.0.2
```

Verify:

```bash
show ip route
```

---

# 🌍 Lab 6 – RIP Routing

## Objective

Configure RIP Version 2.

### Tasks

```bash
router rip

version 2

network 192.168.1.0

network 10.0.0.0

no auto-summary
```

Verify:

```bash
show ip route
```

---

# 🚀 Lab 7 – OSPF Routing

## Objective

Configure single-area OSPF.

### Tasks

```bash
router ospf 1

network 192.168.1.0 0.0.0.255 area 0

network 10.0.0.0 0.0.0.3 area 0
```

Verify:

```bash
show ip ospf neighbor

show ip route
```

---

# 📡 Lab 8 – DHCP Configuration

## Objective

Configure the router as a DHCP server.

### Tasks

Create DHCP Pool.

Example:

```bash
ip dhcp pool OFFICE

network 192.168.10.0 255.255.255.0

default-router 192.168.10.1

dns-server 8.8.8.8
```

Verify that PCs receive IP addresses automatically.

---

# 🌍 Lab 9 – NAT Configuration

## Objective

Configure PAT (NAT Overload).

### Tasks

```bash
access-list 1 permit 192.168.1.0 0.0.0.255

ip nat inside source list 1 interface G0/1 overload
```

Verify:

```bash
show ip nat translations
```

---

# 🔒 Lab 10 – ACL Configuration

## Objective

Block or allow network traffic using ACLs.

### Tasks

Configure Standard ACL.

```bash
access-list 10 permit 192.168.1.0 0.0.0.255

interface G0/0

ip access-group 10 in
```

Verify connectivity.

---

# 🌐 Lab 11 – DNS Simulation

## Objective

Configure DNS in Packet Tracer.

### Devices

- DNS Server
- PCs

### Tasks

- Configure DNS Server.
- Add A Record.
- Configure PCs to use the DNS server.
- Access a website using the hostname.

Expected Result:

The hostname should resolve successfully.

---

# 🛠 Lab 12 – Network Troubleshooting

## Objective

Troubleshoot common networking issues.

### Scenario 1

Incorrect IP Address

Fix:

- Verify IP
- Verify Subnet Mask
- Verify Gateway

---

### Scenario 2

Wrong VLAN

Verify:

```bash
show vlan brief
```

---

### Scenario 3

Routing Failure

Verify:

```bash
show ip route
```

---

### Scenario 4

DHCP Failure

Check:

- DHCP Pool
- Gateway
- Lease

---

### Scenario 5

DNS Failure

Verify:

```bash
nslookup
```

---

### Scenario 6

ACL Blocking Traffic

Verify:

```bash
show access-lists
```

---

# 💡 Best Practices

- Label every device clearly.
- Save configurations frequently.
- Verify every configuration step.
- Test connectivity after each change.
- Document your topology.

---

# 🎯 Suggested Challenges

### Challenge 1

Create a network with:

- 2 Routers
- 2 Switches
- 6 PCs

Configure:

- Static Routing
- DHCP
- VLANs

---

### Challenge 2

Configure:

- VLAN 10
- VLAN 20
- Inter-VLAN Routing

Verify communication.

---

### Challenge 3

Configure OSPF between three routers.

Verify neighbor relationships.

---

### Challenge 4

Configure NAT and ACL together.

Allow only HTTP traffic from one subnet.

---

### Challenge 5

Create a small office network that includes:

- VLANs
- DHCP
- DNS
- NAT
- Static Routing
- ACLs

Verify that all services work correctly.

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- Cisco Packet Tracer Documentation
- CompTIA Network+

---

## 🔗 Related Documents

- [README](README.md)
- [OSI-Model](OSI-Model.md)
- [TCP-IP](TCP-IP.md)
- [IP-Addressing](IP-Addressing.md)
- [Subnetting](Subnetting.md)
- [VLAN](VLAN.md)
- [Switching](Switching.md)
- [Routing](Routing.md)
- [DNS](DNS.md)
- [DHCP](DHCP.md)
- [NAT](NAT.md)
- [ACL](ACL.md)
- [Network-Troubleshooting](Network-Troubleshooting.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
