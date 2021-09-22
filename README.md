# HelpDesk-Dashboard
This project is based on fascination of tool LazyWinAdmin_GUI (currently open source project) created by [François-Xavier Cat](https://lazywinadmin.com/)

# If you want to know how looks LazyWinAdmin_GUI 
Here is link:
https://github.com/lazywinadmin/LazyWinAdmin_GUI

Original look:
![LazyWinAdmin_GUI](https://github.com/lazywinadmin/LazyWinAdmin_GUI/blob/master/Media/lwa-v0.4-main01.png)

# Current look:
One of the main feature of this tool is it has many combined scripts together at one place. It also uses two tabs (User Management and Device Managment). 

User Management was designed to conduct task in Active Directory 
![User Management View](https://user-images.githubusercontent.com/72066881/134351393-47224460-364c-4266-b4b7-de342adbd176.png)

Device Management was designed to conduct tasks on workstations, servers, laptops. 
![Device Management View](https://user-images.githubusercontent.com/72066881/134351903-2bd676ed-528b-4519-b370-644954a211a7.png)

# I need to refactor and clean code before publish.

# Requirements 

1. PowerShell 5.1
2. Modules: 
   - ActiveDirectory
   -  Microsoft.PowerShell.Management
   -  ImportExcel
3. External Tools: 
   - Psexec (Psexec64.exe)
   - Account Lockout Status (LockoutStatus.exe)
   - SolarWinds DameWare Mini Remote Control x64 (dwrcc.exe)

```
#Requires -Modules @{ ModuleName="ActiveDirectory"; ModuleVersion="1.0.0.0" }
#Requires -Modules @{ ModuleName="ImportExcel"; ModuleVersion="1.0.0.0" }
#Requires -Modules @{ ModuleName="Microsoft.PowerShell.Management"; ModuleVersion="1.0.0.0" }

```
Import Assemblies
```
Import-Module PrintManagement
Import-Module Microsoft.PowerShell.Management
Import-Module ActiveDirectory
Import-Module ImportExcel
[void] [System.Reflection.Assembly]::LoadWithPartialName("System.Drawing") 
[void] [System.Reflection.Assembly]::LoadWithPartialName("System.Windows.Forms")
[void] [System.Reflection.Assembly]::LoadWithPartialName("System.DirectoryServices")
[void] [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.VisualBasic")
[void][Reflection.Assembly]::Load("System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089")
[void][Reflection.Assembly]::Load("System.Windows.Forms, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089")
[void][Reflection.Assembly]::Load("System.Drawing, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a")
[void][Reflection.Assembly]::Load("mscorlib, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089")
[void][Reflection.Assembly]::Load("System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089")
[System.Windows.Forms.Application]::EnableVisualStyles()
```

# Roadmap 

- [ ] Refactor and clear code    **[whole code]**
- [ ] Test one more time every feature     **[whole code]**
- [ ] Add jobs and runspaces to make tool more realiable and convient    **[whole code]**
- [ ] Fix paths to certain external tools and scripts    **[whole code]**
- [ ] Update requirements    **[readme]**
- [ ] Apply some leak memory preventing mechanim   **[whole code]**
- [ ] Add new tab for multi Servers/Workstation  management **[Server Managment Tab]**
- [ ] Add AD group management tools (assignment)   **[User Management Tab]**
- [ ] Change photo in AD button    **[User Management Tab]**   
- [ ] Scan for Updates on certain device    **[Device Management Tab]**

