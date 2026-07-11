# Windows 11 Domain Join

## Project Overview

This project demonstrates how to join a Windows 11 Pro workstation to a Windows Server 2022 Active Directory domain.

Joining computers to a domain is a common responsibility for Help Desk and Desktop Support technicians during new computer deployments, workstation replacements, and employee onboarding.

---

# Lab Environment

<img width="1917" height="1197" alt="active directory vmware" src="https://github.com/user-attachments/assets/3dfc9cd2-e435-4f36-81f9-624c15d89a5e" />
<img width="1917" height="1197" alt="active directory pic" src="https://github.com/user-attachments/assets/371972f3-c27f-463a-93a8-6a52f9356ea4" />



|-----------|---------|
| Hypervisor | VMware Workstation |
| Domain Controller | Windows Server 2022 |
| Client Operating System | Windows 11 Pro |
| Domain | homelab.local |
| Server Name | DC01 |
| Client Name | CLIENT01 |

---

# Objectives

- Configure Windows 11 network settings
- Configure DNS
- Verify communication with the Domain Controller
- Join a Windows 11 workstation to an Active Directory domain
- Verify successful domain authentication
- Confirm the computer object appears in Active Directory

---

# Step 1 – Verify Network Connectivity

Opened Command Prompt and verified the Windows 11 network configuration.

Commands used:

```cmd
ipconfig /all
ping 192.168.170.10
```

Verified successful communication with the Domain Controller.

---

# Step 2 – Configure DNS

Configured the Windows 11 client to use the Domain Controller as its Preferred DNS Server.

DNS Server:

```
192.168.170.10
```

This allows the workstation to locate Active Directory services.

---

# Step 3 – Verify DNS Resolution

Verified DNS functionality before joining the domain.

Commands used:

```cmd
nslookup homelab.local
nslookup dc01.homelab.local
```

Confirmed the client could successfully resolve the domain and Domain Controller.

---

# Step 4 – Join the Active Directory Domain

Opened the System Properties window and joined the Windows 11 workstation to the Active Directory domain.

Domain:

```
homelab.local
```

Authenticated using the Domain Administrator account.

Restarted the workstation to complete the domain join process.

---

# Step 5 – Verify Domain Authentication

Logged into Windows using an Active Directory domain user account.

Verified successful authentication and access to the domain environment.

---

# Step 6 – Verify Computer Object

Opened Active Directory Users and Computers on the Domain Controller.

Confirmed the Windows 11 workstation (CLIENT01) successfully appeared as a computer object within the domain.

---

# Troubleshooting

## Issue

The Windows 11 workstation initially could not locate the Domain Controller during the domain join process.

## Investigation

Verified:

- Network connectivity
- IP configuration
- DNS configuration
- Domain name
- Domain Administrator credentials

## Resolution

Configured the Windows 11 workstation to use the Domain Controller as its Preferred DNS Server.

Verified successful DNS resolution using:

```cmd
nslookup
```

Successfully joined the workstation to the Active Directory domain.

---

# Skills Demonstrated

- Windows 11 Administration
- Active Directory Domain Join
- Windows Server Administration
- DNS Configuration
- Network Troubleshooting
- Domain Authentication
- Command Prompt Diagnostics
- VMware Workstation
- Help Desk Support

---

# Commands Used

```cmd
ipconfig /all
ping
nslookup
hostname
whoami
```

---

# What I Learned

This project provided hands-on experience joining a Windows 11 workstation to an Active Directory domain and troubleshooting connectivity issues during the deployment process. I learned how DNS enables client computers to locate a Domain Controller, verified communication using networking tools, authenticated with domain credentials, and confirmed the workstation was successfully added to Active Directory. These tasks reflect common responsibilities performed by Help Desk and Desktop Support technicians during workstation deployments and user onboarding.
<img width="1917" height="1197" alt="active directory vmware" src="https://github.com/user-attachments/assets/32571a5d-d37b-4ca3-a5b9-f670cf590559" />

