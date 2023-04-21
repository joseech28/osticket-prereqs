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
1. Firstly, I created a resource group in Azure for my osTicket system. While creating the resource group, I specified its 
location.  
</p>
<br />

<p>
<img src="https://imgur.com/Achf9CX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. After that, I set up a virtual machine (VM) on the resource group with 2-4 virtual CPUs running on Windows 10. I also 
configured the VM to create a new Virtual Network (Vnet) during its setup process.  
</p>
<br />

<p>
<img src="https://imgur.com/MDxReJK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Now that the Windows 10 VM is up and running, I retrieved its public IP address from the Azure portal. This IP address 
will be used to access the VM remotely.  
</p>
<br />
<p>
<img src="https://imgur.com/7mvVxFl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. Next, I install and activate the Internet Information Services (IIS) with Common Gateway Interface (CGI) feature on the 
Windows VM. This feature is essential for running PHP-based applications such as osTicket.  
</p>
<br />

<p>
<img src="https://imgur.com/P9AXzlu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. Once IIS is installed.
</p>
<br />

<p>
<img src="https://imgur.com/Jv4vaAf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. I proceed to download and install the PHP Manager for IIS, which helps me to manage the PHP 
installations and configurations within IIS.  
</p>
<br />
<p>
<img src="https://imgur.com/CVrqVmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. Then, I download and install the IIS Rewrite Module, which enables me to rewrite URLs in a user-friendly format.  
</p>
<br />

<p>
<img src="https://imgur.com/aGYFlGM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. After that, I created a directory called C:\PHP on the VM's local disk, where I will install PHP.  
</p>
<br />

<p>
<img src="https://imgur.com/6yAocFG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Now, I download the PHP 7.3.8 zip file (php-7.3.8-nts-Win32- VC15-x86.zip) and unzip its contents into the C:\PHP 
directory that I created earlier. 
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
11. Once the zip file contents are extracted, I download and install VC_redist.x86.exe, which is a prerequisite for PHP to run 
on Windows.  

</p>
<br />

<p>
<img src="https://imgur.com/rOffU59.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. After that, I download and install MySQL 5.5.62 Typical Setup on the VM. Once the installation is complete, I launched 
the Configuration Wizard to configure MySQL for use with osTicket. I choose the Standard Configuration option and set the 
password to "Password1".  

</p>
<br />
<p>
<img src="https://imgur.com/Cj7DA68.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. With MySQL installed and configured, I open IIS as an Administrator and register PHP from within IIS. I also reload IIS 
by stopping and starting the server.  
</p>
<br />

<p>
<img src="https://imgur.com/64Y9HPX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Next, I download the latest osTicket version (v1.15.8) and extract its contents to a folder named "upload". Then, I copy 
the entire "upload" folder to the C:\inetpub\wwwroot directory on the VM. Within the C:\inetpub\wwwroot directory, I rename 
the "upload" folder to "osTicket".  
</p>
<br />

<p>
<img src="https://imgur.com/hTm6u9Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
15. After that, I check that all required PHP extensions are enabled in IIS. I navigate to IIS > Sites > Default > osTicket 
and double-click PHP Manager. Then, I click "Enable or disable an extension" and enable the following extensions: 
php_imap.dll, php_intl.dll, and php_opcache.dll. Finally, I refresh the osTicket site in my browser and verify the changes.  
14. Following that, I rename the "ost-sampleconfig.php" file located in C:\inetpub\wwwroot\osTicket\include to "ost-
config.php". This file contains the configuration settings for osTicket.  
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
17. Then, I assigned appropriate permissions to the "ost-config.php" file. I disabled inheritance, removed all inherited 
permissions, and added a new permission for "Everyone" with "All" access.  

</p>
<br />

<p>
<img src="https://imgur.com/EC4r6BP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
18. With the permissions set up, I continued setting up osTicket in my browser by clicking "Continue". I provided a name for 
the helpdesk and set the default email address that receives email from customers.  
</p>
<br />
<p>
<img src="https://imgur.com/K5pqidt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
19. Next, I downloaded and installed HeidiSQL from the installation files. I opened HeidiSQL and created a new session with 
the username "root" and password "Password1", once there I created a dabase called “osTicket”.  

</p>
<br />

<p>
<img src="https://imgur.com/9JN7Gok.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
20. Alright, moving forward with the setup of osticket in my browser. First, I needed to input my MySQL Database information 
which includes my osTicket MySQL Username, which is "root", and my MySQL Password, which is "Password1". Once I have filled 
in the necessary details, I can proceed by clicking on the button that says "Install Now!".  
</p>
<br />

<p>
<img src="https://imgur.com/WyXMUtk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
21.  Great news, I have successfully finished the installation! To access the login page of my help desk, I can simply go to 
this URL: http://localhost/osTicket/scp/login.php. 
</p>
<br />
<p>
<img src="https://imgur.com/S0tiu3P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  21. Now we're in!
</p>
<br />

