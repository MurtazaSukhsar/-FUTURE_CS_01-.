# 🛡️ Web Application Security Assessment – OWASP Juice Shop

This repository documents a complete **web application penetration test** performed against the **OWASP Juice Shop** application.

## 📌 Project Overview
A real-world style assessment covering:
- Manual testing
- Automated scanning (OWASP ZAP)
- XSS exploitation
- SQL Injection testing
- Misconfiguration analysis
- Full PDF and PPTX reports

## ⚙️ Tools Used
- OWASP ZAP
- Kali Linux
- Browser DevTools
- python-pptx
- ReportLab

## 🎯 Scope
Target: http://localhost:4000  
Focus: Injection, Authentication, Security Headers, Components

## 🛑 Key Findings
### 1. Reflected XSS
Payload:
```
"/><img src=x onerror=alert('XSS')>
```

### 2. SQL Injection – Login Page
Payloads:
```
' OR '1'='1' --
admin' --
' OR 1=1--
```

### 3. Security Misconfigurations
- Missing CSP
- Session ID in URL
- Vulnerable JS Libraries

## 📊 OWASP Top 10 Mapping
A03, A05, A06 confirmed

## 📁 Deliverables
- Professional PDF report
- Zap Scan report
- video and screenshot
|- Zap scan mp4

## 👤 Author
Murtaza Sukhsarwala
