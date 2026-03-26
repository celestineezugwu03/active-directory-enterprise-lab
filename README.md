# Active Directory Enterprise Lab Environment

This project simulates a small enterprise Windows Server infrastructure using Active Directory Domain Services (AD DS).

The environment demonstrates centralized authentication, DNS configuration, organizational unit structure, role-based access control (RBAC), NTFS permissions, and Access-Based Enumeration (ABE).

---

## Infrastructure Overview

Domain Name:
corp.local

Components:

• Windows Server Domain Controller  
• Windows 10 Domain-joined Client  
• Active Directory Domain Services (AD DS)  
• DNS Configuration  
• Organizational Units (HR, IT, Marketing)  
• Security Groups for RBAC  
• NTFS Permissions  
• SMB Share Configuration  
• Access-Based Enumeration (ABE)

---

## Lab Objectives

This lab demonstrates how enterprise environments:

• Deploy domain controllers  
• Configure DNS authentication infrastructure  
• Organize users using OUs  
• Implement RBAC with security groups  
• Secure departmental file access  
• Troubleshoot domain join failures  
• Apply NTFS and Share permissions  
• Restrict folder visibility using ABE  

---

## File Server Structure

C:\TESTCompanyData

HR  
IT  
Marketing  

Access permissions enforced using security groups:

HR → HR_Staff  
IT → IT_Admins, IT_Support  
Marketing → Marketing_Staff  

Access-Based Enumeration ensures users only see authorized folders.

---

## Troubleshooting Scenarios Simulated

• Domain join failure  
• DNS misconfiguration  
• Firewall blocking connectivity  
• Permission inheritance conflicts  
• Share visibility without file access  

---

## Skills Demonstrated

Active Directory Domain Services  
DNS configuration  
OU design  
Group policy validation  
Security group management  
NTFS permissions  
Share permissions  
Access-Based Enumeration  
RBAC implementation  
Enterprise file server architecture  

---

## Troubleshooting Scenarios Simulated

During deployment, several realistic infrastructure issues were identified and resolved:

• Windows 10 Home edition cannot join domains  
• Incorrect DNS configuration prevented domain discovery  
• Firewall rules blocked communication between virtual machines  
• Permission inheritance exposed unintended folder visibility  
• Share permissions conflicted with NTFS permissions  

Each issue was diagnosed and corrected using enterprise troubleshooting methodology.
