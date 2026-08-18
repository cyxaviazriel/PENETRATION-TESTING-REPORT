<div align="center">

# 🛡️ PENETRATION TESTING REPORT

### 🔎 FOOTPRINTING & NETWORK SCANNING PHASES

<img src="https://img.shields.io/badge/CYBERSECURITY-NETWORKWALKS-0A66C2?style=for-the-badge&logo=hackthebox&logoColor=white" />
<img src="https://img.shields.io/badge/WEEK%202-B082-6F42C1?style=for-the-badge" />
<img src="https://img.shields.io/badge/STATUS-IN%20PROGRESS-F59E0B?style=for-the-badge" />
<img src="https://img.shields.io/badge/AUTHORIZED-YES-22C55E?style=for-the-badge" />

<br>

**W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS**

### 👤 Alebiosu Oluwadamilare Samuel
**Cybersecurity Professional | Networkwalks Intern | Batch B082**

---

</div>

## 📋 Engagement Overview

| **Category** | **Details** |
|---|---|
| 👤 **Pentester** | Alebiosu Oluwadamilare Samuel |
| 🎓 **Program / Batch** | B082 Networkwalks |
| 📅 **Assessment Date** | 18 August 2026 |
| 🧪 **Modules Completed** | W2-PM1 Multiple Kali Tools<br>W2-PM5 — Zenmap Scanning |
| 🎯 **Assessment Targets** | Networkwalks — Authorized Target<br>My Own Local LAN Network |
| 🔐 **Authorization** | ✅ Written Permission Secured |
| 🔎 **Phase 1** | Reconnaissance & Footprinting |
| 🌐 **Phase 2** | Scanning & Network Discovery |
| 🚧 **Phases 3–5** | In Progress |
| 🖥️ **Primary Platforms** | Kali Linux & Windows |

---

# ⚠️ 1. Liability & Authorization Disclaimer

> **AUTHORIZED SECURITY TESTING ONLY**

All activities documented in this report were performed only against systems and devices for which I had appropriate authorization, including systems belonging to me.

This project is intended strictly for **educational, cybersecurity research, ethical hacking, and professional development purposes**.

Unauthorized access, scanning, enumeration, exploitation, or interference with computer systems may violate applicable laws and regulations.

**Do not use the techniques, commands, or information contained in this repository against systems without explicit authorization.**

The author, instructor, and Networkwalks are not responsible for misuse of the information contained within this project.

> 🔐 **Security principle:** Always define and respect the authorized scope before performing reconnaissance or security testing.

---

# 🎯 2. Introduction

This penetration testing report documents the practical cybersecurity activities completed during **Week 2 of my Networkwalks internship program**.

The assessment focused on two major stages of the penetration testing lifecycle:

### 🔎 Phase 1 Reconnaissance & Footprinting

Publicly available information was collected from the **networkwalks.com** domain using multiple Kali Linux reconnaissance tools.

### 🌐 Phase 2 Scanning & Network Discovery

Zenmap was used to perform network discovery against my **own local network**, identifying active hosts and collecting IP and MAC address information.

Together, these activities demonstrate how a security professional can progress from:

```text
Public Information
       ↓
Reconnaissance
       ↓
Technology Identification
       ↓
DNS Enumeration
       ↓
Network Discovery
       ↓
Host Identification
```

All reconnaissance activities were performed in an authorized educational context.

Each activity was documented with:

- 🖥️ Command/tool used
- 📊 Observed result
- 📸 Supporting evidence
- 🔎 Security relevance
- ⚠️ Potential risk
- 🛡️ Recommended mitigation

---

# 🧰 3. Tools & Technologies

| **Tool / Technology** | **Purpose** |
|---|---|
| 🐉 **Kali Linux** | Security testing and reconnaissance environment |
| 🪟 **Windows** | Local network identification and Zenmap environment |
| 🔍 **WHOIS** | Domain registration and name-server information |
| 🌐 **WhatWeb** | Web technology and CMS fingerprinting |
| 📡 **Nslookup** | DNS resolution and IP identification |
| 📥 **curl** | HTTP response header analysis |
| 🛡️ **Wafw00f** | Web Application Firewall identification |
| 🗂️ **DNSRecon** | DNS record enumeration |
| 🛰️ **Zenmap / Nmap GUI** | Network discovery and host scanning |
| 💻 **Windows CMD** | Local IP and MAC address identification |

