# Networkwalks-B084-week4-PenetrationTesting

# Mediroza General Hospital – Web Application Penetration Testing

**Internship Project | NetworkWalks B084**

![Security](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Focus](https://img.shields.io/badge/Focus-Web%20Application%20Pentesting-blue)
![Role](https://img.shields.io/badge/Role-Junior%20Penetration%20Tester-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview

This project involved performing a penetration test against the Mediroza General Hospital web application as part of my cybersecurity internship at NetworkWalks.

The primary objective was to assess the security of the target application, identify potential vulnerabilities, evaluate access-control weaknesses, and examine the security of password-protected patient laboratory reports.

The assessment focused on identifying weaknesses that could potentially expose sensitive information and compromise the confidentiality of application data.

## 🎯 Objectives

- Identify exposed services and accessible network ports.
- Assess the security of the patient portal authentication mechanism.
- Test for SQL Injection vulnerabilities.
- Evaluate authentication and access-control weaknesses.
- Assess the security of password-protected PDF laboratory reports.
- Demonstrate the potential impact of identified vulnerabilities.
- Document findings and provide remediation recommendations.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Penetration testing environment |
| Nmap | Network scanning and service discovery |
| pdf2john | Extracting password hashes from PDF files |
| Dictionary Attack | Testing PDF password strength |
| Browser Developer Tools | Web application assessment |
| Linux Terminal | Command execution and analysis |

## 🔍 Testing Methodology

### 1. Reconnaissance and Network Scanning

Performed initial reconnaissance and scanned the target to identify accessible services and open ports.

**Observed results:**
- Port 80 – HTTP (Open)
- Port 443 – HTTPS (Open)
- Other scanned TCP ports were filtered.

### 2. Patient Portal Authentication Testing

Assessed the patient portal login functionality and identified an authentication weakness involving SQL Injection.

The testing demonstrated that the authentication mechanism could be bypassed, resulting in access to the patient portal.

### 3. Patient Information Exposure

After obtaining portal access, examined the accessible patient laboratory reports.

The portal exposed multiple patient reports containing sensitive information, including:
- Patient identification information.
- Laboratory report details.
- Medical test results.
- Report reference numbers.

This demonstrated the potential impact of unauthorized access to confidential healthcare information.

### 4. PDF Password Security Assessment

Downloaded the password-protected laboratory PDF reports available through the portal and evaluated their password protection.

**Testing process:**

1. Extracted PDF password hashes using `pdf2john`.
2. Examined the extracted hash information.
3. Performed dictionary-based password testing.
4. Identified matching passwords for the tested PDF documents.
5. Verified access to the protected PDF contents.

This assessment demonstrated weaknesses in the password strength used to protect confidential documents.

## ⚠️ Key Security Findings

| ID | Finding | Severity |
|---|---|---|
| F1 | SQL Injection – Authentication Bypass | High |
| F2 | Unauthorized Access to Sensitive Patient Information | High |
| F3 | Weak Password Protection on PDF Reports | Medium |

*Severity classifications are based on the assessment report and should be reviewed against the organisation's risk-rating criteria.*

## 🛡️ Recommendations

### SQL Injection
- Use parameterized SQL queries and prepared statements.
- Implement secure input validation.
- Avoid dynamically constructing SQL queries using user input.
- Apply secure authentication practices.

### Sensitive Information Exposure
- Implement proper role-based access control (RBAC).
- Restrict patient records to authorized users.
- Implement session management and access-control validation.
- Maintain access logs and monitoring.

### PDF Password Security
- Enforce strong, unique passwords for confidential documents.
- Avoid predictable or commonly used passwords.
- Apply appropriate encryption standards.
- Review document access and distribution procedures.

## 📚 Learning Outcomes

Through this assessment, I gained practical experience in:

- Network reconnaissance and service discovery.
- Web application penetration testing.
- Understanding and testing SQL Injection.
- Authentication bypass assessment.
- Identifying sensitive information exposure.
- PDF password security assessment.
- Linux-based security tools and command-line operations.
- Vulnerability documentation and report preparation.

## 📄 Project Documentation

A detailed penetration testing report was prepared as part of the internship deliverable.

**Note:** The complete report is not publicly distributed because it contains confidential assessment evidence and sensitive information. Sanitized screenshots or demonstrations may be shared separately where permitted.

## 👨‍💻 Author

**Utsav Kumar Thakur**

Junior Penetration Tester  
NetworkWalks – Batch B084

**Area of Interest:** Penetration Testing | VAPT | Ethical Hacking | Web Application Security

---

## ⚖️ Disclaimer

This project was conducted as part of an assigned cybersecurity internship assessment. The activities described are intended for authorized security testing and educational purposes only.

No credentials, patient records, password hashes, or other confidential information are included in this public repository. Do not attempt to reproduce these activities against systems without explicit authorization.

---

Classification: Confidential — Client Use Only
