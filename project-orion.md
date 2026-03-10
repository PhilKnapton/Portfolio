### Project Orion – VMware Datacenter Design

### Overview
Project Orion demonstrates the design of a resilient VMware vSphere environment showcasing core datacenter availability features such as vMotion, High Availability (HA), Fault Tolerance (FT), and Distributed Resource Scheduler (DRS). The lab environment uses shared iSCSI storage to enable live migration and redundancy across multiple ESXi hosts.

### Technologies Used
- VMware ESXi  
- VMware vCenter Server Appliance (vCSA)  
- VMware Workstation  
- FreeNAS / TrueNAS  
- iSCSI Storage  
- Windows Server (Domain Controller)  
- Windows 10 Client  
- Linux Test VM  

### Architecture
The environment consists of two ESXi hosts managed by a vCenter Server and connected to a shared iSCSI datastore provided by a FreeNAS server. This shared storage allows virtual machines to migrate between hosts and enables high availability features within the cluster.

### Resiliency Features Demonstrated
- **vMotion** – Live migration of running VMs between ESXi hosts  
- **Storage vMotion** – Migration of VM storage between datastores  
- **High Availability (HA)** – Automatic restart of VMs during host failure  
- **Fault Tolerance (FT)** – Continuous availability through secondary VM replication  
- **Distributed Resource Scheduler (DRS)** – Load balancing across hosts  

### Skills Demonstrated
- VMware datacenter architecture design  
- Shared storage configuration (iSCSI)  
- High availability and redundancy planning  
- Virtual infrastructure management

### Network Diagram

<img width="1334" height="1657" alt="image" src="https://github.com/user-attachments/assets/1f248967-0eda-44b3-8399-30e17c091fb2" />

In this screenshot, the network architecture for Project Orion is shown. The diagram illustrates a VMware vSphere environment consisting of two ESXi hosts managed by a centralized vCenter Server Appliance. Shared iSCSI storage is provided by a FreeNAS server, allowing virtual machines to reside on shared datastores accessible by both hosts. Separate network segments are configured for management, iSCSI storage, vMotion, and internal VM traffic. This architecture enables core vSphere resiliency features such as vMotion, High Availability (HA), Fault Tolerance (FT), and Distributed Resource Scheduler (DRS).
