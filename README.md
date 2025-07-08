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

- In the Virtual Machine in Azure, you will download and unzip the osTicket-installation-files.zip
- Enable IIS & CGI
IIS is required to host the web application, and CGI allows PHP scripts to run.
- Install PHP Manager for IIS
Makes it easier to configure and manage PHP settings inside IIS.
- Install URL Rewrite Module
Required by osTicket for clean URLs and proper routing within the application.
- Set Up PHP Folder
Created C:\PHP and extracted PHP files into it. This location is used when registering PHP in IIS.


- Install MySQL and HeidiSQL
MySQL is the database for osTicket. HeidiSQL was used to connect and create the osTicket database.



<h2>Installation Steps</h2>

<p>


![Disk Sanitization Steps](https://raw.githubusercontent.com/NickMehmedov/osticket-prereqs/main/Screenshot%202025-07-08%20003709.png)

Enable IIS & CGI

Open Control Panel → Turn Windows features on or off

Enable Internet Information Services

Under Application Development Features, enable CGI

Enable IIS & CGI

Open Control Panel → Turn Windows features on or off

Enable Internet Information Services

Under Application Development Features, enable CGI

This sets up the web server and allows PHP to function properly.
</p>
<br />


![Disk Sanitization Steps](https://raw.githubusercontent.com/NickMehmedov/osticket-prereqs/main/Screenshot%202025-07-08%20004408.png)


Install PHP Manager & Rewrite Module

Installed PHPManagerForIIS_V1.5.0.msi

Installed rewrite_amd64_en-US.msi

These tools are required for managing PHP settings and enabling URL rewriting, both of which are essential for osTicket.
<br />


![New Screenshot](https://raw.githubusercontent.com/NickMehmedov/osticket-prereqs/main/Screenshot%202025-07-08%20004813.png)

<p>
Configure PHP in IIS

Created C:\PHP and extracted PHP files

Opened IIS > PHP Manager > Registered php-cgi.exe

Restarted IIS

This allows IIS to recognize and run PHP scripts.
</p>
<br />


<p>
Install MySQL & Create Database

Installed MySQL 5.5.62 and set up a root password

Used HeidiSQL to connect and create a new database named osTicket

The database is where all ticket and system data will be stored.

![Screenshot 1](https://raw.githubusercontent.com/NickMehmedov/osticket-prereqs/main/Screenshot%202025-07-08%20004341.png)

<p>
Deploy osTicket Files

Unzipped osTicket-v1.15.8.zip

Copied the upload folder to C:\inetpub\wwwroot

Renamed it to osTicket

This is how the web server serves the osTicket application.

![Screenshot 2](https://raw.githubusercontent.com/NickMehmedov/osticket-prereqs/main/Screenshot%202025-07-08%20005504.png)

<p>
Enable Required PHP Extensions

Enabled php_imap.dll, php_intl.dll, and php_opcache.dll in PHP Manager

These are needed for email integration, international support, and performance.


<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>![Screenshot 3](https://raw.githubusercontent.com/NickMehmedov/osticket-prereqs/main/Screenshot%202025-07-08%20010751.png)


<p>
Run osTicket Web Installer

Opened http://localhost/osTicket in a browser

Entered site/admin info and database details

Finalized the setup and confirmed everything was working.
![Screenshot 4](https://raw.githubusercontent.com/NickMehmedov/osticket-prereqs/main/455268971-79bdbc68-dab7-42f6-a237-24949c807afd.png)

