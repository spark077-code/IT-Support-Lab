# DNS Enumeration Cheat Sheet

A quick reference guide for common DNS Enumeration commands used during reconnaissance and penetration testing.

---

# DNS Records

| Record | Purpose |
|---------|---------|
| A | Maps a domain to an IPv4 address |
| AAAA | Maps a domain to an IPv6 address |
| NS | Displays authoritative name servers |
| MX | Shows mail exchange servers |
| TXT | Displays text records such as SPF, DKIM, or verification |
| SOA | Shows Start of Authority information |
| CNAME | Alias for another domain |
| PTR | Reverse DNS lookup |

---

# DIG

### Find IPv4 Address

```bash
dig A example.com
```

### Find Name Servers

```bash
dig NS example.com
```

### Find Mail Servers

```bash
dig MX example.com
```

### Find TXT Records

```bash
dig TXT example.com
```

### Short Output

```bash
dig NS example.com +short
```

### Zone Transfer

```bash
dig AXFR @ns1.example.com example.com
```

---

# NSLOOKUP

```bash
nslookup example.com
```

```bash
nslookup -type=NS example.com
```

```bash
nslookup -type=MX example.com
```

```bash
nslookup -type=TXT example.com
```

---

# HOST

```bash
host example.com
```

```bash
host -t NS example.com
```

```bash
host -t MX example.com
```

---

# DNSRECON

```bash
dnsrecon -d example.com
```

---

# DNSENUM

```bash
dnsenum example.com
```

```bash
dnsenum --enum example.com
```

---

# NMAP

DNS Brute Force

```bash
nmap --script dns-brute example.com
```

DNS Zone Transfer

```bash
nmap --script dns-zone-transfer --script-args dns-zone-transfer.domain=example.com ns1.example.com
```

---

# Common Mistakes

❌ Wrong

```bash
dig NS example.com .short
```

✅ Correct

```bash
dig NS example.com +short
```

---

❌ Wrong

```bash
nmap --script dns-zone-transfer --script-args dns-zone-transfer.domain=example.com
```

✅ Correct

```bash
nmap --script dns-zone-transfer --script-args dns-zone-transfer.domain=example.com example.com
```

---

# Notes

- Perform DNS enumeration only on systems you own or are authorized to test.
- Zone transfers are usually disabled on production DNS servers.
- Use multiple tools to validate results.
- Public DNS information can reveal valuable reconnaissance data.

---

# Quick Revision

✓ A Record → IPv4

✓ AAAA → IPv6

✓ MX → Mail Server

✓ NS → Name Server

✓ TXT → Text Record

✓ SOA → Start of Authority

✓ PTR → Reverse Lookup

✓ CNAME → Alias Record
