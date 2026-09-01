# Home Lab Active Directory Infrastructure Project

A self-directed home lab project simulating the IT infrastructure of a small business, built to practice Active Directory administration, group policy management, file permissions, and help desk ticket resolution.

## Overview

This lab replicates a small business network environment with a domain controller, file server, and client workstations. The goal was to hands-on practice the core responsibilities of a Windows sysadmin / help desk role: user provisioning, access control, policy enforcement, and day-to-day IT support tickets.

## Lab Environment

| Component | Details |
|---|---|
| Hypervisor | *(e.g., VMware Workstation / VirtualBox / Hyper-V)* |
| Domain Controller | *(e.g., Windows Server 2022)* |
| Client Workstations | 2x *(e.g., Windows 10/11)* |
| Users | 10 user accounts |
| Domain Name | *(e.g., corp.local)* |

## Network / AD Topology

*(Insert a simple diagram here — draw.io, Lucidchart, or even a screenshot of your AD topology export. Something like: DC → File Server → Workstation 1, Workstation 2)*

![Topology Diagram](./screenshots/topology.png)

## What I Built

### 1. Active Directory Structure
- Created a domain and configured Organizational Units (OUs) by department to organize users, groups, and computers.
- Set up 10 user accounts with role-based group membership.
- Applied role-based access control across departmental resources.

![OU Structure](./screenshots/ou-structure.png)

### 2. File Server & NTFS Permissions
- Configured a dedicated file server with shared folders for each department.
- Applied NTFS permissions so users could only access resources relevant to their department/role.
- Tested access boundaries by logging in as different users to confirm permission scoping worked as intended.

![NTFS Permissions](./screenshots/ntfs-permissions.png)

### 3. Group Policy Objects (GPOs)
- Enforced password complexity and account lockout policies via GPO.
- Deployed a shared network printer to client workstations using Group Policy Preferences, eliminating manual per-machine setup.

![GPO Settings](./screenshots/gpo-settings.png)

### 4. Simulated Help Desk Tickets
Practiced common day-1 sysadmin/help desk tasks, treating each as a "ticket" with documented resolution steps:

| Ticket | Resolution Summary |
|---|---|
| New user account request | Created user in appropriate OU, assigned to correct security group, set initial password with forced reset on first login |
| Account disable (offboarding) | Disabled account, removed group memberships, documented reason and date |
| Password reset | Reset password via ADUC, enforced "change password at next logon" |

## Skills Demonstrated

- Active Directory Domain Services (AD DS)
- Group Policy Management (GPMC)
- NTFS permissions & departmental access control
- User lifecycle management (onboarding/offboarding)
- Help desk ticket documentation & resolution
- Windows Server administration

## Lessons Learned

*(A few sentences on what surprised you, what you'd do differently, or what you want to explore next — e.g., adding DNS/DHCP, setting up a second DC for redundancy, scripting user creation with PowerShell instead of doing it manually.)*

## Next Steps

- [ ] Automate user provisioning with PowerShell scripts
- [ ] Add a second domain controller for redundancy
- [ ] Configure DHCP/DNS from scratch
- [ ] Document with more detailed screenshots / video walkthrough
