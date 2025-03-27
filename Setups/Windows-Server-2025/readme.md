# Windows Server 2025 Setup
> Windows Server 2025 for this project is serving as the Domain Controller. All of the workstations will connect to this machine for authentication and authorization of each host, as well as provide users for the workstations. This server will have DNS and DHCP enabled.
>
> ***PREREQUISITES:***
> 1) VirtualBox installed
> 2) Virtual machine with Windows Server 2025 ISO has been configured and provisioned

## Table of Contents

* Network Topology
* Setup Windows Server 2025
  - Disable Default Logoff
  - Disable CTRL + ALT + DEL
* Assign Static IP Address
* Promote Active Directory to a Domain Controller
* Setup DNS
* Setup DHCP
* Add User Accounts in Active Directory

***

# Network Topology

[PLACE PHOTO PATH HERE]: #

# Setup Windows Server 2025

#### Step 1: Go through all of the defaults until you get to the "Select Image" box >>> Select "Desktop Experience" >>> Accept Microsoft's EULA

#### Step 2: Select "Disk 0 Unallocated Space" >>> "Create Partition" >>> Use the default "Size in MB" >>> Apply

#### Step 3: Select Disk 0 Partition 3 >>> Install

#### Step 4: Set a password for the default Administrator account

#### Step 5: Once the login screen appears, navigate to the top bar >>> Input >>> Keyboard >>> "Insert Ctrl-Alt-Del" >>> After login, select "Required Only"

## *Disable Default Logoff*

#### Step 1: Settings >>> System >>> Power >>> "Screen timeout" >>> "Never"

## *Disable CTRL + ALT + DEL*

#### Step 1: On the machine, search "Local Security Policy" >>> Navigate to "Security Options" >>> Scroll down and find "Interactive logon: Do not require CTRL+ALT+DEL" >>> Enable >>> Apply >>> OK

# Assign Static IP Address

#### Step 1: Navigate to the Control Panel (Windows + X) >>> "Network and Internet" >>> "Network and Sharing Center" >>> "Change adapter settings" >>> Right-click "Ethernet", click "Properties" >>> Select "Internet Protocol Version 4 (TCP/IPv4)" >>> Properties

#### Step 2: Set the static IP address of for the machine. Select "OK" when finshed. Refer to Project Overview for more information

# Promote Active Directory to a Domain Controller

#### Step 1: Back on the "Server Manager" window, select "Add roles and features"

#### Step 2: Select "Next" until the "Select server roles" window appears >>> Select "Active Directory Domain Services", "DHCP Server", "DNS Server", "File and Storage Services" and "Web Server (IIS)" >>> Leave all of the defaults >>> Select "Next" until the Confirmation tab >>> Install

#### Step 3: Once the installation is done, a notification will pop up. Select "More"

#### Step 4: Select "Promote this erver to a domain" >>> Select "Add a new forest" >>> Enter a root domain name. For this project, it will be *corp.lab-dc.com*

#### Step 5: Leave default options. For DSRM password, use the Administrator password >>> Next >>> Leave "Create DNS delegation" blank >>> CLick "Next" until the "Prerequisites Check" menu appears >>> Click "Install" when the checks are finished

#### Step 6: Restart the machine. After logging in, verify the server is apart of the domain by typing the following command into Powershell:
```bash
Get-ADDomainController
```