---

# 🔎 4. Activities Performed

## 4.1 🔍 Footprinting & Reconnaissance

I performed authorized reconnaissance against the **networkwalks.com** domain using six Kali Linux tools:

```text
WHOIS
WhatWeb
Nslookup
curl
Wafw00f
DNSRecon
```

Each tool provided a different perspective of the target's publicly observable infrastructure.

---

### 🔹 4.1.1 WHOIS

WHOIS was used to collect publicly available domain registration information and identify relevant domain infrastructure, including name-server information.

**Security relevance:**

WHOIS information can provide an initial understanding of how a domain is registered and which infrastructure is associated with it.

---

### 🔹 4.1.2 WhatWeb

WhatWeb was used to fingerprint technologies exposed by the website.

The observed results identified technologies including:

```text
WordPress 7.0.4
WP Download Manager 3.3.58
```

**Security relevance:**

Technology and version information can assist security professionals in identifying software that may require additional security review.

> ⚠️ Technology identification does **not** automatically indicate that a vulnerability exists.

---

### 🔹 4.1.3 Nslookup

Nslookup was used to resolve the target domain to its associated IP address.

**Observed result:**

```text
192.232.216.135
```

**Security relevance:**

IP resolution provides information about the network location associated with a web service and may support further authorized infrastructure analysis.

---

### 🔹 4.1.4 cURL

The following HTTP-header inspection technique was used:

```bash
curl -I networkwalks.com
```

The response provided additional information about the web application and exposed the following REST API endpoint:

```text
/wp-json/
```

**Security relevance:**

HTTP response information can assist with technology fingerprinting and further authorized enumeration.

---

### 🔹 4.1.5 Wafw00f

Wafw00f was used to determine whether a Web Application Firewall was protecting the target.

**Observed result:**

```text
ModSecurity (SpiderLabs)
```

**Security relevance:**

Identifying defensive technologies can help security professionals understand the security architecture protecting a web application.

---

### 🔹 4.1.6 DNSRecon

DNSRecon was used to enumerate publicly accessible DNS information.

The activity provided information relating to:

- Name servers
- Mail servers
- SPF / TXT records
- Service records
- DNS-related information

**Security relevance:**

DNS information can help create a broader understanding of an organization's publicly exposed infrastructure.

---

# 🌐 4.2 Network Scanning with Zenmap

The second practical activity focused on **network discovery using Zenmap**.

The objective was to:

- Identify the local IP address
- Determine the local subnet
- Discover active hosts
- Identify IP addresses
- Identify MAC addresses
- Generate a network topology

The Windows `ipconfig` command was first used to identify the local network configuration.

The identified subnet was then entered into Zenmap.

### 🔍 Scan Type

```text
Ping Scan
```

The scan was used to identify active devices on the local network.

### Example Hosts Identified

```text
10.0.0.1
10.0.0.4
10.0.0.19
10.0.0.5
```

The practical example also identified associated MAC addresses.

After completing the scan, the **Topology** section in Zenmap was used to visualize the discovered network.

The topology legend was enabled and the resulting network topology was saved in PDF format as required by the practical exercise.

> **Important:** The addresses above represent the example results supplied for the practical. When submitting the final assessment, they should be replaced with the actual results from my authorized local network.

---

# ⚠️ 5. Risk Analysis & Impact

The following observations were identified during the footprinting and network discovery activities.

