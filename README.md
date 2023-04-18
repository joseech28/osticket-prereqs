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
<img src="https://imgur.com/8iWKRYp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Build a resource group in azure. 
A location for the resource group 
must be specified when the resource group is created.
</p>
<br />

<p>
<img src="https://imgur.com/Achf9CX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2.  After Establishing a Resource Group
Make a 2-4 Virtual CPU Windows 10 Virtual Machine (VM).
Allow the VM to construct a new Virtual Network (Vnet) when creating it.
</p>
<br />

<p>
<img src="https://imgur.com/MDxReJK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3.  Create a Windows 10 Virtual Machine (VM) now is time to grab the public IP address from azure.
</p>
<br />
<p>
<img src="https://imgur.com/7mvVxFl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. Installing and activating IIS with CGI in Windows
Web Services Features for Application Development 

</p>
<br />

<p>
<img src="https://imgur.com/P9AXzlu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. IIS is now istalled. 
</p>
<br />

<p>
<img src="https://imgur.com/Jv4vaAf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. Download and install PHP Manager for IIS
</p>
<br />
<p>
<img src="https://imgur.com/CVrqVmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. Download and install Rewrite Module
</p>
<br />

<p>
<img src="https://imgur.com/aGYFlGM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Create the directory C:\PHP.
</p>
<br />

<p>
<img src="https://imgur.com/6yAocFG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Download PHP 7.3.8 php-7.3.8-nts-Win32-VC15-x86.zip and unzip the contents into C:\PHP
</p>
<br />
<p>
<img src="https://imgur.com/mmbSnCy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. VC15-x86.zip is now unzipe contents into C:\PHP
</p>
<br />

<p>
<img src="https://imgur.com/aPG6sgN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. download and install VC_redist.x86.exe.

</p>
<br />

<p>
<img src="https://imgur.com/rOffU59.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Download and install MySQL 5.5.62 Typical Setup
Launch Configuration Wizard after install 
Standard Configuration 
Password1

</p>
<br />
<p>
<img src="https://imgur.com/Cj7DA68.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. Open IIS as an Admin
    Register PHP from within IIS
    Reload IIS (Open IIS, Stop and Start the server)

</p>
<br />

<p>
<img src="https://imgur.com/64Y9HPX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
</p>
<br />

<p>
<img src="https://imgur.com/hTm6u9Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
15. Note that some extensions are not enabled
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
<img src="https://imgur.com/2OLg1sb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
16. Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://imgur.com/0AXkoTd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
17. Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

</p>
<br />

<p>
<img src="https://imgur.com/EC4r6BP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
18. Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk Default email (receives email from customers)

</p>
<br />
<p>
<img src="https://imgur.com/K5pqidt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
19. From the Installation Files, download and install HeidiSQL.
Open Heidi SQL 
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”

</p>
<br />

<p>
<img src="https://imgur.com/9JN7Gok.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
20. Continue Setting up osticket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”

</p>
<br />

<p>
<img src="https://imgur.com/WyXMUtk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
21. Congratulations, it is now installed with!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

</p>
<br />
<p>
<img src="https://imgur.com/S0tiu3P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
                                      Now we're in!
</p>
<br />

