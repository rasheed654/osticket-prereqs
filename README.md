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

- Connect to your virtual machine with remote desktop
- Install / Enable IIS in Windows
- Install web platform Installer
- Install Osticket
- Download and Install HeidiSQL
- Setting up OsTicket in the browser

<h2>Installation Steps</h2>

<p>
<img <img width="1170" alt="Screenshot 2025-03-26 at 5 44 19 PM" src="https://github.com/user-attachments/assets/874f051f-2af3-4849-9821-f2adfe41e6ab" />
</p>
<p>
Login to your virtual machine with username and password.
</p>
<br />

<p>
<img <img width="1121" alt="Screenshot 2025-03-26 at 5 47 12 PM" src="https://github.com/user-attachments/assets/b46f9b48-6d76-4fb3-bb89-f88400618067" />
</p>
<p>
In the windows search box type in control panel. then we can go to programs and click uninstall a program and click on turn windows features on/off. look for Internet Information Services and select it. also in the World Wide Web Service go to Application Development Features and select CGI and click ok to install the web service. 
</p>
<br />

<p>
<img <img width="1123" alt="Screenshot 2025-03-26 at 5 52 34 PM" src="https://github.com/user-attachments/assets/bc953b73-af38-4afd-a699-92bc4852d650" />
/>
</p>
<p>
Install PHP Manager for IIS setup. After that install the Rewrite Module.From the OsTicket in installation file folder, unzip PHP 7.3.8 (php- 7.3.8-nts-Win32-VCIS-X86.zip) into the "C:\php" folder on the Cdrive. Then install my VC_redist.x86 file. Lastly install Mysql. 
</p>
<br />
