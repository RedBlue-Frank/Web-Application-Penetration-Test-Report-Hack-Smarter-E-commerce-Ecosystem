# Web-Application-Penetration-Test-Report-Hack-Smarter-E-commerce-Ecosystem
A comprehensive security assessment of a target e-commerce platform, identifying vulnerabilities ranging from Critical (SQLi, RCE) to Low severity. This project demonstrates end-to-end "Grey Box" testing methodologies, manual exploitation, and remediation strategies

## Overview
This repository contains a detailed **Web Application Penetration Test** report for the "Hack Smarter" (HSL) e-commerce ecosystem. Conducted as a **Grey Box** engagement, the assessment focuses on identifying and documenting high-risk security weaknesses that could lead to full system compromise.

**Assessor:** Frank Sheunesu Nhatarikwa

**Engagement Period:** March 2, 2026 – March 6, 2026

---

##  Executive Summary
The assessment uncovered a total of **25 findings**, with a significant concentration of high-impact vulnerabilities:
* **2 Critical**
* **8 High**
* **12 Medium**
* **1 Low**
* **2 Information**

### Key Technical Findings
* **SQL Injection (Critical):** Unauthorized database extraction via the product search functionality.
* **Remote Code Execution (RCE) (Critical):** Full system takeover through unrestricted file uploads in the administrative panel.
* **Server-Side Request Forgery (SSRF):** Exploited to perform Local File Read (LFR) and leak `/etc/passwd`.
* **Insecure Direct Object Reference (IDOR):** Administrative account impersonation in forum threads.
* **Broken Access Control:** Business logic flaws allowing the purchase of restricted items.

---

##  Assessment Scope
* **Target:** `hacksmarter.hsm` 
* **Environment:** Externally facing web applications.
* **Methodology:** Manual investigation of injection, authentication, authorization, and client-side attack vectors.

---

##  Remediation Strategy
The report provides a multi-tiered remediation roadmap, including:
1. **Critical Hotfixes:** Web server hardening and disabling diagnostic scripts like `phpinfo()`.
2. **Software Fixes:** Transitioning to parameterized queries and strict file extension whitelisting.
3. **Defense-in-Depth:** Implementation of Content Security Policies (CSP) and rate limiting.

---

##  Disclaimer
This report is shared strictly for **educational and training purposes**. All testing was performed in an authorized, controlled environment. Unauthorized use of these techniques against live systems is illegal.
