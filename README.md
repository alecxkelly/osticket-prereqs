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
<p>Create an Azure Virtual Machine Windows 10, 4 vCPUs -> Log into the VM with Remote Desktop -> Within the VM (osticket-vm), I downloaded the osTicket-Installation-Files.zip file and unzipped it onto my desktop. The folder is now called “osTicket-Installation-Files” -> Right-Click folder -> extract all -> Now, Install / Enable IIS in Windows WITH CGI -> Click start menu  -> type Control Panel -> Open -> programs-uninstall a program -> click Turn Window features on or off -> tick, Internet information Services -> expand world wide web services -> application development features -> tick CG1 -> Now From the “osTicket-Installation-Files” folder, install PHP Manager for IIS, Open the “osTicket-Installation-Files” folder to look for the PHP manager -> click PHP manager within the OS Ticket files folder to set it up -> next -> tick I Agree -> next -> PHP should now be installed -> From the “osTicket-Installation-Files” folder install the Rewrite Module, tick "I accept the terms" -> Install -> Now, Create the directory C:\PHP, Right-Click folder in bottom menu -> click file explorer, go to Windows C Drive in the menu, click -> make a folder in the C Drive, Right click, New Folder name it PHP -> Now, From the “osTicket-Installation-Files” folder, I unzipped the PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder, Right Click PHP folder within the Os Ticket files folder, click Browse -> click C folder in menu, click PHP folder, select, extract -> Now From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe. Double Click the file, I agree, Install -> Now, From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) -> click file -> next -> I accept the terms, click next -> Typical Setup,clicked -> Install, launch it -> tick Standard Configuration -> next -> login with root password -> next -> execute -> finish -> Now,Open IIS as an Admin, go to start menu, type iis, Right Click-Run as administrator -> Now,Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe), click PHP manager-click Register new PHP version, click the 3 dots, click Windows C drive in folder, double click php-cgi, press ok -> Reload IIS (Open IIS, Stop and Start the server), click OS ticket in IIS, click restart in the actions menu, press stop, then press start -> Now, Install osTicket v1.15.8
 -> From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and I copied the “upload” folder into “c:\inetpub\wwwroot”,by going into the folder, Right-click the zip, extract all -> click extract ->  -> Now, to copy the uploaded folder “c:\inetpub\wwwroot”,and Rename “upload” to “osTicket”, click folder at menu bar, Right-Click, click file explorer, click Windows C drive folder click "inetpub", click "wwwroot", from OS ticket files folder, drag the upload file into the wwroot fodler, Right-click the uploaded folder, rename it -> Next I reloaded IIS (Open IIS, Stop and Start the server) -> Now, go to sites, default and click osTicket and on the right, click “Browse *:80” which will open the osTicket system we've installed-some extensions are not enabled, so now we are back in IIS manager, sites, Default-osTicket, Double-click PHP Manager, click on "enable or disable an extension, Enable: php_imap.dll, Enable: php_intl.dll, Enable: php_opcache.dll -> Now, I'll Refresh the osTicket site in my browser and observe the changes and see now the checks where extdnsions were enabled on osTicket Browser -> Now, Rename: ost-config.php -> Now Assign Permissions: ost-config.php, Right click-properties,security-advanced, Click "Disable Inheritance", remove all inherited permissions -> add new permissions, Everyone -> All -> "Select a principal", everyone just for the lab -> ok, check full-control, apply,click ok,click ok -> back to the osticket website,click continue -> continue the setup -> 
Now, From the “osTicket-Installation-Files” folder, I installed HeidiSQL, click on it, I accept, next, next, Install,Finish

Next step after Heidi SQL is installed -> Open Heidi SQL -> Create a new session, root/root -> Connect to the session -> Create a database called “osTicket” which will make use of the osTicket database, fill out the database settings, click install
 
</p>
<br />
