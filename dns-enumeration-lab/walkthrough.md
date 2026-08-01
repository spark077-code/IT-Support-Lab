# DNS Enumeration Lab Walkthrough

> **Course:** Cyber Security / Ethical Hacking Lab  
> **Lab Title:** DNS Enumeration  
> **Category:** Information Gathering (Reconnaissance)  
> **Platform:** Kali Linux & Windows Command Prompt  
> **Tools:** dig, nslookup, host, dnsrecon, dnsenum, Nmap, HackerTarget

---

# Aim

The aim of this practical lab is to understand DNS Enumeration techniques and perform information gathering using industry-standard tools. The lab demonstrates how publicly available DNS records can be collected during the reconnaissance phase of a penetration test.

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Kali Linux |
| Additional Platform | Windows Command Prompt |
| Internet Connection | Required |
| Target Domain | `zonetransfer.me` (Authorized Learning Target) |

---

# Tool 1 – dig

## Objective

Test whether the target DNS server permits DNS Zone Transfer (AXFR).

### Command

```bash
dig AXFR @nsztm1.digi.ninja zonetransfer.me
```

### Screenshots

> **Figure 1.1 – DNS Zone Transfer Request**

`images/dig-zone-transfer1.png`

> **Figure 1.2 – DNS Zone Transfer Results**

`images/dig-zone-transfer2.png`

> *(Later, replace these with a single collage image such as `images/dig-collage.png`.)*

### Observation

- DNS Zone Transfer request executed successfully.
- DNS records were returned by the server.

### Result

The server allowed DNS Zone Transfer for the lab environment.

---

# Tool 2 – nslookup

## Objective

Retrieve Mail Exchange (MX) records.

### Command

```cmd
nslookup -type=MX zonetransfer.me
```

### Screenshots

Figure 2.1

`images/nslookup-mx-record1.png`

Figure 2.2

`images/nslookup-mx-record2.png`

Figure 2.3

`images/nslookup-mx-record3.png`

Figure 2.4

`images/nslookup-mx-record4.png`

Figure 2.5

`images/nslookup-mx-record5.png`

> *(Later replace with `images/nslookup-collage.png`.)*

### Observation

- Multiple MX records were identified.
- Google Workspace mail servers were detected.
- MX priorities were displayed successfully.

### Result

The mail infrastructure of the target domain was identified.

---

# Tool 3 – HackerTarget

## Objective

Perform online DNS reconnaissance.

### Website

https://hackertarget.com/dns-lookup/

### Screenshot

Figure 3.1

`images/Hacker-target.png`

### Observation

- Public DNS information was successfully retrieved.

### Result

Online reconnaissance confirmed publicly available DNS records.

---

# Tool 4 – dnsrecon

## Objective

Perform automated DNS Enumeration.

### Command

```bash
dnsrecon -d zonetransfer.me
```

### Screenshots

Figure 4.1

`images/dnsrecon-output1.png`

Figure 4.2

`images/dnsrecon-output2.png`

Figure 4.3

`images/dnsrecon-output3.png`

Figure 4.4

`images/dnsrecon-output4.png`

Figure 4.5

`images/dnsrecon-output5.png`

Figure 4.6

`images/dnsrecon-output6.png`

> *(Later replace with `images/dnsrecon-collage.png`.)*

### Observation

- DNS records were collected successfully.
- Nameservers and other DNS information were identified.

### Result

Automated DNS Enumeration completed successfully.

---

# Tool 5 – dnsenum

## Objective

Perform comprehensive DNS Enumeration.

### Command

```bash
dnsenum zonetransfer.me
```

### Screenshots

Figure 5.1

`images/dnsenum-output1.png`

Figure 5.2

`images/dnsenum-output2.png`

Figure 5.3

`images/dnsenum-output3.png`

Figure 5.4

`images/dnsenum-output4.png`

Figure 5.5

`images/dnsenum-output5.png`

> *(Later replace with `images/dnsenum-collage.png`.)*

### Observation

- DNS records were collected successfully.
- Zone Transfer checks were completed.
- Public information was gathered.

### Result

Comprehensive DNS Enumeration was completed successfully.

---

# Tool 6 – Nmap DNS Enumeration

## Objective

Perform DNS Enumeration using Nmap NSE scripts.

### Commands

```bash
nmap --script dns-brute zonetransfer.me
```

```bash
nmap --script dns-zone-transfer --script-args dns-zone-transfer.domain=zonetransfer.me nsztm1.digi.ninja
```

### Screenshot

Figure 6.1

`images/nmap-dns-enumeration.png`

### Observation

- NSE scripts executed successfully.
- DNS-related information was collected.

### Result

Nmap successfully performed DNS Enumeration.

---

# Tool 7 – host Command

## Objective

Retrieve DNS information using the host command.

### Command

```bash
host zonetransfer.me
```

### Screenshot

Figure 7.1

`images/host-command.png`

### Observation

- DNS records were resolved successfully.

### Result

The host command successfully retrieved DNS information.

---

# Practical Summary

| Tool | Purpose | Status |
|------|---------|--------|
| dig | DNS Zone Transfer | ✅ Completed |
| nslookup | DNS Lookup | ✅ Completed |
| HackerTarget | Online Enumeration | ✅ Completed |
| dnsrecon | Automated Enumeration | ✅ Completed |
| dnsenum | Comprehensive Enumeration | ✅ Completed |
| Nmap | NSE DNS Scripts | ✅ Completed |
| host | DNS Lookup | ✅ Completed |

---

# Learning Outcomes

After completing this lab, I was able to:

- Understand DNS Enumeration techniques.
- Identify common DNS record types.
- Perform DNS Zone Transfer testing.
- Use multiple enumeration tools for reconnaissance.
- Interpret DNS information collected during assessments.
- Understand the role of reconnaissance in penetration testing.

---

# Conclusion

This practical lab successfully demonstrated DNS Enumeration using multiple industry-standard tools. Publicly available DNS information was collected, analyzed, and interpreted to understand how reconnaissance supports penetration testing and security assessments. The lab also emphasized the importance of properly securing DNS infrastructure to reduce information disclosure risks.

---

# Disclaimer

This project was conducted in an authorized learning environment for educational purposes only. All testing should be performed only against systems or domains for which explicit permission has been obtained.
