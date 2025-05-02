<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- (Adding video soon)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create a Domain Controller and Install Active Directory
- Create a Domain Admin user within the domain
- Add a client computer to your domain
- Set up remote desktop for non-admin users on Client computer

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  - Created Resource Group in Azure, Virtual Network, Subnet, and DC (Domain Controller).
  
  - Set up a Client VM and title it Client-1, attaching it to the same region and VN as the Domain Controller.
  
  - Logged in to Client-1, pinged DC-1 IP to ensure it's being accessed, and opened Powershell and ran ipconfig /all
    DNS should match DC-1's Private IP.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  - Logged into DC-1 and installed Active Directory Domain Services
  
  - Promoted to Domain Controller and set up a new forest, titling it mydomain.com
    
  - Restarted DC and signed back in using mydomain.com\@useraccount
    
  - In Active Directory Users and Computers, create an Organizational Unit for Employees and Admins
    
  - Created an admin account, moved it into the Domain Admins Security Group, and logged back into the DC
    as mydomain.com\@adminaccount
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
</p>
<br />
