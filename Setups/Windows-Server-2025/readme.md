# Windows Server 2025 Setup
> Windows Server 2025 for this project is serving as the Domain Controller. All of the workstations will connect to this machine for authentication and authorization of each host, as well as provide users for the workstations. This server will have DNS and DHCP enabled.
>
> ***PREREQUISITES:***
> 1) VirtualBox installed
> 2) Virtual machine with Windows Server 2025 ISO has been configured and provisioned

## Table of Contents

* Setup Windows Server 2025
  - Disable Default Logoff
  - Disable CTRL + ALT + DEL
* Assign Static IP Address
* Promote Active Directory to a Domain Controller
* Setup DNS
* Setup DHCP
* Add User Accounts in Active Directory
