## Day 29: Supply Chain Security

### Objective
Learn how SOC analysts detect, investigate, and respond to supply chain attacks targeting trusted software, vendors, and third-party services.

---

# What is Supply Chain Security?

Supply Chain Security protects software, hardware, vendors, third-party services, and software dependencies from cyber threats and malicious compromise.

Organizations rely on trusted vendors, software updates, cloud services, and open-source libraries. Attackers target these trusted systems to distribute malware or gain unauthorized access.

---

# Why Supply Chain Attacks are Dangerous

- Target trusted software  
- Affect multiple organizations  
- Spread malware through updates  
- Bypass traditional security defenses  

---

# Common Supply Chain Threats

## 1. Malicious Software Updates
Attackers inject malware into legitimate software updates.

### Risks
- Malware infections  
- Backdoors  
- Credential theft  
- Data exfiltration  

---

## 2. Compromised Vendors
Attackers breach third-party vendors to attack customers.

### Risks
- Trusted relationship abuse  
- Enterprise compromise  
- Large-scale attacks  

---

## 3. Dependency Hijacking
Malicious code is inserted into software libraries or dependencies.

### Risks
- Remote code execution  
- Backdoor installation  
- Supply chain compromise  

---

## 4. Fake Software Packages
Attackers distribute trojanized or fake applications.

### Risks
- Ransomware  
- Spyware  
- Malware installation  

---

# Common Attack Indicators

- Suspicious behavior after updates  
- Unknown external network connections  
- Modified application files  
- Unexpected PowerShell activity  
- Unknown DLL files  
- Suspicious processes  
- File hash mismatches  

---

# Example Investigation

## Alert
Suspicious activity detected after software update installation.

## Findings
- Application connected to malicious domain  
- Unknown DLL files detected  
- Suspicious PowerShell execution observed  

## Analysis
Possible supply chain compromise detected.

### Risk Level
**CRITICAL**

---

# Detection Techniques

## Verify Digital Signatures
Validate software authenticity using trusted vendor certificates.

## Monitor Software Integrity
Check for unauthorized file modifications and hash mismatches.

## Analyze Update Behavior
Monitor applications for suspicious activity after updates.

## Monitor Vendor Activity
Track vendor security incidents and suspicious behavior.

---

# SOC Workflow

```text
Software Update Installed
            ↓
Suspicious Activity Detected
            ↓
SOC Investigation
            ↓
Containment
```

---

# Workflow Explanation

## 1. Software Update Installed
A software update is deployed in the environment.

## 2. Suspicious Activity Detected
Security tools detect unusual behavior such as:
- Unknown connections  
- Malicious DLL files  
- Suspicious PowerShell activity  

## 3. SOC Investigation
SOC analysts investigate:
- File integrity  
- Network traffic  
- Threat intelligence matches  

## 4. Containment
SOC teams:
- Isolate affected systems  
- Block malicious domains/IPs  
- Remove malicious files  

---

# SOC Team Responsibilities

## L1 Analyst – Monitoring & Triage
- Monitor alerts  
- Review suspicious software activity  
- Escalate incidents  

## L2 Analyst – Investigation
- Analyze applications and logs  
- Investigate malicious behavior  
- Review suspicious network traffic  

## L3 Analyst – Threat Hunting & Engineering
- Perform threat hunting  
- Improve detection logic  
- Conduct advanced malware analysis  

---

# Famous Supply Chain Attacks

## SolarWinds Attack (2020)
Malicious code inserted into trusted software updates.

## Kaseya Attack (2021)
Ransomware distributed through remote management software.

## CCleaner Attack (2017)
Malware added to legitimate software downloads.

---

# Response & Mitigation Strategies

## Immediate Response Actions
- Isolate affected systems  
- Block malicious IPs/domains  
- Stop malicious processes  
- Remove compromised software  

## Investigation
- Review software installation logs  
- Analyze file integrity  
- Check network activity  

## Containment
- Restrict network communication  
- Quarantine infected systems  
- Disable compromised applications  

## Recovery
- Restore clean backups  
- Reinstall trusted software  
- Apply patches  
- Validate system integrity  

## Prevention
- Verify digital signatures  
- Use trusted repositories  
- Conduct vendor risk assessments  
- Monitor software integrity  
- Implement application allowlisting  

---

# Assignment

## 1. Explain Supply Chain Security
Supply Chain Security protects software, vendors, and third-party services from cyber threats that may compromise systems or data.

---

## 2. Research Famous Supply Chain Attacks

Examples:
- SolarWinds  
- Kaseya  
- CCleaner  

---

## 3. Analyze Malicious Update Scenario

### Scenario
A software update is installed and suspicious activity begins immediately afterward.

### Findings
- Unknown DLL files detected  
- Malicious network connections observed  
- Suspicious PowerShell execution identified  

### Analysis
The update may have been compromised and used to distribute malware.

### Recommended Actions
- Isolate affected systems  
- Block malicious domains  
- Verify software integrity  
- Investigate vendor compromise  

---

# Summary

Supply chain attacks target trusted software, vendors, and third-party services to compromise organizations. These attacks are difficult to detect because they originate from legitimate applications and trusted infrastructure.

SOC analysts use SIEM, EDR/XDR, threat intelligence, integrity monitoring, and behavioral analysis to detect and respond to supply chain compromises effectively.

---

# Key Takeaway

Strong software validation, vendor monitoring, integrity checks, and rapid SOC response are essential for detecting and mitigating supply chain attacks.
