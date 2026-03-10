### Project Pegasus – Datacenter Resiliency with VMware Site Recovery Manager

### Overview
Project Pegasus demonstrates a disaster recovery (DR) strategy using VMware vSphere Replication and Site Recovery Manager (SRM). The project was designed to simulate an enterprise datacenter failover scenario with a 1-hour Recovery Point Objective (RPO). The environment consists of a physical ESXi host representing the primary site (PHOENIX) and a virtual ESXi environment running in VMware Workstation representing the recovery site (LIVERPOOL).

### Technologies Used
- VMware ESXi
- VMware vCenter Server Appliance (vCSA)
- VMware vSphere Replication
- VMware Site Recovery Manager (SRM)
- VMware Workstation
- Windows Server
- DNS Services

### Architecture
The disaster recovery environment consists of two sites:

**Primary Site – PHOENIX**
- Physical ESXi host
- vCenter Server Appliance
- vSphere Replication Appliance
- VMware SRM Appliance
- Windows DNS Server
- Windows File Server (protected workload)

**Recovery Site – LIVERPOOL**
- Nested ESXi host running in VMware Workstation
- vCenter Server Appliance
- vSphere Replication Appliance
- VMware SRM Appliance
- Windows DNS Server
- Placeholder VM for automated failover

### Disaster Recovery Strategy
The Windows File Server VM hosted at the PHOENIX site is replicated to the LIVERPOOL site using VMware vSphere Replication. Site Recovery Manager is used to coordinate disaster recovery operations by creating Protection Groups and Recovery Plans. These plans define the sequence of operations required to perform failover and failback between sites.

### Failover and Recovery Testing
Multiple disaster recovery scenarios were tested:

- Test failover using SRM recovery plans
- Live failover of the File Server VM from PHOENIX to LIVERPOOL
- Verification of file share accessibility during failover
- Failback of the File Server VM to the primary site
- Re-protection of the VM after failback

These tests confirmed that the replication and recovery process functioned correctly and that services remained accessible during the recovery process.

### Skills Demonstrated
- Disaster recovery architecture design
- VMware vSphere Replication configuration
- VMware Site Recovery Manager deployment
- Protection groups and recovery plan configuration
- Cross-site DNS configuration
- Failover and failback testing
- Enterprise infrastructure documentation

### Network Diagram

<img width="816" height="599" alt="image" src="https://github.com/user-attachments/assets/ee3ae5be-a03d-451b-9f42-e6b0c033ddd3" />

In this screenshot, the disaster recovery architecture for Project Pegasus is shown. The diagram illustrates the primary site (PHOENIX) running on a physical ESXi host and the recovery site (LIVERPOOL) running as a nested ESXi host in VMware Workstation. Both sites include vCenter Server, vSphere Replication, Site Recovery Manager, and DNS services. The Windows File Server VM at the primary site is replicated to the recovery site using vSphere Replication, allowing Site Recovery Manager to coordinate failover and failback operations between the two datacenters.
