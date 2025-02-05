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
- Enabled IIS
- Installed web platform installer
- Installed MySQL +Setup UN/PW
- Configured OsTicket System

<h2>Installation Steps</h2>

<p>
<img <img width="1440" alt="os ticket STEP 1" src="https://github.com/user-attachments/assets/7a12bd3b-7d05-4284-b462-9b878b02b825"/>
<img /> 
</p>
<p>Create an Azure Virtual Machine Windows 10, 4 vCPUs -> Log into the VM with Remote Desktop -> Within the VM (osticket-vm)
</p>
<br />

<p>
<img <img width="1440" alt="OS STEP 2" src="https://github.com/user-attachments/assets/78d88acd-6b0c-4b82-8db2-e32b1c1339fc"/>
<img /> 
<img <img width="1431" alt="OS STEP 3" src="https://github.com/user-attachments/assets/847c17c8-3bc4-4b6a-ad1d-57e9bd1716af"/>
<img /> 
</p>
<p>
I downloaded the osTicket-Installation-Files.zip file and unzipped it onto my desktop. The folder is now called “osTicket-Installation-Files”
</p>
<br />

<p>
<img <img width="1123" alt="OS STEP 4" src="https://github.com/user-attachments/assets/0858edd1-426b-4bd5-a87d-3f7670d8668d" />
<img /> 
<img width="1440" alt="OS STEP 5" src="https://github.com/user-attachments/assets/3927c2e5-786a-492b-a6d8-55307b1700e4" />
<img /> 
</p>
<p>
I Right-Clicked folder -> extract all -> Now, Install / Enable IIS in Windows WITH CGI -> Click start menu -> type Control Panel -> Open -> programs-uninstall a program -> click Turn Window features on or off -> tick, Internet information Services -> expand world wide web services -> application development features -> ticked CG1 
</p>
<br />

<p>
<img width="1118" alt="OS STEP 6" src="https://github.com/user-attachments/assets/df105448-4821-4c18-89a7-f807abb35e1c"/>
<img /> 
<img width="1121" alt="INSTALLED PHP manager OS STEP 7" src="https://github.com/user-attachments/assets/efea90f2-8a2f-47ba-a423-d44e2f73f3a4"/>
<img /> 
</p>
<p>
Now From the “osTicket-Installation-Files” folder, install PHP Manager for IIS, Open the “osTicket-Installation-Files” folder to look for the PHP manager -> click PHP manager within the OS Ticket files folder to set it up -> next -> tick I Agree -> next -> PHP should now be installed
</p>
<br />

<p>
<img width="1119" alt="OS Ticket STEP 8" src="https://github.com/user-attachments/assets/a6d9c46f-215d-494a-9a92-a9f81505e9f3"/>
<img /> 
<img width="1123" alt="OS STEP 10" src="https://github.com/user-attachments/assets/f2ce5897-6111-4a8c-b91f-2cf2d26cd5b2"/>
<img /> 
</p>
<p>
From the “osTicket-Installation-Files” folder install the Rewrite Module, tick "I accept the terms" -> Install -> Now, Create the directory C:\PHP, Right-Click folder in bottom menu -> click file explorer, go to Windows C Drive in the menu, click -> make a folder in the C Drive, Right click, WhereNew Folder is highlighted, I now have renamed it PHP
</p>
<br />

<p>
<img width="1263" alt="os step 11" src="https://github.com/user-attachments/assets/3f88f717-63d7-4217-9ceb-4c88e0d86202"/>
<img /> 
</p>
<p>
Now, From the “osTicket-Installation-Files” folder, I unzipped the PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder, Right Clicked PHP folder within the Os Ticket files folder, click Browse -> clicked C folder in menu, clicked PHP folder, select, extract
</p>
<br />

<p>
<img width="1124" alt="os step 12" src="https://github.com/user-attachments/assets/fbbea4fa-5f2f-4372-bcdd-e064113da1f2"/>
<img /> 
</p>
<p>
Now From the “osTicket-Installation-Files” folder, I installed VC_redist.x86.exe. Double Clicked the file, I agree, clicked Install
</p>
<br />

<p>
<img width="1122" alt="os step 13" src="https://github.com/user-attachments/assets/25e3a900-43e3-40c8-9395-e14c06002060"/>
<img width="1127" alt="os step14" src="https://github.com/user-attachments/assets/871dc359-f14d-4dc7-bce6-c4caebdaacf4"/>
<img />
</p>
<p>
Now, From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) -> click file -> next -> I accept the terms, click next -> Typical Setup,clicked -> Install, launch it -> tick Standard Configuration -> next -> login with root password -> next -> execute -> finish 
</p>
<br />

<p>
<img width="829" alt="os step 15" src="https://github.com/user-attachments/assets/6f063957-a5c3-41c1-a18d-b76552639142"/>
<img />
</p>
<p>
Now, Open IIS as an Admin, go to start menu, type iis, Right Click-Run as administrator 
</p>
<br />

