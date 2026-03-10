### Golden Ticket Attack Demonstration – Active Directory Security Project

### Overview
This project expands on concepts introduced in cybersecurity labs by exploring the Kerberos Golden Ticket attack within a controlled Active Directory environment. The goal was to better understand how attackers can exploit weaknesses in Kerberos authentication after gaining privileged access to a domain controller.

Rather than stopping at the basic lab demonstration, this project involved further experimentation and analysis to understand how forged Kerberos tickets can be generated and used to access domain resources.

### Technologies Used
- Windows Server
- Active Directory Domain Services
- Kerberos Authentication
- Kali Linux
- Mimikatz
- Impacket
- Evil-WinRM
- Wireshark

### Environment
The project was conducted in a contained virtual lab environment consisting of a domain controller, domain-joined client machines, and an attacker system used to simulate post-exploitation scenarios. This environment allowed testing of Kerberos ticket manipulation and privilege escalation techniques in a safe and isolated network.

### Attack Concept
The Golden Ticket technique involves forging a Kerberos Ticket Granting Ticket (TGT) after obtaining the hash of the KRBTGT account. Because this account signs Kerberos tickets in Active Directory, a forged ticket can be trusted by the domain and used to impersonate privileged users.

This allows an attacker to authenticate as a domain administrator and access domain resources without needing the original credentials.

### Security Insights
Through this project, the focus was placed not only on how the attack works but also on the security implications and defensive considerations. Understanding how Golden Ticket attacks operate helps highlight the importance of protecting domain controller credentials and monitoring suspicious Kerberos activity.

### Defensive Considerations
- Protect domain controller access
- Monitor abnormal Kerberos authentication activity
- Rotate the KRBTGT account password during incident response
- Implement strong privileged access management

### Purpose
This project was conducted as a personal exploration of Active Directory security to deepen understanding of Kerberos authentication, identity security, and post-exploitation techniques used in enterprise environments.

### Gallery

<img width="1757" height="950" alt="image" src="https://github.com/user-attachments/assets/3fa17c03-afc1-4e23-b8fa-96a56adb613d" />
In this screenshot, the title slide of the Golden Ticket Attack project presentation is shown. The project focuses on understanding Kerberos ticket forgery within Active Directory and analyzing the security implications of compromised domain credentials.


<img width="1697" height="936" alt="image" src="https://github.com/user-attachments/assets/77a5351b-9b6b-4943-a611-755ed456f86e" />
In this screenshot, the concept of a Golden Ticket attack is explained. It shows how a forged Kerberos Ticket Granting Ticket (TGT) can be created using the KRBTGT account hash and domain SID to impersonate users within an Active Directory environment.


<img width="1712" height="966" alt="image" src="https://github.com/user-attachments/assets/841c3ce3-0cc8-486d-8766-e9908ae50136" />
In this screenshot, the process of a Golden Ticket attack is outlined. It shows how an attacker with elevated privileges can obtain the KRBTGT account hash and domain SID, generate a forged Kerberos ticket, and use it to authenticate within the Active Directory domain.


<img width="1712" height="959" alt="image" src="https://github.com/user-attachments/assets/7ca4e392-9641-40ff-8487-338d5becc4f4" />
In this screenshot, potential uses of a Golden Ticket are illustrated. A forged Kerberos ticket can allow an attacker to impersonate privileged users, access domain resources, maintain persistence, and move laterally within an Active Directory environment.


<img width="1690" height="1127" alt="image" src="https://github.com/user-attachments/assets/ea01f1ad-1926-44f1-add8-b3f801950cc3" />
In this screenshot, a visual analogy explains the Golden Ticket attack. It illustrates how a forged Kerberos ticket signed by the KRBTGT account can be trusted by the domain controller, allowing an attacker to impersonate privileged users and gain access to protected domain resources.
