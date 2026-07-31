# 🌐 Domain Name System (DNS)

> A beginner-friendly guide to understanding the Domain Name System (DNS), how it works, DNS records, troubleshooting, and practical networking examples.

---

# 📌 Objective

This document explains the Domain Name System (DNS), its purpose, how name resolution works, common DNS record types, troubleshooting techniques, and essential commands used in Networking, IT Support, and Cyber Security.

---

# 📚 Table of Contents

1. What is DNS?
2. Why is DNS Important?
3. How DNS Works
4. DNS Hierarchy
5. Types of DNS Servers
6. Common DNS Record Types
7. Forward Lookup vs Reverse Lookup
8. Public DNS Servers
9. Common DNS Commands
10. DNS Troubleshooting
11. Practical Lab
12. Best Practices
13. Common Mistakes
14. Interview Questions

---

# 🧠 What is DNS?

DNS (Domain Name System) translates human-readable domain names into IP addresses.

Instead of remembering:

```
142.250.190.14
```

You simply type:

```
www.google.com
```

DNS finds the correct IP address and allows your browser to connect to the website.

---

# 🎯 Why is DNS Important?

DNS helps to:

- Convert domain names into IP addresses
- Make websites easy to access
- Support email delivery
- Improve user experience
- Enable Internet communication

Without DNS, users would need to remember IP addresses instead of domain names.

---

# ⚙️ How DNS Works

When you visit a website:

```
www.example.com
```

The process is:

```
User
   │
Browser
   │
DNS Resolver
   │
Root DNS Server
   │
TLD Server (.com)
   │
Authoritative DNS Server
   │
Returns IP Address
   │
Browser connects to the Web Server
```

Example:

```
www.google.com

↓

142.250.x.x
```

---

# 🌍 DNS Hierarchy

DNS is organized in a hierarchical structure:

```
.

↓

.com

↓

google

↓

www
```

Levels:

- Root Domain (.)
- Top-Level Domain (TLD)
- Second-Level Domain
- Hostname

Example:

```
www.google.com
```

- Hostname → www
- Domain → google
- TLD → .com

---

# 🖥 Types of DNS Servers

## Recursive Resolver

Receives DNS queries from clients and finds the correct answer.

---

## Root Name Server

Directs the query to the appropriate Top-Level Domain server.

---

## TLD (Top-Level Domain) Server

Handles domains such as:

- .com
- .org
- .net
- .edu

---

## Authoritative DNS Server

Stores the actual DNS records for the domain and returns the final answer.

---

# 📋 Common DNS Record Types

| Record | Purpose |
|----------|-------------------------------|
| A | Maps a domain to an IPv4 address |
| AAAA | Maps a domain to an IPv6 address |
| CNAME | Creates an alias for another hostname |
| MX | Mail server record |
| NS | Name server record |
| TXT | Stores text information (SPF, verification, etc.) |
| PTR | Reverse DNS lookup |

---

# 🔄 Forward Lookup vs Reverse Lookup

## Forward Lookup

Converts:

```
Domain Name

↓

IP Address
```

Example:

```
google.com

↓

142.250.x.x
```

---

## Reverse Lookup

Converts:

```
IP Address

↓

Domain Name
```

Usually performed using PTR records.

---

# 🌐 Popular Public DNS Servers

| Provider | Primary DNS | Secondary DNS |
|-----------|-------------|---------------|
| Google | 8.8.8.8 | 8.8.4.4 |
| Cloudflare | 1.1.1.1 | 1.0.0.1 |
| Quad9 | 9.9.9.9 | 149.112.112.112 |
| OpenDNS | 208.67.222.222 | 208.67.220.220 |

---

# 🛠 Common DNS Commands

## Linux

Check DNS configuration:

```bash
cat /etc/resolv.conf
```

DNS lookup:

```bash
nslookup google.com
```

Detailed DNS query:

```bash
dig google.com
```

---

## Windows

DNS lookup:

```cmd
nslookup google.com
```

Display DNS cache:

```cmd
ipconfig /displaydns
```

Flush DNS cache:

```cmd
ipconfig /flushdns
```

Renew IP configuration:

```cmd
ipconfig /renew
```

---

# 🔍 DNS Troubleshooting

### Verify Internet Connectivity

```bash
ping 8.8.8.8
```

If this works but domain names fail, the issue is likely DNS.

---

### Test DNS Resolution

```bash
nslookup google.com
```

---

### View DNS Configuration

Linux:

```bash
cat /etc/resolv.conf
```

Windows:

```cmd
ipconfig /all
```

---

### Test Another DNS Server

Example:

```
8.8.8.8
```

or

```
1.1.1.1
```

---

# 💻 Practical Lab

## Task 1

Check your IP address.

Linux

```bash
ip a
```

Windows

```cmd
ipconfig
```

---

## Task 2

Test Internet connectivity.

```bash
ping 8.8.8.8
```

---

## Task 3

Perform a DNS lookup.

```bash
nslookup google.com
```

---

## Task 4

Run a detailed DNS query.

```bash
dig google.com
```

(Linux only)

---

## Task 5

Change your DNS server (Lab Environment).

Test with:

- Google DNS
- Cloudflare DNS

Verify website access after the change.

---

# 💡 Best Practices

- Use reliable DNS providers.
- Keep DNS records updated.
- Monitor DNS performance.
- Use secure DNS where possible (DoH/DoT).
- Document internal DNS records.

---

# ⚠️ Common Mistakes

❌ Assuming Internet issues are always DNS-related.

❌ Forgetting to flush the DNS cache after changes.

❌ Using incorrect DNS server addresses.

❌ Ignoring DNS record propagation delays.

❌ Confusing DNS with DHCP.

---

# 🎯 Interview Questions

1. What is DNS?
2. Why is DNS important?
3. What is the purpose of an A record?
4. What is the difference between an A record and a CNAME record?
5. What is an MX record used for?
6. What is the difference between forward and reverse lookup?
7. What is the purpose of a Recursive Resolver?
8. Which command performs a DNS lookup?
9. What does `dig` do?
10. How would you troubleshoot a DNS issue?

---

# 📖 References

- Cisco CCNA Official Cert Guide
- Cisco Networking Academy
- RFC 1034
- RFC 1035
- CompTIA Network+

---

## 🔗 Related Documents

- [Networking README](README.md)
- [TCP-IP](TCP-IP.md)
- [IP Addressing](IP-Addressing.md)
- [DHCP](DHCP.md)
- [Routing](Routing.md)
- [Network Troubleshooting](Network-Troubleshooting.md)

---

⭐ **Created by Faisal Mehmood**

**IT Support | Networking | Cyber Security**
