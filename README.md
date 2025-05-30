# Vulnerability Scan Report - OpenVAS
**Attacker Machine**: Kali Linux  
**Victim Machine**: Windows 10 VM  
**Target IP**: 192.168.163.129  
**Scanner Used**: OpenVAS (Greenbone Community Edition)  
**Scan Duration**: ~45 minutes  

---

## Scan Summary

| Vulnerability Name           | Severity | CVE ID         | CVSS Score | Description |
|-----------------------------|----------|----------------|------------|-------------|
| SMBv1 Enabled               | High     | CVE-2017-0144  | 9.8        | SMBv1 is outdated and vulnerable to ransomware attacks like WannaCry. |
| Outdated OpenSSL Version   | Medium   | CVE-2022-0778  | 7.5        | Vulnerability in OpenSSL could lead to DoS attacks. |
| Unpatched Windows Services | High     | Multiple       | 8.5        | Several Windows services are outdated and missing patches. |
| Weak SSH Cipher Suites     | Medium   | N/A            | 6.5        | Use of deprecated ciphers in SSH configuration. |
| Exposed RDP Port (3389)    | Medium   | N/A            | 6.8        | RDP port is exposed and may allow brute-force attacks. |

## Fixes & Mitigations

- **Disable SMBv1**: via Group Policy or registry editor.
- **Update OpenSSL**: Run `choco upgrade openssl` or install latest version.
- **Patch Windows Services**: Use Windows Update or WSUS.
- **Restrict RDP**: Use firewall rules or VPN access.
- **Disable Weak SSH Ciphers**: Edit SSH config and restart SSH service.

---

## Top 3 Critical Vulnerabilities

1. SMBv1 Enabled  
2. Unpatched Windows Services  
3. Outdated OpenSSL Version  

---
