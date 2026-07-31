# DNS Records Explained

This document explains the most common DNS record types used during DNS Enumeration and penetration testing.

---

# A Record (Address Record)

## Purpose

Maps a domain name to an IPv4 address.

## Example

```bash
dig A example.com
```

## Sample Output

```
example.com.    300    IN    A    93.184.216.34
```

## Security Importance

A Records reveal the IPv4 address of a target server, which can be used during reconnaissance and network scanning.

---

# AAAA Record (IPv6 Address Record)

## Purpose

Maps a domain name to an IPv6 address.

## Example

```bash
dig AAAA example.com
```

## Security Importance

Shows whether the target supports IPv6, which may expose additional attack surfaces if not properly secured.

---

# NS Record (Name Server)

## Purpose

Identifies the authoritative DNS servers responsible for a domain.

## Example

```bash
dig NS example.com
```

## Sample Output

```
ns1.example.com
ns2.example.com
```

## Security Importance

Knowing the authoritative nameservers helps during DNS reconnaissance and zone transfer testing.

---

# MX Record (Mail Exchange)

## Purpose

Specifies the mail servers responsible for receiving emails for a domain.

## Example

```bash
dig MX example.com
```

## Sample Output

```
10 mail.example.com
```

## Security Importance

Mail servers can become targets for phishing assessments, email security testing, and SPF/DKIM validation.

---

# TXT Record

## Purpose

Stores text-based information related to a domain.

Common uses include:

- SPF
- DKIM
- Domain Verification
- DMARC

## Example

```bash
dig TXT example.com
```

## Security Importance

TXT records help evaluate email security configurations and domain verification settings.

---

# SOA Record (Start of Authority)

## Purpose

Contains administrative information about a DNS zone.

## Example

```bash
dig SOA example.com
```

## Information Included

- Primary Name Server
- Administrator Email
- Serial Number
- Refresh Time
- Retry Time
- Expire Time

## Security Importance

Useful for understanding DNS zone configuration and synchronization details.

---

# CNAME Record (Canonical Name)

## Purpose

Creates an alias that points one domain name to another.

## Example

```bash
dig CNAME www.example.com
```

## Security Importance

Helps identify third-party services and understand domain redirection.

---

# PTR Record (Pointer Record)

## Purpose

Performs Reverse DNS Lookup by mapping an IP address back to a domain name.

## Example

```bash
host 8.8.8.8
```

## Sample Output

```
8.8.8.8.in-addr.arpa domain name pointer dns.google.
```

## Security Importance

Useful for server identification, email verification, and network troubleshooting.

---

# Summary Table

| Record | Purpose | Example |
|---------|---------|---------|
| A | Maps Domain → IPv4 | 192.168.1.10 |
| AAAA | Maps Domain → IPv6 | 2001:db8::1 |
| NS | Name Server | ns1.example.com |
| MX | Mail Server | mail.example.com |
| TXT | Text Information | SPF / DKIM |
| SOA | Zone Information | Primary DNS |
| CNAME | Alias Record | www → example.com |
| PTR | Reverse Lookup | IP → Domain |

---

# Key Takeaways

- A and AAAA records identify IP addresses.
- NS records identify authoritative DNS servers.
- MX records identify mail servers.
- TXT records often contain SPF, DKIM, and DMARC information.
- SOA records describe the DNS zone configuration.
- CNAME records create aliases between domains.
- PTR records are used for reverse DNS lookups.

---

# Disclaimer

This document is intended for educational purposes only. Perform DNS enumeration only on systems that you own or have explicit permission to test.
