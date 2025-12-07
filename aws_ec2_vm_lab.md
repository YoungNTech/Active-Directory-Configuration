
# Active Directory Domain Services Configuration Setup

## Lab Overview
This lab demonstrates the setup and configuration of Windows Active Directory Domain Services (AD DS) on an AWS EC2 virtual machine running Windows Server.

## Steps Performed

1. **Accessed Windows Server Manager**
   - Logged into the AWS EC2 instance running Windows Server.
   - Opened **Server Manager** from the Start Menu.
   - 
<img width="1720" height="800" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/be7ef4a9-6458-43e8-8b5a-fd37a93303e7" />



2. **Configured Active Directory Domain Services (AD DS)**
   - Selected **Manage → Add Roles and Features**.
   - Chose **Active Directory Domain Services** as the role to install.
   - Completed the setup wizard and began the installation process.

  <img width="1720" height="800" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/1e6006d1-cca0-4cf1-9481-3f530ad8cdb1" />


3. **Installed AD DS and Promoted the Server to a Domain Controller**
   - After installation, promoted the server to a **Domain Controller**.
   - Configured the domain name and administrative credentials.
<img width="700" height="600" alt="Screenshot 2025-12-04 235145" src="https://github.com/user-attachments/assets/d8b1cbe3-b7a2-41d8-a793-ec426254b3e0" />



4. **Automatic System Restart**
   - The VM automatically shut down and restarted to apply configuration changes.
   - 
<img width="2777" height="1599" alt="Screenshot 2025-12-05 000128" src="https://github.com/user-attachments/assets/5157d7e0-dc1d-47f7-861b-8b51e65c2a20" />
<img width="2849" height="1463" alt="Screenshot 2025-12-05 000201" src="https://github.com/user-attachments/assets/ac856a5e-f317-4765-bc86-1c8328862930" />


## Result
The EC2 Windows Server instance was successfully configured with Active Directory Domain Services and restarted as part of the setup process.

## Notes
- Ensure that necessary inbound security group rules (e.g., RDP 3389) are configured for administrative access.
- Always take a snapshot or AMI backup before major configuration changes.
