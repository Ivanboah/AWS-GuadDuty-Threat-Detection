# 🛡️ AWS GuardDuty Threat Detection Project  
[![AWS](https://img.shields.io/badge/AWS-CloudSecurity-orange?logo=amazon-aws&logoColor=white)](https://aws.amazon.com/guardduty)  
[![Juice Shop](https://img.shields.io/badge/OWASP-Juice%20Shop-blue)](https://owasp.org/www-project-juice-shop/)  
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

## 📚 Table of Contents  
- [Overview](#overview)  
- [Project Setup](#project-setup)  
- [Simulated Attacks](#simulated-attacks)  
- [GuardDuty Findings](#guardduty-findings)  
- [Key Takeaways](#key-takeaways)  
- [Technologies Used](#technologies-used)

---

## 🔎 Overview  
This repository documents a hands-on threat detection project using **AWS GuardDuty**, focused on identifying cloud-native vulnerabilities through attack simulations. The goal was to test GuardDuty’s response to real-world threats in a controlled lab environment.

---

## ⚙️ Project Setup  
Deployed the following components using a CloudFormation template:
- Vulnerable web application: **OWASP Juice Shop**
- AWS services: S3, EC2, CloudShell
- Security: Amazon GuardDuty with malware protection enabled

---

## 🚨 Simulated Attacks  
<details>
<summary>Click to expand attack scenarios</summary>

| 🧪 Attack Type            | 🔧 Technique Used                                 | ⚠️ Impact                     |
|--------------------------|--------------------------------------------------|-------------------------------|
| SQL Injection            | Malicious SQL used to bypass login               | Unauthorized access           |
| Command Injection        | JS injected via username field                   | System-level command execution |
| Credential Exfiltration | Stolen EC2 credentials used via CloudShell       | S3 bucket access              |
| Malware Simulation       | Uploaded [EICAR test file](https://www.eicar.org/) | Triggered malware alert       |

</details>

---

## 🛡️ GuardDuty Findings  
GuardDuty promptly identified threats with the following alerts:

- `UnauthorizedAccess:IAMUser/InstanceCredentialExfiltration.InsideAWS`
- `Object:S3/MaliciousFile`  
Each finding included metadata such as:
- IAM roles used  
- S3 bucket targeted  
- Attacker IP and timestamps  
- AWS account details

---

## 🧠 Key Takeaways  
- Validated GuardDuty’s real-time detection across multiple threat vectors  
- Improved understanding of IAM misconfigurations and public resource exposure  
- Gained hands-on experience with security automation and threat forensics  
- Reinforced cloud security best practices and governance strategies  

---

## 🛠 Technologies Used  

| Category       | Tools & Services |
|----------------|------------------|
| Cloud Security | AWS GuardDuty, IAM |
| Web App        | OWASP Juice Shop |
| Infrastructure | AWS S3, EC2, CloudShell |
| Automation     | AWS CloudFormation |
| CLI Tools      | `wget`, `jq`, `cat` |

---

> ✨ _“Security isn’t just a checklist—it’s a mindset. GuardDuty gives you eyes on everything.”_

---

📌 _Want to collaborate, give feedback, or explore AWS security tooling together? Feel free to connect or open an issue on this repo._

# AWS-GuadDuty-Threat-Detection
