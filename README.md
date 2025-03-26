# Table of Contents

* Project Overview
  - Network Design Map
  - Computer Specs
  - Downloads
    - Hypervisor
    - ISO Images
  - NAT Netowrk
  - Hosts
  - Accounts & Passwords
  - Virtual Machines
  - Tools

***

# Project Overview :briefcase:

## Network Design Map

## Computer Specs
*   **CPU**: Intel(R) Core(TM) i7-9750H CPU @ 2.60GHz   2.59 GHz
*   **RAM**: 16.0 GB (15.9 GB usable)
*   **GPU**: NVIDIA GeForce GTX 1660 Ti

## Downloads

### *Hypervisor*
* VirtualBox _7.1.6_

### *ISO Images*
* Kali Linux 2024
* Windows Server 2025
* Windows 11 Enterprise
* Ubuntu Live Server _22.04.5_
* Ubuntu Desktop _22.04.5_
* SecurityOnion _2.4.110_

## NAT Network

*** **Name:** lab-network
* **IP Address Range:** 10.0.0.0/24
  - **Usable Range:** 10.0.0.1 - 10.0.0.254
  - **DHCP Dynamic Scope:** 10.0.0.100 - 10.0.0.200

## Host

| **Hostname [lab-...]** | **IP Address**          | **Function**                       |
|------------------------|-------------------------|------------------------------------|
| dc (corp.lab-dc.com)   | 10.0.0.5                | Domain Controller (DNS, DHCP, SSO) |
| email-svr              | 10.0.0.8                | SMTP Relay Server                  |
| sec-box                | 10.0.0.10               | Dedicated Security Server          |
| sec-work               | 10.0.0.103 or (dynamic) | Security Playground                |
| win-client             | 10.0.0.100 or (dynamic) | Windows Workstation                |
| linux-client           | 10.0.0.101 or (dynamic) | Linux Desktop Workstation          |
| attacker               | dynamic                 | Attacker Environment               |

## Accounts & Passwords

| **Account**             | **Password**    | **Host**         |
|-------------------------|-----------------|------------------|
| Administrator           | boomersooner25! | ...-dc           |
| johnd@corp.lab-dc.com   | password123!    | ...-win-client   |
| janed@linux-client      | password123!    | ...-linux-client |
| lab-sec-work            | password123!    | ...-sec-work     |
| sec-work@sec-box        | password123!    | ...-sec-box      |
| email-svr@lab-email-svr | password123!    | ...-email-svr    |
| attacker@attacker       | attacker        | attacker         |

## Virtual Machines

| **VM Name**        | **Operating System**  | **Specs**       | Storage (Minimum) |
|--------------------|-----------------------|-----------------|-------------------|
| [lab-dc]           | Windows Server 2025   | 2 CPU / 4096 MB |50 GBs             |
| [lab-win-client]   | Windows 11 Enterprise | 2 CPU / 4096 MB |80 GBs             |
| [lab-linux-client] | Ubuntu 22.04 Desktop  | 1 CPU / 2048 MB |80 GBs             |
| [lab-sec-work]     | Security Onion        | 1 CPU / 2048 MB |55 GBs             |
| [lab-sec-box]      | Ubuntu 22.04 Desktop  | 2 CPU / 4096 MB |80 GBs             |
| [lab-email-svr]    | Ubuntu Server 22.04   | 1 CPU / 2048 MB |25 GBs             |
| [attacker]         | Kali Linux 2024       | 1 CPU / 2048 MB |55 GBs             |

## Tools

### *Enterprise Tools + Defense*

* **Microsoft Active Directory:** A centralized directory service that manages users, devices, and permissions in a Windows domain environment
* **Wazuh:** An open-source security platform for threat detection, incident response, and compliance monitoring
* **Postfix:** A mail transfer agent (MTA) used to route and deliver email securely in Unix-based systems

### Offense

* **Evil-WinRM:** A post-exploitation tool that allows remote command execution on Windows systems using WinRM
* **Hydra:** A fast and flexible password-cracking tool that supports numerous authentication protocols
* **SecLists:** A comprehensive collection of security-related wordlists used for reconnaissance, brute-force attacks, and pentesting
* **NetExec:** A remote command execution tool for managing Windows machines across a network
* **XFreeRDP:** An open-source implementation of the Remote Desktop Protocol (RDP) for accessing Windows systems remotely
