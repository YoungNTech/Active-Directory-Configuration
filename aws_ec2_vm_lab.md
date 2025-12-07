## Watch me do the lab HERE
https://www.loom.com/share/0c421230e9394dbeb698c7a4f2fd23ea


# Active Directory Domain Services Configuration Setup

## Lab Overview
This lab demonstrates the setup and configuration of Windows Active Directory Domain Services (AD DS) on an AWS EC2 virtual machine running Windows Server.

## Steps Performed

1. **Accessed Windows Server Manager**
   - Logged into the AWS EC2 instance running Windows Server.
   - Opened **Server Manager** from the Start Menu.
<img width="1302" height="840" alt="image" src="https://github.com/user-attachments/assets/4a336c1e-5b52-4d10-a843-44a349fed0d8" />


2. **Configured Active Directory Domain Services (AD DS)**
   - Selected **Manage → Add Roles and Features**.
   - Chose **Active Directory Domain Services** as the role to install.
   - Completed the setup wizard and began the installation process.
 <img width="784" height="556" alt="image" src="https://github.com/user-attachments/assets/e6f708af-38ad-4d4c-a86a-b804446815e1" />
  

3. **Installed AD DS and Promoted the Server to a Domain Controller**
   - After installation, promoted the server to a **Domain Controller**.
   - Configured the domain name and administrative credentials.
<img width="336" height="267" alt="image" src="https://github.com/user-attachments/assets/2023e4fc-7a72-42b6-9ceb-f753faa962dd" />
<img width="1150" height="542" alt="image" src="https://github.com/user-attachments/assets/eae66df9-6366-4a14-9ebc-f06eb731dde0" />


4. **Automatic System Restart**
   - The VM automatically shut down and restarted to apply configuration changes.

## Result
The EC2 Windows Server instance was successfully configured with Active Directory Domain Services and restarted as part of the setup process.

## Notes
- Ensure that necessary inbound security group rules (e.g., RDP 3389) are configured for administrative access.
- Always take a snapshot or AMI backup before major configuration changes.
