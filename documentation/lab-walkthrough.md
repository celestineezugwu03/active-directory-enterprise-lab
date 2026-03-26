
# Active Directory Enterprise Lab Environment

## Overview

This project documents the deployment of a simulated enterprise Active Directory infrastructure using Windows Server and a Windows 10 client virtual machine inside VirtualBox.

The environment demonstrates:

- Domain Controller installation
- Forest creation (corp.local)
- Organizational Unit structure
- Security group-based RBAC
- DNS configuration and verification
- Client domain join
- Group Policy implementation
- Departmental file share segmentation
- NTFS permission enforcement
- Access-based resource visibility validation

This lab mirrors how organizations deploy centralized identity and access management systems in production environments.

---

# Environment Architecture

**Platform:** VirtualBox  
**Server:** Windows Server (Domain Controller)  
**Client:** Windows 10 Pro  
**Domain:** corp.local  
**Network Mode:** Host-only adapter  

---

# Step 1 — Virtual Machine Environment Setup

The infrastructure environment was built using Oracle VirtualBox with separate Server and Client virtual machines configured for domain communication.

![Virtual hardware setup](screenshots/Virtual hardware setup.png)

![VirtualBox overview Page](screenshots/VirtualBox overview Page.png)

---

# Step 2 — Windows Server Installation and Disk Configuration

Disk allocation and partitioning were configured prior to installing Windows Server.

![Disk allocation and partition](screenshots/Disk allocation and partition.png)

After installation, Server Manager confirmed successful deployment.

![Server Manager Dashboard](screenshots/Server Manager Dashboard.png)

---

# Step 3 — Installing Active Directory Domain Services

Active Directory Domain Services (AD DS) was installed through Server Manager.

![Add AD Roles and Features](screenshots/Add AD Roles and Features.png)

Prerequisite checks confirmed the system was ready for domain promotion.

![prerequisites check](screenshots/prerequisites check.png)

---

# Step 4 — Promoting Server to Domain Controller

The server was promoted to a Domain Controller and configured as the root of a new forest.

![promote to domain controller](screenshots/promote to domain controller.png)

A new forest root domain was created: corp.local

![adding a new forect with a root domain](screenshots/adding a new forect with a root domain.png)

Domain controller configuration options were verified during setup.

![Domain controller options](screenshots/Domain controller options.png)

Installation completed successfully with administrator role configured.

![domain installed and admin role](screenshots/domain installed and admin role.png)

---

# Step 5 — Verifying Domain Activation

The Active Directory domain environment was confirmed operational.

![domain active](screenshots/domain active.png)

![domain active 02](screenshots/domain active 02.png)

---

# Step 6 — Network Communication Between Server and Client

Connectivity between the domain controller and the client virtual machine was verified.

![Client Server communicating with Server VM](screenshots/Client Server communicating with Server VM.png)

The server also confirmed inbound communication from the client system.

![Server VM receiving network from Client VM](screenshots/Server VM receiving network from Client VM.png)

---

# Step 7 — Creating Organizational Units and Security Groups

Organizational Units were created for HR, IT, and Marketing departments to simulate enterprise identity segmentation.

Users were assigned to security groups within their respective OUs.

![adding a user to a group within its OU](screenshots/adding a user to a group within its OU.png)

---

# Step 8 — Joining the Client Machine to the Domain

The Windows client system was successfully joined to the domain environment.

![successfully added ClientVM to domain](screenshots/successfully added ClientVM to domain.png)

Domain authentication was verified using domain user accounts.

![User accounts successfully logged in on client VM](screenshots/User accounts successfully logged in on client VM.png)

---

# Step 9 — Implementing Group Policy Configuration

Group Policy settings were configured to allow domain user authentication and environment control.

![GPO allowing domain users log in](screenshots/GPO allowing domain users log in.png)

Group Policy configuration was verified through Group Policy Management.

![Group Policy Management Implemented](screenshots/Group Policy Management Implemented.png)

---

# Step 10 — Creating Departmental File Share Structure

A centralized departmental directory structure was created to simulate enterprise file server segmentation.
C:\TESTCompanyData
│
├── HR
├── IT
└── Marketing

![Test Company Data Folder created on Server](screenshots/Test Company Data Folder created on Server.png)

---

# Step 11 — Applying Role-Based Access Control Using Security Groups

Security group membership was used to enforce department-level file access permissions.

HR users were restricted to HR resources only.

![HR user being able to access only HR file as a result of share](screenshots/HR user being able to access only HR file as a result of share.png)

IT users were restricted to IT resources only.

![IT user being able to access only IT file as a result of share](screenshots/IT user being able to access only IT file as a result of share.png)

Marketing users were restricted to Marketing resources only.

![Marketing user being able to access only marketing file as a result of share](screenshots/Marketing user being able to access only marketing file as a result of share.png)

Access verification confirmed correct permission enforcement.

![TEST FILE being accessed on IT account with authorized group](screenshots/TEST FILE being accessed on IT account with authorized group.png)

---

# Final Environment Capabilities Demonstrated

This environment successfully implements:

- Domain controller deployment
- Forest creation (corp.local)
- OU segmentation by department
- Security group RBAC implementation
- Client domain authentication
- DNS-based communication between systems
- Group Policy configuration
- Departmental file server segmentation
- NTFS permission enforcement
- Access-based folder visibility validation

---

# Skills Demonstrated

This project demonstrates practical experience with:

- Active Directory Domain Services (AD DS)
- Domain Controller deployment
- DNS configuration
- Organizational Unit design
- Security group-based RBAC
- Group Policy Management
- Domain join troubleshooting
- NTFS permissions
- SMB share configuration
- Access-Based Enumeration
- Enterprise-style file server architecture
