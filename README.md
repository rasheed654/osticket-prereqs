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
<img width="498" alt="image" src="https://github.com/user-attachments/assets/5a901ba3-0a22-4f66-923b-c876248285e2" />
<p>Type in a username and password and then click execute</p>

<h3>Step 13</h3>

<img width="768" alt="Screenshot 2025-04-24 at 4 17 43 PM" src="https://github.com/user-attachments/assets/85177c0b-9979-4536-9899-54afa9125f4b" />\
<p>Open IIS as an Admin</p>
<img width="1248" alt="Screenshot 2025-04-24 at 4 20 17 PM" src="https://github.com/user-attachments/assets/18b6dc1b-c23d-43e2-a14d-3f5e1a5c4a9d" />
<p>next select PHP Manager</p>
<img width="1667" alt="Screenshot 2025-04-24 at 4 24 38 PM" src="https://github.com/user-attachments/assets/97ef084d-76af-409a-85ef-596e80886d24" />
<p>Next select new Register new php version</p>
<img width="1108" alt="Screenshot 2025-04-24 at 4 27 17 PM" src="https://github.com/user-attachments/assets/2375825a-d533-4e08-acb2-b5f64a54451e" />
<p>Then Browse through the Php folder and look for php-cgi and click on it</p>
<img width="200" alt="Screenshot 2025-04-24 at 4 34 09 PM" src="https://github.com/user-attachments/assets/c5b0fe9d-6084-48de-8fcc-3d64e3420617" />

<p>Reload IIS by Stopping and starting the server</p>

<h3>Step 14</h3>
<img width="1124" alt="Screenshot 2025-04-24 at 4 40 20 PM" src="https://github.com/user-attachments/assets/000333ac-d5ef-4c36-9782-ed705e0d7d77" />

<p>Install osTicket v1.15.8 From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip”</p>
<img width="1126" alt="Screenshot 2025-04-24 at 4 43 49 PM" src="https://github.com/user-attachments/assets/df67e8b6-730f-4efb-a47d-62efc099cbd9" />
<img width="1125" alt="Screenshot 2025-04-24 at 4 45 02 PM" src="https://github.com/user-attachments/assets/a46ec4d7-fa47-4095-8286-e6fa4df86372" />
<p>In the OsTicket installation files folder, unzip "OsTicket-w.15.8.zip" and copy the upload folder in "c:\inetpub\wwwroot". </p>

 

</p>

<img width="1117" alt="Screenshot 2025-04-24 at 4 54 15 PM" src="https://github.com/user-attachments/assets/5a56a954-bf3b-4189-be99-e68d20d2ff98" />

<p>Within "C:inetpub\wwwroot", Rename " upload" to "osTicket".</p>
<br />
<img width="1121" alt="image" src="https://github.com/user-attachments/assets/aa860e10-1243-4e21-9972-fe6aaafae032" />
<p>Reload IIS by Stopping and starting the server</p>
<img width="1120" alt="Screenshot 2025-04-24 at 5 01 56 PM" src="https://github.com/user-attachments/assets/f4d0324b-0217-4f4b-b349-67dc27a9a76a" />
<img width="1100" alt="Screenshot 2025-04-24 at 5 15 44 PM" src="https://github.com/user-attachments/assets/6237dadf-66bd-432f-b122-00892edd760a" />

Go to sites then Default and click osTicket
On the right, click “Browse *:80”


</p>
<br />
<h3>Step 15</h3>

<<img width="1123" alt="Screenshot 2025-04-24 at 5 24 57 PM" src="https://github.com/user-attachments/assets/86e6f286-6e43-4cc6-9c66-0103d56c0ade" />


<p>To enable some extensions we got to Go back to IIS, sites -> Default -> osTicket
 </p>

 <img width="1121" alt="Screenshot 2025-04-24 at 5 23 44 PM" src="https://github.com/user-attachments/assets/146ca36b-e2fc-4a64-a4d4-cc5c2b230c72" />
<p>Double-click PHP Manager and then Click “Enable or disable an extension”
</p>
<img width="1105" alt="Screenshot 2025-04-24 at 5 29 47 PM" src="https://github.com/user-attachments/assets/1d1b056b-b8b4-4cc4-b1c4-8b32ef2b3b49" />

<p>Enable these three extentions Enable: php_imap.dll,Enable: php_intl.dll, Enable: php_opcache.dll
</p>
<img width="825" alt="Screenshot 2025-04-24 at 5 33 37 PM" src="https://github.com/user-attachments/assets/1f88507a-c543-44a8-b3b7-4fcd3ade5fc1" />

<p>Refresh the OsTicket browser and observe the changes</p>




  <h3>Step 16</h3>
  <h4>Rename ost-config.php</h4>
<img width="1119" alt="Screenshot 2025-04-24 at 5 37 23 PM" src="https://github.com/user-attachments/assets/e0063f4d-5808-4376-85df-14d14d72cc51" />
 <img width="1115" alt="Screenshot 2025-04-24 at 5 37 41 PM" src="https://github.com/user-attachments/assets/f2837e7f-574d-4564-8c59-85d8f63a640a" />
 <img width="1118" alt="Screenshot 2025-04-24 at 5 38 59 PM" src="https://github.com/user-attachments/assets/ed94ae9e-1a62-417a-88a3-15bb97ff690f" />

<p> From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
</p>

<img width="1115" alt="Screenshot 2025-04-24 at 5 39 39 PM" src="https://github.com/user-attachments/assets/0d6de784-d238-4261-bb05-e85474d4930a" />
<p>To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<h4>Assign Permissions</h4>
<img width="363" alt="Screenshot 2025-04-24 at 5 47 56 PM" src="https://github.com/user-attachments/assets/12eef890-156d-4143-bc4d-c2fd1900a8fc" />
<img width="360" alt="Screenshot 2025-04-24 at 5 48 28 PM" src="https://github.com/user-attachments/assets/f1352975-ac23-4694-8ab4-a55dcd391bd2" />
<img width="768" alt="Screenshot 2025-04-24 at 5 49 24 PM" src="https://github.com/user-attachments/assets/d32d1389-78fa-4468-a953-33fa312e112a" />
<p>Disable Inheritance</p>

