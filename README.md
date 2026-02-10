# DIRECTORY-BRUTEFORCE-SCAN-REPORT-DIRB-
This report documents the result of a directory brute-force scan conducted on the target website using the DIRB tool. The purpose of the scan was to identify publicly accessible directories and files that could expose sensitive information or increase the attack surface of the web application.
---

### DIRECTORY BRUTEFORCE SCAN REPORT (DIRB)
* Target: http://testfire.net.
* Tool Used: DIRB
* Date: 03/02/2026
* Tester: ORTUANYA, L. CHIMA
* Purpose: Security Assessment
---

## EXECUTIVE SUMMARY
 
This report documents the result of a directory brute-force scan conducted on the target website using the DIRB tool. The purpose of the scan was to identify publicly accessible directories and files that could expose sensitive information or increase the attack surface of the web application

## SCOPE OF TESTING

The assessment was limited to directory enumeration on the target website using DIRB.
No exploitation or modification of data was performed during the scan.

```

TOOL USED:
 DIRB (Directory Brute Forcer) is a web content scanner used to discover hidden directories and files on a web server by using predefined wordlists.
METHODOLOGY: 
The scan was performed by running DIRB against the target URL using a default wordlist.
DIRB sent HTTP requests to the server and analyzed responses such as status codes (200, 301, 403) to identify existing directories and files.
    Wordlist used: 
    Scan mode: Default
```
---
**FINDINGS** :
 <img width="937" height="850" alt="image" src="https://github.com/user-attachments/assets/e78a0148-0e0e-4bd0-b613-51cb15603911" />
 



**ANALYSIS OF FINDINGS:**
The scan revealed several directories that are accessible or partially accessible. Directories returning 200 OK indicate publicly available content, while Directories with 301/302 REDIRECTS suggest existing paths that may lead to restricted or protected resources.
Directories returning 403 FORBIDDEN indicate that access is restricted but directory exists, which may still be valuable information for attackers.

**SECURITY IMPACT:**
Exposed directories can provide attackers with useful information about the application structure. 
If sensitive directories such as admin panels, backups, or upload folders are not properly secured, they may lead to unauthorized access or data leakage.

---
**RECOMMENDATIONS:**

*  Disable directory listing
*		Restrict access to sensitive directories
*		Use strong authentication for admin areas
*		Remove unused files and folders
*		Implement web application Firewall (WAF)
*		Monitor unusual scanning activity

**CONCLUSION :**
    The DIRB scan provided insight into the directory structure of the target website. While directory enumeration alone does not confirm vulnerabilities, it highlights potential entry points that should be reviewed and secured to reduce attack surface.

