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

#### Step 1: Go through all of the defaults until you get to the "Select Image" box > Select "Desktop Experience" > Accept Microsoft's EULA

#### Step 2: Select "Disk 0 Unallocated Space" > "Create Partition" > Use the default "Size in MB" > Apply

#### Step 3: Select Disk 0 Partition 3 > Install

#### Step 4: Set a password for the default Administrator account

#### Step 5: Once the login screen appears, navigate to the top bar > Input > Keyboard > "Insert Ctrl-Alt-Del" > After login, select "Required Only"

## *Disable Default Logoff*

#### Step 1: Settings > System > Power > "Screen timeout" > "Never"

## *Disable CTRL + ALT + DEL*

#### Step 1: On the machine, search "Local Security Policy" > Navigate to "Security Options" > Scroll down and find "Interactive logon: Do not require CTRL+ALT+DEL" > Enable > Apply > OK

# Assign Static IP Address

#### Step 1: 
