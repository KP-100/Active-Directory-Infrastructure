# Home Lab Active Directory Infrastructure Project

A self-directed home lab project simulating the IT infrastructure of a small business, built to practice Active Directory administration, group policy management, file permissions, and help desk ticket resolution.

## Overview

This lab replicates a small business network environment with a domain controller, file server, and client workstations. The goal was to hands-on practice the core responsibilities of a Windows sysadmin / help desk role: user provisioning, access control, policy enforcement, and day-to-day IT support tickets.

## Lab Environment

| Component | Details |
|---|---|
| Hypervisor | *VirtualBox* |
| Domain Controller | *Windows Server 2022* |
| Client Workstations | *2x Windows 11* |
| Users | 10 user accounts |
| Domain Name | *LAB.local* |

## Network / AD Topology

<img width="641" height="231" alt="ADTopology" src="https://github.com/user-attachments/assets/08ab82d5-26b0-4e5e-8c7e-2ef5a9a4520a" />


## What I Built

### 1. Active Directory Structure
- Created a domain and configured Organizational Units (OUs) by department to organize users, groups, and computers.
- Set up 10 user accounts with role-based group membership.
- Applied role-based access control across departmental resources.

<img width="1027" height="731" alt="image" src="https://github.com/user-attachments/assets/77d7d3fe-c1c4-4e16-8823-f5fbb22bb9bd" />


### 2. File Server & NTFS Permissions
- Configured a dedicated file server with shared folders for each department.
- Applied NTFS permissions so users could only access resources relevant to their department/role.
- Tested access boundaries by logging in as different users to confirm permission scoping worked as intended.

<img width="1024" height="731" alt="image" src="https://github.com/user-attachments/assets/53d740e8-4799-4745-adc2-cff0c04cc1bd" />


### 3. Group Policy Objects (GPOs)
- Enforced password complexity and account lockout policies via GPO.
- Deployed a shared network printer to client workstations using Group Policy Preferences, eliminating manual per-machine setup.

<img width="1028" height="727" alt="image" src="https://github.com/user-attachments/assets/3030c07d-76a4-4ac9-94cc-fdc9f8ac0028" />


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

