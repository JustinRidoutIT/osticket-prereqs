<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and How to Install</h1>
osTicket is an open source ticketing system. Ticketing systems are used in Information Technology (IT) for users to create requests for service. It is widely used across all areas of IT especially help desk. This tutorial will go over how to install osTicket on an Azure virtual machine. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable IIS 
- Download web platform installer, MySQL, PHP
- Download PHP lastest version, install PHP manager
- Register New php version
- Download OsTicket

<h2>Installation Steps</h2>
<p> 
Preparing our Virtual Machine to install and use osTicket was a lengthy process. In the prerequisites above, you can see that first we had to enable IIS, download Web Platform installer, MySQL, PHP, and install PHP Manager and register new PHP versions to fix the failures and to be able to properly install OsTicket. 
</p>
</br>

<h3>Step 1: Install Internet Information Services </h3>
The first step is to install Internet Information Services (IIS) in Windows. Go to the Start menu and type in "Control Panel" in the search bar and open it. Click "Uninstall a program" and check Internet Information Services. 
</br>

<h3>Step 2: Install Web Platform Installer</h3> 
Next is to install Web Platform Installer. 

<p></p>

First, you need to open the download files [at this link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) and download Web Platform Installer. Then open up the file in the Downloads folder and install the application. 

<p>
<img src="https://i.imgur.com/TVHltiS.png" height="80%" width="80%" alt="6."/>
</p>

Once installed, go to the Start menu, type it in, and open the application. 

Install the following:
- MySQL 5.5 (This will ask for credentials. Account: root Password: Password1.)
- All simple versions of x86 PHP up until 7.3

<p>
<img src="https://i.imgur.com/pqDM8rr.png" height="80%" width="80%" alt="8."/>
</p>

Follow the installation process carefully. The Installer will fail installing some of the items. Find those items in the Google Drive folder that was mentioned previously.

Install the following:
- PHP Version 7.3.8.
- Microsoft Visual C++ 2009 Redistributable Package.
- PHP Manager 1.5.0 for IIS 10.

<p>
<img src="https://i.imgur.com/nQoI9GZ.png" height="80%" width="80%" alt="10."/>
</p>

<h3>Step 3: Install osTicket</h3>
The third step is to install osTicket. Go to the Google Drive mentioned above and download the osTicket files. Once it is downloaded, open the osTicket folder. Copy the "Upload" folder. 

Paste "c:\inetpub\wwwroot" into the explore bar in the Windows Explorer Window. Paste the "Upload" folder into the wwwroot folder and rename it to "osTicket."

Once you've completed the above, open up IIS from the start menu. Open up the directory, then go to sites, then osTicket. Once osTicket has been opened in IIS, click "Browse *:80 (http)".

<p>
<img src="https://i.imgur.com/kYMCMY2.png" height="80%" width="80%" alt=""/>
</p>

Before going forward with the osTicket Installer, there must be some add-ons enabled first. Go back to IIS and click on "PHP Manager." Then click "Enable or disable an extension."

Right click and enable the following: 
- php_imap.dll.
- php_intl.dll.
- php_opcache.dll.

Once this is done, go back to the osTicket Installer. Start to fill out the setup page until you get to the database settings. 

<h3>Step 4: Install HeidiSQL</h3>
The final step to installing osTicket is installing HeidiSQL.
Go back to the Google Drive with the downloads in it and download HeidiSQL if you haven't already. Once it's downloaded, open the installer and install the application. 
</br>
<p>
<img src="https://i.imgur.com/OnSF4i9.png" height="80%" width="80%" alt=""/>
</p>
<p>
If everything is downloaded correctly, you should be able to now use OsTicket in your virtual machine!
</p>
