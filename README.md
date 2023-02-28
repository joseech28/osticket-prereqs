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

<p>
<img src="https://i.imgur.com/ECJ3akq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On this step From the Installation Files, download and install MySQL 5.5.62.

</p>
<br />

<p>
<img src="https://i.imgur.com/MNC3olz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Typical Setup
Launch Configuration Wizard (after install)
Standard Configuration
setting Password and username
Open IIS as an Admin and Register PHP from within IIS

</p>
<br />

<p>
<img src="https://i.imgur.com/NcGSe6s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”


</p>
<br />

<p>
<img src="https://i.imgur.com/x9lp458.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”


</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/jyZAhyy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes



</p>
<br />

<p>
<img src="https://i.imgur.com/e9YPAYl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php


</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/M49q2Vq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All


</p>
<br />

</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/kz7cIfA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)



</p>
<br />

<p>
<img src="https://i.imgur.com/qhf4CbN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the Installation Files, download and install HeidiSQL.
Open Heidi SQL Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”




</p>
<br />

</p>
<br />

<p>
<img src="https://i.imgur.com/shHeVWA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osticket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”





</p>
<br />

<p>
<img src="https://i.imgur.com/qhf4CbN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Continue Setting up osticket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”





</p>
<br />












