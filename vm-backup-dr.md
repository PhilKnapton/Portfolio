### Project Scapegoat – VM Backup & Disaster Recovery

### Overview
Project Scapegoat demonstrates a virtual machine backup and recovery solution using VMware Workstation and TrueNAS storage. The objective was to design a reliable backup workflow capable of protecting virtual machines and restoring them after deletion or failure.

### Technologies Used
- VMware Workstation Pro  
- TrueNAS / FreeNAS  
- iSCSI storage  
- Backup software (Vimalin / Veeam Community Edition)  
- Windows host system  

### Architecture
In this setup, VMware Workstation virtual machines are backed up to a TrueNAS storage volume hosted on shared infrastructure. The NAS system acts as the centralized backup repository where VM backups are stored and maintained.

### Storage Configuration
- TrueNAS virtual machine deployed on shared infrastructure  
- 10 GB disk allocated for the TrueNAS operating system  
- 500 GB storage volume created for backup data  
- Storage configured as a backup repository accessible from the host system  

### Backup Process
- Backup software installed on the VMware Workstation host  
- TrueNAS storage configured as the backup destination  
- Virtual machines backed up to the NAS repository  
- Multiple backup copies retained for recovery purposes  

### Disaster Recovery Test
To verify the reliability of the backup system, a virtual machine was intentionally deleted and then restored from the backup repository. The restored VM successfully booted and resumed normal operation, confirming that the backup and recovery process functioned correctly.

### Skills Demonstrated
- Virtual machine backup strategy  
- Network-attached storage configuration  
- Backup repository management  
- Disaster recovery testing  
- Infrastructure documentation

### Network Diagram

<img width="1407" height="2037" alt="image" src="https://github.com/user-attachments/assets/96e3268d-15f8-41f4-9854-ab28bd7aaded" />

In this screenshot, the network architecture for Project Scapegoat is shown. The diagram illustrates the VMware Workstation environment running on a Windows host, multiple virtual machines connected through NAT, Host-Only, and Bridged virtual switches, and a TrueNAS/FreeNAS storage system used as the backup repository. VM backups are performed from the host system to the FreeNAS iSCSI storage to support backup verification and recovery testing.
