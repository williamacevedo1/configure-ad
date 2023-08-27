<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Deployed in the Cloud (Azure)</h1>
This project outlines the implementation of Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Set up Cloud(azure) VM's
- Test Connectivity
- Install Active Directory
- User Creation

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/EPAdQzH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, I set up the resource group. Next, I created the first virtual machine named "DC-1," which will serve as the domain controller. Following that, I proceeded to create the second virtual machine named "client-1." I then associated "client-1" with the virtual network of "DC-1." Finally, I configured the Private IP address of "DC-1" to be static.
</p>
<br />

<p>
<img src="https://i.imgur.com/4E8VGpF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After logging into DC-1, I accessed the Windows Firewall settings and enabled the inbound rule for ICMPv4. Subsequently, I logged in to client-1 and opened the command line. From there, I obtained the private IP address of DC-1 and proceeded to ping it for connectivity testing.
</p>
<br />

<p>
<img src="https://i.imgur.com/4OHaPJr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within DC-1, I navigated to Server Manager and selected "Add Roles." Following that, I installed Active Directory Domain Services and subsequently promoted the server to function as a domain controller.
</p>
<br />

<p>
<img src="https://i.imgur.com/Ng5UOtX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I launched PowerShell ISE with administrator privileges and used a script to create users within the "employee" folder that I had previously set up in files.
</p>
<br />

<p>
<img src="https://i.imgur.com/5FTtIYY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
