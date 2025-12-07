# Active Directory Domain Services (AD DS) Setup on AWS EC2

## Overview
This lab shows how to install Active Directory Domain Services (AD DS) and promote a Windows Server EC2 instance to a Domain Controller.

Estimated time: 20–30 minutes  
Recommendation: Take a snapshot or create an AMI before major changes.

## Prerequisites
- A running Windows Server EC2 instance with Administrator access (RDP)
- Security group allowing RDP (TCP 3389) from your IP
- Administrative credentials for the Windows Server

---

## Steps

1. Access the server
   - Connect to the EC2 instance via RDP and sign in as Administrator.
   - Open **Server Manager** from the Start menu.

   <img width="1720" height="800" alt="Server Manager screenshot" src="https://github.com/user-attachments/assets/be7ef4a9-6458-43e8-8b5a-fd37a93303e7" />

2. Add the AD DS role
   - In Server Manager: **Manage → Add Roles and Features**.
   - Select **Active Directory Domain Services** and proceed through the wizard to install the role.

   <img width="1720" height="800" alt="Add Roles and Features screenshot" src="https://github.com/user-attachments/assets/1e6006d1-cca0-4cf1-9481-3f530ad8cdb1" />

3. Promote the server to a Domain Controller
   - After installation completes, choose the notification flag in Server Manager and select **Promote this server to a domain controller**.
   - Configure:
     - Deployment operation: Add a new forest (or join an existing domain as appropriate)
     - Root domain name: e.g., example.local
     - DSRM password and other required settings
   - Review options and complete the promotion.

   <img width="700" height="600" alt="Promotion to Domain Controller screenshot" src="https://github.com/user-attachments/assets/d8b1cbe3-b7a2-41d8-a793-ec426254b3e0" />

4. Reboot and finalize
   - The server will automatically restart to apply AD DS configuration.
   - After reboot, sign in using the domain Administrator account and verify AD services.

   <img width="2777" height="1599" alt="Restart screenshot 1" src="https://github.com/user-attachments/assets/5157d7e0-dc1d-47f7-861b-8b51e65c2a20" />
   <img width="2849" height="1463" alt="Restart screenshot 2" src="https://github.com/user-attachments/assets/ac856a5e-f317-4765-bc86-1c8328862930" />

---

## Verification
- Open **Active Directory Users and Computers** to confirm the domain is present and functional.
- Check Event Viewer for AD DS or replication errors.
- Confirm DNS entries (forward lookup zones) were created for the domain controller.

---

## Result
The EC2 Windows Server was successfully configured with AD DS and promoted to a Domain Controller. The system restarted as part of the process.

```
