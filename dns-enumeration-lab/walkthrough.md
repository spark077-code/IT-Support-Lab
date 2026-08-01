# DNS Enumeration Lab Walkthrough

This walkthrough provides a step-by-step guide to the DNS Enumeration Lab performed during the reconnaissance phase of a penetration test. Each section includes the objective, command, screenshot, observations, and learning outcomes.

> **Note:** Replace the image filenames with your actual screenshots stored inside the `images/` directory.

---

# Lab Overview

## Objective

The purpose of this lab is to learn how to gather publicly available DNS information using industry-standard tools.

## Tools Used

- dig
- nslookup
- HackerTarget
- dnsrecon
- dnsenum
- Nmap (NSE Scripts)
- host

---

# Step 1 – DNS Zone Transfer using dig

## Objective

Determine whether the target DNS server allows an unrestricted DNS Zone Transfer (AXFR).

## Command

```bash
dig AXFR @nsztm1.digi.ninja zonetransfer.me
```

## Screenshot

```text
images/dig-zone-transfer.png
```

```markdown
![DNS Zone Transfer](images/dig-zone-transfer.png)
```

## Observation

- The DNS server responded to the AXFR request.
- DNS records were returned successfully.
- This indicates that DNS Zone Transfer was permitted.

## Learning Outcome

DNS Zone Transfers should normally be restricted. If enabled publicly, an attacker may obtain valuable DNS information during reconnaissance.

---

# Step 2 – DNS Lookup using nslookup

## Objective

Retrieve DNS records for the target domain.

## Command

```cmd
nslookup -type=MX zonetransfer.me
```

## Screenshot

```text
images/nslookup-mx-record.png
```

```markdown
![nslookup MX Record](images/nslookup-mx-record.png)
```

## Observation

- Multiple MX records were identified.
- Google mail servers were configured for the domain.
- MX preference values determined mail server priority.

## Learning Outcome

MX records help identify the email infrastructure of a target domain and are useful during information gathering.

---

# Step 3 – Online DNS Enumeration (HackerTarget)

## Objective

Collect publicly available DNS information using an online reconnaissance tool.

## Website

https://hackertarget.com/dns-lookup/

## Screenshot

```text
images/hackertarget.png
```

```markdown
![HackerTarget](images/hackertarget.png)
```

## Observation

- DNS information was collected successfully.
- Multiple DNS records were displayed.

## Learning Outcome

Online reconnaissance tools provide a quick overview of publicly available DNS information.

---

# Step 4 – DNS Enumeration using dnsrecon

## Objective

Perform automated DNS enumeration.

## Command

```bash
dnsrecon -d zonetransfer.me
```

## Screenshot

```text
images/dnsrecon-output.png
```

```markdown
![dnsrecon Output](images/dnsrecon-output.png)
```

## Observation

- DNS records were successfully identified.
- Name servers and other DNS information were collected.

## Learning Outcome

dnsrecon automates DNS reconnaissance and reduces manual effort.

---

# Step 5 – DNS Enumeration using dnsenum

## Objective

Perform comprehensive DNS enumeration.

## Command

```bash
dnsenum zonetransfer.me
```

## Screenshot

```text
images/dnsenum-output.png
```

```markdown
![dnsenum Output](images/dnsenum-output.png)
```

## Observation

- DNS records were collected successfully.
- Zone transfer testing was performed.
- Public DNS information was identified.

## Learning Outcome

dnsenum combines several DNS enumeration techniques into a single tool.

---

# Step 6 – DNS Enumeration using Nmap

## Objective

Perform DNS enumeration using Nmap NSE scripts.

## Commands

```bash
nmap --script dns-brute zonetransfer.me
```

```bash
nmap --script dns-zone-transfer --script-args dns-zone-transfer.domain=zonetransfer.me nsztm1.digi.ninja
```

## Screenshot

```text
images/nmap-dns-enumeration.png
```

```markdown
![Nmap DNS Enumeration](images/nmap-dns-enumeration.png)
```

## Observation

- DNS-related NSE scripts executed successfully.
- DNS information was collected.
- Zone Transfer testing was completed.

## Learning Outcome

Nmap extends DNS enumeration capabilities through powerful NSE scripts.

---

# Step 7 – DNS Lookup using host

## Objective

Retrieve DNS records using the host command.

## Command

```bash
host zonetransfer.me
```

## Screenshot

```text
images/host-command.png
```

```markdown
![Host Command](images/host-command.png)
```

## Observation

- DNS records were resolved successfully.
- Basic DNS information was retrieved.

## Learning Outcome

The host command provides a simple and efficient way to query DNS records.

---

# Overall Lab Summary

| Task | Status |
|------|--------|
| DNS Zone Transfer (dig) | ✅ Completed |
| nslookup | ✅ Completed |
| HackerTarget | ✅ Completed |
| dnsrecon | ✅ Completed |
| dnsenum | ✅ Completed |
| Nmap DNS Enumeration | ✅ Completed |
| host Command | ✅ Completed |

---

# Skills Gained

- DNS Enumeration
- DNS Record Analysis
- Zone Transfer Testing
- Information Gathering
- Reconnaissance Techniques
- Kali Linux
- Nmap NSE
- Linux Command Line

---

# Key Takeaways

- DNS Enumeration is an essential part of reconnaissance.
- Different tools provide different types of DNS information.
- Zone Transfers should never be publicly accessible.
- Combining multiple tools improves reconnaissance accuracy.
- Ethical hacking should always be performed with proper authorization.

---

# Conclusion

This lab successfully demonstrated practical DNS Enumeration using industry-standard tools. The exercises provided hands-on experience in collecting publicly available DNS information, understanding DNS infrastructure, and evaluating DNS configurations for common security weaknesses. These skills are fundamental for penetration testers, security analysts, and cybersecurity professionals.

---

# Disclaimer

This walkthrough is intended for educational purposes only. Perform all DNS enumeration activities only on systems and domains for which you have explicit authorization. Unauthorized testing may violate laws and organizational policies.
