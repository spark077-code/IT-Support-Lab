# 🌐 DNS Enumeration Lab

> **Hands-on Cybersecurity Reconnaissance Project**

---

# 📖 Overview

This repository documents a hands-on **DNS Enumeration Lab** performed in an authorized learning environment. It demonstrates how industry-standard reconnaissance tools collect publicly available DNS information during the information gathering phase of a penetration test.

---

# 🎯 Objectives

- Understand DNS Enumeration
- Identify DNS Records (A, AAAA, MX, NS, SOA, TXT)
- Test DNS Zone Transfer
- Discover Publicly Available Subdomains
- Practice Ethical Reconnaissance

---

# 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| `dig` | DNS Queries & Zone Transfer Testing |
| `nslookup` | DNS Lookups |
| `host` | DNS Record Lookup |
| `dnsrecon` | DNS Enumeration |
| `dnsenum` | DNS Enumeration & Subdomain Discovery |
| `Nmap (NSE)` | DNS Enumeration Scripts |
| `HackerTarget` | Online DNS Reconnaissance |

---

# 💻 Lab Environment

- Kali Linux
- Terminal
- Internet Connection
- Authorized Target / Lab Environment

---

# 📑 DNS Record Types

| Record | Description |
|---------|-------------|
| **A** | IPv4 Address |
| **AAAA** | IPv6 Address |
| **NS** | Name Server |
| **MX** | Mail Server |
| **TXT** | Text Record |
| **SOA** | Start of Authority |
| **CNAME** | Canonical Name |
| **PTR** | Reverse Lookup |

---

# ✅ Practical Tasks

- DNS Zone Transfer (`dig`)
- `nslookup`
- HackerTarget
- `dnsrecon`
- `dnsenum`
- Nmap DNS Enumeration
- `host` Command

---

# 💡 Common Commands

```bash
dig NS example.com +short

host -t MX example.com

nslookup example.com

dnsrecon -d example.com

dnsenum example.com

nmap --script dns-brute example.com
```

---

# 🎓 Learning Outcomes

- Performed DNS reconnaissance using multiple tools.
- Collected and interpreted common DNS records.
- Understood DNS Zone Transfer testing.
- Learned how reconnaissance supports penetration testing.
- Practiced ethical information gathering techniques.

---

# 🔧 Troubleshooting

- Use `+short` instead of `.short` with the `dig` command.
- Nmap requires a valid scan target in addition to script arguments.
- Verify DNS resolution and internet connectivity before performing scans.

---

# 📌 Conclusion

This project demonstrates practical DNS Enumeration using industry-standard tools. The exercises illustrate how publicly available DNS information can be collected, how DNS configurations can be evaluated for common security issues such as unrestricted zone transfers, and why DNS reconnaissance is a critical component of penetration testing and security assessments.

---

# ⚠️ Disclaimer

This repository is intended **for educational purposes only**. All demonstrations and techniques should be performed only against systems and domains for which you have **explicit authorization**. Do **not** use these techniques against systems you do not own or do not have permission to test.

---

## 👨‍💻 Author

**Faisal Mehmood**

*Cybersecurity Learner • Networking Enthusiast • Continuous Learner*
Author

Faisal Mehmood Cybersecurity Learner | Networking Enthusiast |Continuous Learner
