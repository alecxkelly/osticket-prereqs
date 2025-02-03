<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- OsTicket Prerequisites
- OsTicket Installation 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Create an Azure Virtual Machine Windows 10, 4 vCPUs -> Log into the VM with Remote Desktop -> Within the VM (osticket-vm), I downloaded the osTicket-Installation-Files.zip file and unzipped it onto my desktop. The folder is now called “osTicket-Installation-Files” -> Right-Click folder -> extract all -> Now, Install / Enable IIS in Windows WITH CGI -> Click start menu  -> type Control Panel -> Open -> programs-uninstall a program -> click Turn Window features on or off -> tick, Internet information Services -> expand world wide web services -> application development features -> tick CG1 -> Now From the “osTicket-Installation-Files” folder, install PHP Manager for IIS 
</p>
<br />
