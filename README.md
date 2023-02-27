<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/5Lt9VNS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On this step I Created Virtual Machine in Azure
Create a Resource Group
Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPUs
When creating the VM, allow it to create a new Virtual Network (Vnet)
</p>
<br />

<p>
<img src="https://i.imgur.com/7WCDJHN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On this step I will Install and Enable IIS in Windows WITH CGI
World Wide Web Services and Application Development Features 
on my Virtual Machine 
</p>
<br />

<p>
<img src="https://i.imgur.com/zHXkHgz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On this step I will Install and Enable PHP Manager 
From my Installation Files, download and install PHP Manager for IIS PHP Manager laterst application.

</p>
<br />

<p>
<img src="https://i.imgur.com/wyWXP01.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On this step Installation Files, 
download and install the Rewrite Module rewrite_amd64_en-US.msi.

</p>
<br />

<p>
<img src="https://i.imgur.com/k8mHE1U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create the directory C:\PHP
download PHP 7.3.8 php-7.3.8-nts-Win32-VC15-x86.zip and unzip the contents into C:\PHP

</p>
<br />

<p>
<img src="https://i.imgur.com/AYGRlPT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On this step Installation Files, download and install VC_redist.x86.exe.

</p>
<br />
