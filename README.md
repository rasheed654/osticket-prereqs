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

<p>
<img <img width="1123" alt="Screenshot 2025-03-26 at 5 52 34 PM" src="https://github.com/user-attachments/assets/bc953b73-af38-4afd-a699-92bc4852d650" />
</p>
<p>
Install PHP Manager for IIS setup. After that install the Rewrite Module.From the OsTicket in installation file folder, unzip PHP 7.3.8 (php- 7.3.8-nts-Win32-VCIS-X86.zip) into the "C:\php" folder on the Cdrive. Then install my VC_redist.x86 file. Lastly install Mysql. As an admin within IIS register PHP and restart it.
</p>
<br />
<p>
<img <img width="1115" alt="Screenshot 2025-03-26 at 6 47 35 PM" src="https://github.com/user-attachments/assets/14d5e5bd-e7ef-4565-a340-893e5156e2fb" />
</p>
<p>
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