| # | 🔎 Finding | 📊 Evidence / Observation | ⚠️ Potential Impact | Risk |
|---:|---|---|---|---|
| 1 | Web technology information exposed | WhatWeb identified WordPress and WP Download Manager | Could assist technology fingerprinting and further security review | 🟠 **Medium** |
| 2 | Server IP identifiable | Nslookup resolved the domain to `192.232.216.135` | Provides information about the network location of the web service | 🟢 **Low** |
| 3 | HTTP technical information exposed | curl returned HTTP headers and exposed `/wp-json/` | May assist fingerprinting and further enumeration | 🟢 **Low** |
| 4 | WAF technology identifiable | Wafw00f identified ModSecurity | Reveals information about the web application's defensive architecture | 🟢 **Low** |
| 5 | DNS infrastructure information exposed | DNSRecon identified DNS, mail and service records | Can assist in building an infrastructure profile | 🟠 **Medium** |
| 6 | Multiple live hosts visible | Zenmap identified four hosts in the example network | Unknown devices may represent unauthorized or unmanaged assets | 🟠 **Medium** |

### Risk Rating Key

| Indicator | Severity |
|---|---|
| 🔴 | **Critical** |
| 🟠 | **Medium** |
| 🟢 | **Low** |

> **Important Assessment Note:**  
> These findings represent observations from reconnaissance and network discovery activities. They are **not confirmed vulnerabilities**.

No exploitation or vulnerability validation was performed during these two modules.

The presence of a software version, IP address, DNS record, or HTTP endpoint does not by itself prove that a system is vulnerable.

Additional authorized security testing would be required to validate any suspected vulnerability.

---

# 🛡️ 6. Recommendations

Based on the observations collected during the assessment, the following security improvements are recommended.

### 1️⃣ Review Publicly Exposed Technology Information

Organizations should regularly review publicly exposed information relating to their CMS platforms, plugins, frameworks, and web technologies.

### 2️⃣ Maintain Updated Software

CMS platforms, plugins, frameworks, and other technologies should be regularly updated and monitored against current security advisories.

### 3️⃣ Review HTTP Response Headers

HTTP response headers should be reviewed to determine whether unnecessary technical information is being exposed.

### 4️⃣ Review DNS Records

DNS records should be periodically reviewed to ensure that only required information and services are publicly exposed.

### 5️⃣ Properly Configure & Monitor the WAF

The Web Application Firewall should remain enabled, properly configured, monitored, and regularly tuned according to the organization's security requirements.

### 6️⃣ Perform Regular Internal Network Discovery

Organizations should periodically scan their authorized internal networks to identify active devices and maintain visibility of their infrastructure.

### 7️⃣ Investigate Unknown Devices

Unexpected devices identified during network discovery should be investigated and verified.

### 8️⃣ Maintain Network Documentation

Network topology, IP addresses, devices, and infrastructure documentation should be maintained and updated regularly.

### 9️⃣ Perform Security Testing Within an Authorized Scope

All reconnaissance, scanning, enumeration, and security testing should be performed only against systems and networks where appropriate authorization has been obtained.

---

# 📊 7. Security Assessment Summary

| **Assessment Area** | **Status** |
|---|---|
| 🔎 Reconnaissance | ✅ Completed |
| 🌐 Footprinting | ✅ Completed |
| 🛰️ Network Discovery | ✅ Completed |
| 🖥️ Host Identification | ✅ Completed |
| 🗺️ Network Topology | ✅ Completed |
| 💥 Exploitation | ⏳ Not Performed |
| 🧪 Vulnerability Validation | ⏳ Not Performed |
| 🚧 Advanced Testing | 🔄 In Progress |

### Overall Assessment

```text
RECONNAISSANCE       ████████████████████ 100%
FOOTPRINTING         ████████████████████ 100%
NETWORK DISCOVERY    ████████████████████ 100%
EXPLOITATION         ░░░░░░░░░░░░░░░░░░░░   0%
```

---

# 🎓 8. Key Learning Outcomes

Through these practical exercises, I developed hands-on experience with:

- 🔎 Reconnaissance methodology
- 🌐 Domain footprinting
- 🧩 Web technology fingerprinting
- 📡 DNS enumeration
- 🛡️ WAF identification
- 🛰️ Network discovery
- 🖥️ Host identification
- 📍 IP and MAC address analysis
- 🗺️ Network topology visualization
- 📝 Professional security documentation
- ⚖️ Authorized security testing principles

