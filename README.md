# Windows Server  Lab

**Portfolio Priority: #1 — Core Windows **

A practical Windows Server  lab focused on **Active Directory, DNS, DHCP, Group Policy, file services, permissions, and troubleshooting**.

## Business Scenario

A small company with five departments:

- IT
- HR
- Finance
- Sales
- Management

The environment provides centralized identity, network services, endpoint policy, and department file access.

## Environment

| System | Role | IP |
|---|---|---|
| DC01 | AD DS / DNS / DHCP | 10.10.10.33 |
| FS01 | File Server / DFS Namespace | 10.10.10.28 |
| CLIENT01 | Domain-joined test system | 10.10.10.50 |

- Domain: `corp.contoso.local`
- NetBIOS: `CORP`
- Network: `10.10.10.0/24`
- Lab subnet: `10.10.10.0/26`
- Gateway: `10.10.10.1`

> CLIENT01 uses a Windows Server image as the test system for domain, DNS, GPO, and file-access validation.

## Architecture

<img width="1536" height="1024" alt="Windows Server infrastructure topology" src="https://github.com/user-attachments/assets/46a1c150-af91-4ca6-a8f0-023a2a674c15" />

```text
Active Directory
      |
   DNS / DHCP
      |
   Group Policy
      |
  Domain Clients
      |
  File Services
      |
 SMB / NTFS / DFS
```

## Tasks

| # | Task | Status |
|---:|---|:---:|
| 01 | [DC01 Preparation](documentation/01-dc01-preparation.md) | ✅ |
| 02 | [Domain Controller Promotion](documentation/02-domain-controller-promotion.md) | ✅ |
| 03 | [Active Directory](documentation/03-active-directory.md) | ✅ |
| 04 | [DNS](documentation/04-dns.md) | ✅ |
| 05 | [DHCP](documentation/05-dhcp.md) | ✅ |
| 06 | [Group Policy](documentation/06-group-policy.md) | ✅ |
| 07 | [File Server & Permissions](documentation/07-file-server-permissions.md) | ✅ |

Detailed implementation notes: [Documentation](documentation/).

## Core Skills Demonstrated

- Active Directory users, groups, OUs, computers, and domain membership
- DNS forward/reverse lookup and troubleshooting
- DHCP scopes, exclusions, reservations, and options
- Group Policy creation, linking, verification, and troubleshooting
- SMB file shares
- NTFS and share permissions
- Access-Based Enumeration
- DFS Namespace
- PowerShell-based verification
- Evidence-driven troubleshooting

## Troubleshooting Method

```text
Problem
   ↓
Evidence
   ↓
Hypothesis
   ↓
Test
   ↓
Fix
   ↓
Verify
```

Examples include DNS resolution, domain connectivity, GPO application, SMB access, and permission problems.

## Security

The lab applies:

- Group-based access control
- Least-privilege permissions
- Domain authentication
- NTFS + SMB permission separation
- Controlled network access

## Project Structure

```text
windows-server-infrastructure-lab/
├── README.md
└── documentation/
    ├── 01-dc01-preparation.md
    ├── 02-domain-controller-promotion.md
    ├── 03-active-directory.md
    ├── 04-dns.md
    ├── 05-dhcp.md
    ├── 06-group-policy.md
    └── 07-file-server-permissions.md
```

## Result

The lab demonstrates a small but realistic Windows domain environment covering:

**Identity → DNS/DHCP → Group Policy → File Services → Permissions → Verification → Troubleshooting**

