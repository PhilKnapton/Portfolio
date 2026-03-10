# Project Quantum – Always On VPN Proof of Concept

### Overview
Project Quantum was a proof of concept demonstrating a secure and redundant remote access solution for a fictional Calgary-based oil and gas company, White Hot Oil & Gas LLC. The goal was to allow remote employees to securely access internal resources from any location.

### Environment
The lab environment was built in VMware Workstation and consisted of:

- **Server 1:** Active Directory, DNS, DHCP, AD CS, NPS, DFS  
- **Server 2:** RRAS Always On VPN server with DFS replication  
- **Windows 11 Client:** Simulated remote employee device

### Key Features
- Always On VPN using **IKEv2 device tunnel**
- **Certificate-based authentication**
- Automatic VPN connection **before user logon**
- **DFS namespace and replication** for redundant file storage
- Centralized authentication using **Network Policy Server (RADIUS)**

### Demonstration
The client device automatically established a secure VPN connection when outside the internal network. Once connected, the user could authenticate with Active Directory and access shared files through the DFS namespace.

### Technologies Used
- Windows Server 2022  
- Windows 11 Enterprise  
- VMware Workstation Pro  
- RRAS / Always On VPN  
- Active Directory  
- AD CS (Certificate Services)  
- Network Policy Server  
- Distributed File System (DFS)
- Group Policy (GPO) Auto-Enroll

<img width="1928" height="1085" alt="image" src="https://github.com/user-attachments/assets/1ed3e793-6708-4c1c-a5f2-55420f2dbc58" />

In this screenshot, the network topology for Project Quantum is shown. It illustrates how a remote Windows 11 client automatically connects to the internal network using an Always On VPN (IKEv2 device tunnel) with certificate-based authentication. The environment includes a Windows Server 2022 Domain Controller (AD DS, DNS, DHCP, AD CS, NPS) and a RRAS VPN server, along with DFS replication for redundant file sharing.
