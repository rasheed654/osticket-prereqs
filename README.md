<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>OsTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Connect to your virtual machine with remote desktop
- Install / Enable IIS in Windows
- Install web platform Installer
- Install Osticket
- Download and Install HeidiSQL
- Setting up OsTicket in the browser

<h2>Installation Steps</h2>
<h3>Step 1</h3>
<p>
<img width="1046" alt="Screenshot 2025-04-24 at 2 37 02 PM" src="https://github.com/user-attachments/assets/ab371dfa-b3e9-4cc5-be6f-6aa1298fa3e5" />
</p>
<p>
Create an Azure Virtual Machine Windows 10, 4 vCPUs
Name: osticket-vm
Username: labuser
Password: osTicketPassword1!

</p>
<br />
<h3>Step 2</h3>
<p>
<img <img width="1170" alt="Screenshot 2025-03-26 at 5 44 19 PM" src="https://github.com/user-attachments/assets/874f051f-2af3-4849-9821-f2adfe41e6ab" />
</p>
<p>
Login to your virtual machine with username and password.
</p>
<br />
<h3>Step 3</h3>
<p>
<img width="1087" alt="image" src="https://github.com/user-attachments/assets/664f06d5-1e06-4e7e-8ab5-72ad87aaf4cb" />

</p>
<p>
Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
I will use the files in this folder to install osTicket and some of the dependencies.

</p>
<br />
<h3>Step 4</h3>
<p>
<img width="786" alt="Screenshot 2025-04-24 at 2 47 04 PM" src="https://github.com/user-attachments/assets/02e85bf3-7900-4a26-a541-a68f913f840b" />

</p>
<p>
 
In the windows search box type in control panel.
<h3>Step 5</h3>
<img width="1122" alt="Screenshot 2025-04-24 at 2 47 33 PM" src="https://github.com/user-attachments/assets/693d26d3-682d-4bae-bf59-e41d4ef66109" />


then we can go to programs and click uninstall a program and click on turn windows features on/off. 
<h3>Step 6</h3>
<img width="1124" alt="Screenshot 2025-04-24 at 2 54 14 PM" src="https://github.com/user-attachments/assets/73fd48f9-43a6-4d5d-9e17-ff462f1283a8" />

look for Internet Information Services and select it. also in the World Wide Web Service go to Application Development Features and select CGI and click ok to install the web service. 
</p>
<br />
<h3>Step 7</h3>
<p>
 <img width="1121" alt="Screenshot 2025-04-24 at 3 07 51 PM" src="https://github.com/user-attachments/assets/de56c00f-4b77-4f97-a051-80b2284e0ae0" />

<img width="1123" alt="Screenshot 2025-03-26 at 5 52 34 PM" src="https://github.com/user-attachments/assets/bc953b73-af38-4afd-a699-92bc4852d650" />

 <p>
<img width="499" alt="Screenshot 2025-04-24 at 3 06 47 PM" src="https://github.com/user-attachments/assets/154bc918-8550-4540-ada4-d70b9753ac2d" />
</p>
</p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

<p>
<h3>Step 8</h3>
<img width="1124" alt="Screenshot 2025-04-24 at 3 17 40 PM" src="https://github.com/user-attachments/assets/a2b89a66-50e5-49ad-82d9-52fd45a159a7" />
<img width="491" alt="Screenshot 2025-04-24 at 3 18 29 PM" src="https://github.com/user-attachments/assets/be37ed9e-fa8d-402e-a022-8fa32d105da0" />
</p>
From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

<p>

<br />
<p>
<h3>Step 9 Create the directory C:\PHP </h3>
<img width="1124" alt="Screenshot 2025-04-24 at 3 30 12 PM" src="https://github.com/user-attachments/assets/c08bee5c-9d74-4b79-aab5-e568427648fd" />
<p>
in the windows File explorer go to Cdrive
</p>



<img width="1127" alt="Screenshot 2025-04-24 at 3 32 27 PM" src="https://github.com/user-attachments/assets/1df82d14-c8a8-43aa-8da5-f9dc43a0ef5e" />
<p>
next we are going to create a folder on the Cdrive called capital PHP
 </p>
<h3>Step 10</h3>
<p> From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<img width="1124" alt="Screenshot 2025-04-24 at 3 40 35 PM" src="https://github.com/user-attachments/assets/707b8585-4741-4741-bf65-1eaa90dceba9" />
<img width="1107" alt="Screenshot 2025-04-24 at 3 41 35 PM" src="https://github.com/user-attachments/assets/5f04f0af-7e59-40d5-a2aa-2c762ccda573" />


<br />
<h3>Step 11</h3>

<img width="1126" alt="Screenshot 2025-04-24 at 3 53 22 PM" src="https://github.com/user-attachments/assets/990d7a36-c1ec-469c-b006-498acbaf23b6" /><img width="472" alt="Screenshot 2025-04-24 at 3 54 13 PM" src="https://github.com/user-attachments/assets/60bca9af-0f42-44e1-8d53-b682ffb9479b" />

<p> install VC_redist.x86.exe. From the “osTicket-Installation-Files” folder.

</p>
</p>
<h3>Step 12</h3>
<img width="1127" alt="Screenshot 2025-04-24 at 3 59 07 PM" src="https://github.com/user-attachments/assets/7438d63a-6fde-4ce7-89ef-dc694dc7bdc4" />
<p>From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
</p>
<img width="495" alt="Screenshot 2025-04-24 at 4 00 00 PM" src="https://github.com/user-attachments/assets/b7fab071-373c-4dee-8ea9-4cad3418f0ae" />
<p>Click on tipical Setup and hit then hit install
</p>
 <img width="343" alt="image" src="https://github.com/user-attachments/assets/0cac1b4b-e44f-4d7c-b689-abbcfbce4b86" />
<p>Next we Launch Configuration Wizard (after install) </p>
<img width="499" alt="Screenshot 2025-04-24 at 4 08 22 PM" src="https://github.com/user-attachments/assets/3c569dcc-a240-4f14-b49f-f8843ab5ba02" />
<p>Click on Standard Configuration</p>
In the OsTicket installation files folder, unzip "OsTicket-w.15.8.zip" and copy the upload folder in "c:\inetpub\wwwroot". Within "C:inetpub\wwwroot", Rename " upload" to "osTicket". Reload IIS by opening IIS, stop and start the server.
</p>
<br />
<img width="599" alt="Screenshot 2025-03-26 at 7 10 39 PM" src="https://github.com/user-attachments/assets/ae3dcf4f-4723-4b0f-9c04-d35c89527c2c" />

 <p>
In the OsTicket installation files folder install HeidiSQL Setup , Create a new session with root as username and password. Lastly we connected to the session and created a database called "osTicket".
</p>
<br />
<img <img width="823" alt="Screenshot 2025-03-26 at 7 29 39 PM" src="https://github.com/user-attachments/assets/d6f94389-c4fd-4cbf-a27e-a403d55bcd4f" />

 <p>
In MYsql Database"osTicket" and then puttin in your username and password click install now.
</p>

