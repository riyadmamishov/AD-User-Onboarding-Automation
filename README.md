# AD User Onboarding Automation - PowerShell Lab

> Automated 30 minutes of manual HR onboarding work into 30 seconds.

This lab automates bulk creation of 10 Active Directory users using PowerShell. Real-world scenario: HR sends an Excel file, the script creates all users automatically.

### 🎯 The Problem
- Creating users manually in ADUC is time-consuming
- Typing errors in SamAccountName / UPN
- Same OU and password policy repeated for every user

### ✅ The Solution
With PowerShell:
- 10 users created with 1 command
- All users placed in `OU=Users,DC=company,DC=local`
- Default password: `P@ssw0rd2024!` + force change at next logon
- Green confirmation output in console
- <img width="1600" height="1066" alt="NewUsers" src="https://github.com/user-attachments/assets/9b43cc15-0f1f-4ef3-b2b8-4ae504b01cd9" />


### 🛠️ Tech Stack
- Windows Server 2022
- Active Directory PowerShell Module
- `New-ADUser`, `ConvertTo-SecureString`, `Import-Csv`

### 📸 Lab Results

**1. PowerShell Execution:**
![PowerShell Execution](./01-powershell2.png)

**2. Verification in ADUC:**
![ADUC Verification](./ADUC.png)

### 🚀 How to Run

1. Import AD module:
```powershell
Import-Module ActiveDirectory
