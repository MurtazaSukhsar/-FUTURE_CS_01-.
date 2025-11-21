🛡️ Web Application Security Assessment – OWASP Juice Shop

This repository documents a complete web application penetration test performed against the OWASP Juice Shop application.
The assessment includes manual testing, automated scanning, XSS, SQL Injection, misconfiguration analysis, and a full professional report.

📌 Project Overview

This project simulates a real-world client engagement where a web application is tested for vulnerabilities following the OWASP Top 10 methodology.

You will find:

✔ Manual exploitation (XSS, SQL Injection)

✔ Automated scanning with OWASP ZAP

✔ Vulnerability analysis & screenshots

✔ Full professional PDF report

✔ PowerPoint presentation for clients

✔ Risk ratings & remediation steps

⚙️ Tools Used
Tool	Purpose
OWASP ZAP	Automated scanning, spidering, passive & active analysis
Kali Linux	Penetration testing environment
Browser DevTools	Manual payload injection
python-pptx	Generating PowerPoint
ReportLab	Creating PDF report
🎯 Scope of Assessment

Target: OWASP Juice Shop (http://localhost:4000/)

Attack Surface:

Search functionality

Login page

API endpoints (observed via ZAP)

UI components & JavaScript files

Testing Focus:

Injection flaws

Authentication weaknesses

Security misconfigurations

Vulnerable dependencies

🛑 Key Findings
🔸 1. Reflected Cross-Site Scripting (XSS)

Location: Search bar
Payload:

"/><img src=x onerror=alert('XSS')>


Impact:

JavaScript execution

Session hijacking risk

Stored cookie extraction attacks

Fix: Input sanitization, output encoding, implement CSP.

🔸 2. SQL Injection – Login Page

Payloads tested:

' OR '1'='1' --
admin' --
' OR 1=1--


Impact:

Authentication bypass

Unauthorized access

Database compromise

Fix: Use prepared statements, parameterized queries.

🔸 3. Security Misconfigurations

From OWASP ZAP:

Missing Content Security Policy

Cross-domain misconfigurations

Session ID in URL

Timestamp disclosure

Weak or missing security headers

Vulnerable JavaScript library detected

📊 OWASP Top 10 Mapping
OWASP Category	Status
A01 Broken Access Control	Not Observed
A02 Cryptographic Failures	Not Observed
A03 Injection	✔ XSS & SQLi Confirmed
A04 Insecure Design	CSP Missing
A05 Security Misconfiguration	✔ Confirmed
A06 Vulnerable Components	✔ Detected
A07 Authentication Failures	Possible Risk
A08 Integrity Failures	Not Observed
A09 Logging Failures	Not Tested
A10 SSRF	Not Observed
📸 Evidence Screenshots

XSS popup

ZAP alerts panel

Login page (authenticated)

Application dashboard

(All included in the full PDF report)

📁 Deliverables
📄 Professional PDF Report

A fully corporate-style assessment report including PoC screenshots, severity ratings, and remediation steps.
File: Professional_Web_App_Security_Report.pdf

📊 PowerPoint Presentation

Client-friendly slides summarizing vulnerabilities and recommendations.
File: Web_Application_Security_Report_Final_With_SQLi_and_Screenshot.pptx

🚀 Running Juice Shop (for reviewers)
docker run -p 4000:3000 bkimminich/juice-shop


Access the app:
👉 http://localhost:4000/

👤 Author

Murtaza Sukhsarwala
Aspiring Cybersecurity Analyst | Web Penetration Tester
