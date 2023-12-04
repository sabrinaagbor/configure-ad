<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Datacenter Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Installing Active Directory Domain Services.
- Creating an Administrative and Normal User Account within Active Directory.
- Connecting main server to our domain controller.
- Configuring Remote Desktop for non-administrative users on main server.

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/3T3Wvu7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using Server Manager, I use the 'Add Roles and Features Wizard' to select and install Active Directory Services. Once installed, I selected the option to promote the server to a domain controller.
</p>
<br />

<p>
<img src="https://i.imgur.com/jAiSIrb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/SwmMbkA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<p>
In the Server Manager, I went to Tools > Active Directory Users and Computers > Selected my domain name > right-clicked and created new organizational units with the names 'Administrative' and 'Employees' with both posessing different privileges. I have created a user 'Jessica Doe' and added the user to the Domain Admins group.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To join my main server with the domain controller, obtained the private IP address from my domain controller. Within the Networking section for my main server on Azure Portal, I set its DNS Server to that of the private IP from the domain controller. Following this, I right clicked the Start button on the main server > System > Rename this PC (Advanced).
</p>
<br />
