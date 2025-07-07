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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable IIS & CGI

Open Control Panel → Turn Windows features on or off

Enable Internet Information Services

Under Application Development Features, enable CGI

This sets up the web server and allows PHP to function properly.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install PHP Manager & Rewrite Module

Installed PHPManagerForIIS_V1.5.0.msi

Installed rewrite_amd64_en-US.msi

These tools are required for managing PHP settings and enabling URL rewriting, both of which are essential for osTicket.
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure PHP in IIS

Created C:\PHP and extracted PHP files

Opened IIS > PHP Manager > Registered php-cgi.exe

Restarted IIS

This allows IIS to recognize and run PHP scripts.
</p>
<br />
