Vulnerability Assessment report


## Executive Summary

A report that present the security assessment findings conducted on testphp.vulnweb.com

The main reason to conduct this report was to identify the potential vulnerabilities that may impact (CIA) security, confidentiality and availability of the system.

---

## Tools and the Scope used for this Assessment
   - Website    : testphp.vulnweb.com
   - Tools used : Nmap
               , OWASP ZAP
               , Browser DevTools
   - Date       : 01 March 2026

---
## Methodology

 I've used the network scanning and passive vulnerability analysis techniques. This objective was to identify potential security weaknesses in the target website.

 ### Network Scanning (Nmap)
 - Tool used to scan the target server to identify open ports and running services. it determine the potential weakness the attakers use to exploit.

### Passive Vulnerability Scanning (OWASP ZAP)
- To detect potential web application vulnerabilities without actively attacking the system. Scan identified security issues as missing HTTP security headers which could expose the website to attakers.

---
## My findings

   ID          | Vulnerability                 | Risk level                | Impact
   
   1 -     Missing Security Headers | Medium      | May allow clickjacking
   
   2 -     Open Port 80 (HTTP)      | Low         | Traffic not encrypted 

---

## *Detailed Findings*


 ###  Open Port 80 (HTTP)
   
   **Risk Level:**  
   - Low  
   
   **State:** 
   - Open
   
   **Description:**  
   - the website accepts connections over HTTP — so the data is sent in plain text instead of being encrypted.
   
   **Business Impact:**  
   - information sent between a user and a server can be captured or read by someone else during transmission.
   
   **Recommendation:**  
   - Redirect HTTP traffic to HTTPS and enforce TLS encryption.
  

   
### Missing Security Headers

   **Risk Level:** 
   - Medium  

  **Description:**  
   - The web server does not implement certain HTTP security headers.
   
   **Business Impact:**  
   - Attackers may exploit this port to perform attacks such as clickjacking.
   
   **Recommendation:**  
   - Configure the web server to implement necessary security headers to avoid the system to be exploited by the attackers.

---


## Conclusion
- The evaluation revealed that there are minor to moderate vulnerabilities on the website. Implementing the recommended security measures will strengthen the website security.

---
## Evidence

 (7.1) Nmap screenshot

<img width="1365" height="766" alt="Screenshot 2026-03-01 200204" src="https://github.com/user-attachments/assets/82f11b43-435d-45cb-8ad8-60ed7504c764" />


 (7.2) OWASP ZAP screenshot

 <img width="1365" height="766" alt="Screenshot 2026-03-01 200204" src="https://github.com/user-attachments/assets/2fc140d0-101a-41a4-96fc-1b9b9985dfd2" />

Internship: Cyber Security Intern  
Organization: Future Interns
