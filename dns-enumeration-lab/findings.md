# DNS Enumeration Findings

This document summarizes the findings obtained during the DNS Enumeration Lab.

---

# Assessment Summary

| Task | Tool | Status |
|------|------|--------|
| DNS Zone Transfer | dig | ✅ Completed |
| DNS Lookup | nslookup | ✅ Completed |
| Online DNS Lookup | HackerTarget | ✅ Completed |
| DNS Enumeration | dnsrecon | ✅ Completed |
| DNS Enumeration | dnsenum | ✅ Completed |
| DNS Enumeration | Nmap NSE | ✅ Completed |
| DNS Lookup | host | ✅ Completed |

---

# Finding 1 – DNS Zone Transfer (dig)

## Objective

Determine whether the target DNS server allows unrestricted zone transfers.

## Command

```bash
dig AXFR @nameserver target-domain
```

## Observation

- The DNS server was tested for zone transfer.
- No unrestricted DNS zone transfer was identified during testing.

## Conclusion

The DNS server appears to be configured securely against unauthorized zone transfer requests.

---

# Finding 2 – nslookup

## Objective

Retrieve DNS information for the target domain.

## Commands

```bash
nslookup target-domain
```

```bash
nslookup -type=MX target-domain
```

## Observation

- Successfully retrieved DNS records.
- Nameserver and mail server information was available.

## Conclusion

Public DNS information was successfully collected.

---

# Finding 3 – HackerTarget

## Objective

Perform online DNS reconnaissance.

## Observation

- Public DNS information was collected using an online reconnaissance service.

## Conclusion

Online tools can provide a quick overview of publicly available DNS information.

---

# Finding 4 – dnsrecon

## Objective

Perform automated DNS enumeration.

## Command

```bash
dnsrecon -d target-domain
```

## Observation

- DNS records were successfully identified.
- Enumeration completed successfully.

## Conclusion

dnsrecon provides an efficient method for collecting DNS information.

---

# Finding 5 – dnsenum

## Objective

Perform comprehensive DNS enumeration.

## Command

```bash
dnsenum target-domain
```

## Observation

- DNS records were collected.
- Common DNS enumeration techniques were executed.
- Zone transfer checks were performed.

## Conclusion

dnsenum automates multiple reconnaissance tasks and improves enumeration efficiency.

---

# Finding 6 – Nmap DNS Enumeration

## Objective

Perform DNS enumeration using Nmap NSE scripts.

## Commands

```bash
nmap --script dns-brute target-domain
```

```bash
nmap --script dns-zone-transfer --script-args dns-zone-transfer.domain=target-domain nameserver
```

## Observation

- DNS scripts executed successfully.
- Zone transfer testing was completed.
- Public DNS information was analyzed.

## Conclusion

Nmap provides flexible DNS enumeration through its NSE scripting engine.

---

# Finding 7 – Host Command

## Objective

Retrieve DNS records using the host command.

## Command

```bash
host target-domain
```

## Observation

- DNS records were successfully resolved.

## Conclusion

The host command provides a simple and efficient method for DNS lookups.

---

# Overall Findings

During this lab, multiple DNS enumeration tools were used to collect publicly available DNS information. The assessment demonstrated how different tools complement each other during reconnaissance by identifying DNS records, nameservers, mail servers, and other publicly accessible information.

No unauthorized exploitation was performed, and testing remained focused on information gathering in an authorized learning environment.

---

# Final Conclusion

This lab provided practical experience with industry-standard DNS enumeration tools commonly used by penetration testers and security professionals. The exercises improved understanding of DNS infrastructure, reconnaissance methodologies, and the importance of securing DNS services against common misconfigurations.
