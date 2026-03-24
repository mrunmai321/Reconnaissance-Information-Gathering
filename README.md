# Reconnaissance-Information-Gathering
 gather domain-related information
## Objective
Perform basic reconnaissance to gather domain-related information using publicly available tools.
## Target
http://testphp.vulnweb.com  
## Description
This challenge focuses on the **reconnaissance phase** of cybersecurity, where publicly available information about a target domain is collected.
Using basic networking tools like `whois` and `nslookup`, we can gather:
- Domain registration details  
- IP address  
- DNS records  
- Name server information  
This information helps in understanding the target environment before performing further security testing.
##  Tools Used
 whois  
- nslookup  
##  Steps to Reproduce
### 1. Open Terminal
Launch terminal (Linux / Windows CMD / PowerShell)

---

### 2. Run WHOIS Command
```bash
whois testphp.vulnweb.com
````

### Output Includes:

* Registrar details
* Domain creation & expiry date
* Registrant information

---

### 3. Run NSLOOKUP Command

```bash
nslookup testphp.vulnweb.com
```
 Output Includes:

* IP address
* DNS resolution details

### 4. Retrieve Specific DNS Records

#### Name Server Records:

```bash
nslookup -type=ns testphp.vulnweb.com
```

#### Mail Exchange Records:

```bash
nslookup -type=mx testphp.vulnweb.com
```
## Mitigation & Security Considerations

Reconnaissance is a **passive activity**, but organizations can reduce exposure by:

* Enabling WHOIS privacy protection
* Limiting publicly available domain information
* Using split-horizon DNS to restrict internal data visibility