<p>
<img width="1118" alt="os step 16" src="https://github.com/user-attachments/assets/58896bdc-74f9-43bc-9f75-581ada4fcc1a"/>
<img />
<img width="1125" alt="os step 17" src="https://github.com/user-attachments/assets/4614506f-21e0-41aa-a5e7-89c0cf92bb4b"/>
<img />
</p>
<p>
Now, Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe), click PHP manager-click Register new PHP version, click the 3 dots, click Windows C drive in folder, double click php-cgi, pressed ok -> Reload IIS (Open IIS, Stop and Start the server), click OS ticket in IIS, click restart in the actions menu, press stop, then press start 
</p>
<br />

<p>
<img width="1125" alt="os ticket 18" src="https://github.com/user-attachments/assets/a9d0302f-966f-418f-a68d-5a521b19e5c6"/>
<img />
</p>
<p>
Now, I Install osTicket v1.15.8 -> From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and I copied the “upload” folder into “c:\inetpub\wwwroot”, by going into the folder, Right-click the zip, extract all -> click extract
</p>
<br />

<p>
<img width="1208" alt="os step 19" src="https://github.com/user-attachments/assets/70ffe512-136e-4a88-a5df-b75a02222b50"/>
<img />
<img width="1124" alt="os step 20" src="https://github.com/user-attachments/assets/6e5addbb-56e2-41fe-a730-9c5fb8860e3d" />
<img />
</p>
<p>
Now, to copy the uploaded folder “c:\inetpub\wwwroot”, and Renameed “upload” to “osTicket”, click folder at menu bar, Right-Click, click file explorer, click Windows C drive folder click "inetpub", click "wwwroot", from OS ticket files folder, drag the upload file into the wwwroot folder, Right-click the uploaded folder, rename it
</p>
<br />

<p>
<img <img width="1045" alt="os step 21" src="https://github.com/user-attachments/assets/3dcd0cf2-d4ac-4b86-bf7a-e97497e52159" />
<img />
<img width="1414" alt="os step 22" src="https://github.com/user-attachments/assets/bd8fe6ba-8902-4e73-8436-682dc8dfdef1" />
<img />
<img width="1058" alt="os step 23" src="https://github.com/user-attachments/assets/2d720cf6-f737-4737-986c-efb037e62ded"/>
<img />
</p>
<p>
Next I reloaded IIS (Open IIS, Stop and Start the server) -> Now, go to sites, default and click osTicket and on the right, click “Browse *:80” which will open the osTicket system we've installed-some extensions are not enabled, so now we are back in IIS manager, sites, Default-osTicket, Double-click PHP Manager, click on "enable or disable an extension, Enable: php_imap.dll, Enable: php_intl.dll, Enable: php_opcache.dll
</p>
<br />

<p>
<img width="1027" alt="os step 24" src="https://github.com/user-attachments/assets/da3ad3cd-64e2-4d19-97ad-eae8e67b9aae"/>
<img />
</p>
<p>
Now, I'll Refresh the osTicket site in my browser and observe the changes and see now the checks where extensions were enabled on osTicket Browser
</p>
<br />

<p>
<img width="1178" alt="os step 25" src="https://github.com/user-attachments/assets/20e376e1-4792-4ce8-ae20-1ac53eb24e6c"/>
<img />
<img width="1036" alt="os step 26" src="https://github.com/user-attachments/assets/1aa2911f-7a2f-447d-ba58-f9a2a6ff0f50"/>
<img />
<img width="1434" alt="continue setup OS STEP 27" src="https://github.com/user-attachments/assets/6d600a66-b7b2-40eb-930a-f32d6d6e2c88" />
<img />
</p>
<p>
Now, Rename: ost-config.php -> Now Assign Permissions: ost-config.php, Right click-properties,security-advanced, Click "Disable Inheritance", remove all inherited permissions -> add new permissions, Everyone -> All -> "Select a principal", everyone just for the lab -> ok, check full-control, apply,click ok,click ok -> back to the osticket website,click continue -> continue the setup
</p>
<br />

<p>
<img width="1435" alt="step 28 heidi sql" src="https://github.com/user-attachments/assets/8931521c-613c-4aeb-a41c-9e1d345178d9"/>
<img />
</p>
<p>
Now, From the “osTicket-Installation-Files” folder, I installed HeidiSQL, click on it, I accept, next, next, Install,Finish
</p>
<br />

<p>
<img width="1435" alt="os step 29 name database osTicket" src="https://github.com/user-attachments/assets/077c6996-8236-4312-89bc-c309786c350c" />
<img />
</p>
<p>
Next step after Heidi SQL is installed -> Open Heidi SQL -> Create a new session, root/root -> Connect to the session -> Create a database called “osTicket” which will make use of the osTicket database, fill out the database settings, click install
</p>
<br />

<p>
<img width="1440" alt="osTicket installed step 30" src="https://github.com/user-attachments/assets/0781baad-a81d-4450-8afa-6ff4dd34a1ac"/>
<img />
</p>
<p>
osTicket is now Installed!
</p>
<br />
