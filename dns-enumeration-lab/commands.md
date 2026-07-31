# DNS Enumeration Commands

This document contains the commands used during the DNS Enumeration Lab.

---

# 1. DIG

## Find A Record

```bash
dig A example.com
```

## Find Nameservers

```bash
dig NS example.com
```

## Short Output

```bash
dig NS example.com +short
```

## Find Mail Servers

```bash
dig MX example.com
```

## Find TXT Records

```bash
dig TXT example.com
```

## Find SOA Record

```bash
dig SOA example.com
```

## DNS Zone Transfer

```bash
dig AXFR @ns1.example.com example.com
```

---

# 2. NSLOOKUP

```bash
nslookup example.com
```

```bash
nslookup -type=MX example.com
```

```bash
nslookup -type=NS example.com
```

```bash
nslookup -type=TXT example.com
```

---

# 3. HOST

```bash
host example.com
```

```bash
host -t A example.com
```

```bash
host -t NS example.com
```

```bash
host -t MX example.com
```

```bash
host -t AAAA example.com
```

---

# 4. DNSRECON

```bash
dnsrecon -d example.com
```

```bash
dnsrecon -d example.com -t std
```

---

# 5. DNSENUM

```bash
dnsenum example.com
```

```bash
dnsenum --enum example.com
```

---

# 6. NMAP

```bash
nmap --script dns-brute example.com
```

```bash
nmap --script dns-zone-transfer --script-args dns-zone-transfer.domain=example.com ns1.example.com
```

---

# 7. Online DNS Lookup

HackerTarget DNS Lookup

https://hackertarget.com/dns-lookup/