The exercises demonstrated how much information can be collected before exploitation is even considered.

A cybersecurity professional must therefore understand both **how information can be discovered** and **how organizations can reduce unnecessary exposure**.

---

# 📝 9. Conclusion

During **Week 2 of my Cybersecurity & Ethical Hacking internship at Networkwalks**, I completed practical activities covering **reconnaissance, footprinting, and network scanning**.

During the footprinting phase, I used multiple Kali Linux tools to collect and analyze publicly observable information about the target domain.

I learned how:

```text
WHOIS       → Domain information
WhatWeb     → Web technology fingerprinting
Nslookup    → DNS / IP resolution
cURL        → HTTP header inspection
Wafw00f     → WAF identification
DNSRecon    → DNS enumeration
```

During the network scanning phase, I used **Zenmap** to discover active hosts within my authorized local network environment and examine IP, MAC address, and topology information.

The exercises reinforced an important cybersecurity principle:

> **Effective security testing begins with understanding the environment.**

I also learned the importance of documenting security findings professionally by clearly explaining:

```text
What was performed
        ↓
What was discovered
        ↓
Why it matters
        ↓
What risk it may create
        ↓
How the risk can be reduced
```

Most importantly, these exercises reinforced the requirement that reconnaissance and scanning must always be conducted within an **authorized scope**.

This project represents another step in my development as a cybersecurity professional and contributes to my ongoing practical experience in **ethical hacking, network security, reconnaissance, and security assessment**.

---

# 📸 10. Evidence Collected

Evidence from the practical activities is included below.

### 🔎 Footprinting Evidence

<details>
<summary><b>WHOIS Results</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>WhatWeb Results</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>Nslookup Results</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>cURL Results</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>Wafw00f Results</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>DNSRecon Results</b></summary>

_Add screenshot here._

</details>

### 🌐 Zenmap Evidence

<details>
<summary><b>Windows IP Configuration</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>Zenmap Ping Scan</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>Zenmap Host Discovery</b></summary>

_Add screenshot here._

</details>

<details>
<summary><b>Zenmap Network Topology</b></summary>

_Add screenshot here._

</details>

---

# 🧭 Assessment Progress

```text
PHASE 1
Reconnaissance & Footprinting
████████████████████████████████  COMPLETED ✅

PHASE 2
Scanning & Network Discovery
████████████████████████████████  COMPLETED ✅

PHASE 3
Vulnerability Assessment
████████████████░░░░░░░░░░░░░░░░  IN PROGRESS 🔄

PHASE 4
Exploitation
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  PENDING ⏳

PHASE 5
Reporting & Remediation
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  PENDING ⏳
```

---

# 👤 Author

<div align="center">

### **Alebiosu Oluwadamilare Samuel**

**Cybersecurity Professional | Networkwalks Intern | Batch B082**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Alebiosu%20Oluwadamilare%20Samuel-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alebiosu-soc)

[![GitHub](https://img.shields.io/badge/GitHub-cyxaviazriel-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/cyxaviazriel)

</div>

---

# 📌 Project Information

| **Project Detail** | **Information** |
|---|---|
| 🏢 **Program** | Cybersecurity Program Networkwalks |
| 📅 **Week** | Week 02 |
| 🎓 **Batch** | B082 |
| 🔐 **Project Type** | Authorized Penetration Testing Lab |
| 🔎 **Primary Focus** | Footprinting & Network Scanning |
| 🐉 **Primary OS** | Kali Linux |
| 🛰️ **Scanning Tool** | Zenmap / Nmap |
| 📊 **Assessment Status** | In Progress |
| 📁 **Repository** | GitHub |

---

<div align="center">

### 🛡️ CYBERSECURITY • ETHICAL HACKING • NETWORK SECURITY

**Learn → Practice → Analyze → Secure**

<br>

*W2-PM-FINAL | Networkwalks | B082 | August 2026*

</div>

---
