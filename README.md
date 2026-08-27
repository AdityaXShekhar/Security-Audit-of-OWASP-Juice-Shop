# OWASP Juice Shop - Security Assessment Report

## Overview
This repository contains the documentation and findings of a structured security assessment performed against a local instance of **OWASP Juice Shop**[cite: 1]. The objective of this engagement was to map the application's attack surface, evaluate authentication mechanisms, test input validation, and identify vulnerabilities aligned with the OWASP Top 10 Web Application Security Risks[cite: 1]. 

## Target Application
* **Application:** OWASP Juice Shop (Node.js web application)[cite: 1].
* **Purpose:** An intentionally vulnerable web application maintained by the OWASP Foundation for security training and awareness[cite: 1].
* **Deployment:** Localhost (TCP Port 3000)[cite: 1].

## Tools & Technologies Used
The following tools were utilized during the penetration testing phases[cite: 1]:
* **Kali Linux:** Primary testing operating system environment[cite: 1].
* **Nmap:** Used for active host discovery, port scanning, and service version detection[cite: 1].
* **Burp Suite:** Intercepting proxy utilized for request/response analysis and manipulation of authentication and feedback forms[cite: 1].
* **OWASP ZAP:** Supplementary tool for automated vulnerability scanning[cite: 1].

## Key Vulnerabilities Identified
The assessment successfully identified and exploited multiple vulnerabilities mapping to the OWASP Top 10[cite: 6]:
* **Broken Access Control:** Discovered the hidden administrative Score Board via unauthenticated routing[cite: 6].
* **Injection (DOM & Reflected XSS):** Achieved arbitrary script execution using crafted iframe payloads in search and comment fields[cite: 6].
* **Sensitive Data Exposure:** Accessed confidential internal documents without proper authorization[cite: 6].
* **Security Misconfiguration:** Provoked unhandled application errors revealing internal stack traces[cite: 6].
* **Improper Input Validation:** Bypassed client-side constraints to submit a zero-star rating and retrieved restricted image assets via manipulated paths[cite: 6].
* **Unvalidated Redirects:** Exploited an outdated external allowlist to trigger a redirect to a Blockchain address[cite: 6].

## Disclaimer
All testing activities documented in this repository were performed entirely against a local, isolated instance of the application for educational purposes as part of a cybersecurity training program[cite: 1]. No third-party systems or production data were targeted[cite: 1].
