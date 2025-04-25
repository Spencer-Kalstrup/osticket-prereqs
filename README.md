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

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/rKfRVl6.png" height="80%" width="80%"/>
</p>

<p>
The first step, is to log in to microsoft azure and create a new virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/Vw8T2Ih.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/dpAl2EM.png" height="80%" width="80%"/>
</p>

</p>
<p>
Be sure to select windows 10 here, the username and password will be the login you use on remote desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/FlHR3lP.png" height="80%" width="80%"/>
</p>

</p>
<p>
Once the virtual machine is deployed, we switch over to the windows app on mac os to use remote desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/cEhBF5r.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/6iW46ZD.png" height="80%" width="80%"/>
</p>

</p>
<p>
The ip address for the virtual machine can be found under network settings, be sure to use the public ip address instead of the private ip address.
</p>
<br />

<p>
<img src="https://i.imgur.com/xvtOgLR.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/6JBXpMG.png" height="80%" width="80%"/>
</p>

<p>
Once logged into the virtual machine, download this file on the virtual machine to install <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">os Ticket</a></h1>. Extract the contents the desktop by right-clicking the zip file.
</p>
<br />

<p>
<img src="https://i.imgur.com/M241kq1.png" height="80%" width="80%"/>
</p>

<p>
Next we will enable IIS with CGI by navigating to the control panel and clicking "Uninstall a program".
</p>
<br />

<p>
<img src="https://i.imgur.com/8z33DjA.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/LNvXtW0.png" height="80%" width="80%"/>
</p>

<p>
Click turn windows feature on or off.
</p>
<br />

<p>
<img src="https://i.imgur.com/ED9YVEE.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/hqQRyUk.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/WpApS9s.png" height="80%" width="80%"/>
</p>

<p>
Click the following drop down boxes and ensure the correct boxes are checked. Once this is completed, open a browser and enter 127.0.0.1 to verify internet information services are enabled. The screen should look like the following image.
</p>
<br />

<p>
<img src="https://i.imgur.com/n82Wwzn.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/f6ZNt9Y.png" height="80%" width="80%"/>
</p>

<p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/AGDoyx2.png" height="80%" width="80%"/>
</p>

<p>
From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img src="https://i.imgur.com/Hu2kBHY.png" height="80%" width="80%"/>
</p>

<p>
Create the directory C:\PHP, then from the “osTicket-Installation-Files” folder, extract PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<br />

<p>
<img src="https://i.imgur.com/ktIqHKn.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/jP9nKeN.png" height="80%" width="80%"/>
</p>

<p>
From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
</p>
<br />

<p>
<img src="https://i.imgur.com/K5YaimU.png" height="80%" width="80%"/>
</p>

<p>
From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi). When going through the install wizard, select the following options:
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Username: root
Password: root
</p>
<br />

<p>
<img src="https://i.imgur.com/rx3W9xm.png" height="80%" width="80%"/>
</p>

<p>
Open IIS as an admin.
</p>
<br />

<p>
<img src="https://i.imgur.com/mJjdXrR.png" height="80%" width="80%"/>
</p>

<p>
Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe), then restart the server.
</p>
<br />

<p>
<img src="blob:https://imgur.com/b5d92073-005c-48da-8b97-b0fff8aaa8cb" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/xzOjFZ3.png" height="80%" width="80%"/>
</p>

<p>
Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” to the desktop
  and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
Restart the server
</p>
<br />

<p>
<img src="https://i.imgur.com/TDZTysZ.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/7LljKPX.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/EcU2nz2.png" height="80%" width="80%"/>
</p>

<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
</p>
<br />

<p>
<img src="https://i.imgur.com/SUJ3ExS.png" height="80%" width="80%"/>
</p>

<p>
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
</p>
<br />

<p>
<img src="https://i.imgur.com/Pt7hKYH.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/yv4n9En.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/eHLxfXW.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/eKBzHf8.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/riyGcEA.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/sZedcME.png" height="80%" width="80%"/>
</p>

<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>
<img src="https://i.imgur.com/Xb1vzpa.png" height="80%" width="80%"/>
</p>

<p>
Assign Permissions to ost-config.php by right-clicking the icon -> properties -> security -> advanced -> disable inheritance -> remove all
new permissions -> everyone -> all
</p>
<br />

<p>
<img src="https://i.imgur.com/wtaXHQ9.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/0POwB3Q.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/A1mOCwm.png" height="80%" width="80%"/>
</p>

<p>
Continue Setting up osTicket in the browser (click Continue)
Name: Helpdesk
Default email (receives email from customers)
</p>
<br />

<p>
<img src="https://i.imgur.com/HCv9iA2.png" height="80%" width="80%"/>
</p>

<p>
From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/P4pBisT.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/p58FC2H.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/NXqa2dj.png" height="80%" width="80%"/>
</p>

<p>
<img src="https://i.imgur.com/k42jEDI.png" height="80%" width="80%"/>
</p>

<p>
Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
</p>
<br />

<p>
<img src="https://i.imgur.com/9GPXPPe.png" height="80%" width="80%"/>
</p>

<p>
Browse to your <a href="http://localhost/osTicket/scp/login.php">help desk login page</a></h1>.

<a href="http://localhost/osTicket/">End Users osTicket URL</a></h1>.
</p>
<br />
