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

<p>The first step, is to log in to microsoft azure and create a new virtual machine. Click the "Virtual Machine" Icon</p>
<p><img src="https://i.imgur.com/rKfRVl6.png" height="80%" width="80%"/></p>
<br />
<p>Click "Create" then "Azure Virtual Machine" from the list
<p><img src="https://i.imgur.com/Vw8T2Ih.png" height="80%" width="80%"/></p>
<br />
<p>Select windows 10, and use 2 vcpus and 8GB ram so the computer isn't too slow. The username and password will be the credentials used on remote desktop.</p>
<p><img src="https://i.imgur.com/dpAl2EM.png" height="80%" width="80%"/></p>
<br />
<p>Once the virtual machine is deployed, open remote desktop.</p>
<p><img src="https://i.imgur.com/FlHR3lP.png" height="80%" width="80%"/></p>
<br />
<p>The PC Name is the Virtual Machine's public IP address, which can be found by navigating back to azure and clicking on the Virtual Machine we created</p>
<p><img src="https://i.imgur.com/cEhBF5r.png" height="80%" width="80%"/></p>
<br />
<p>Click "Network Settings" and copy "Public IP Address"</p>
<p><img src="https://i.imgur.com/6iW46ZD.png" height="80%" width="80%"/></p>
<br />
<p>Copy this number into Remote Desktop</p>
<p><img src="https://i.imgur.com/xvtOgLR.png" height="80%" width="80%"/></p>
<br />
<p>Once logged into the virtual machine, download this file on the virtual machine to install
<a href="https://drive.google.com/ucexport=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket</a>.
Extract the contents the desktop by right-clicking the zip file.
</p>
<p><img src="https://i.imgur.com/6JBXpMG.png" height="80%" width="80%"/></p>
<br />
<p>Open the control panel</p>
<p><img src="https://i.imgur.com/M241kq1.png" height="80%" width="80%"/></p>
<br />
<p>Click "Uninstall a program".</p>
<p><img src="https://i.imgur.com/8z33DjA.png" height="80%" width="80%"/></p>
<br />
<p>Click turn windows feature on or off</p>
<p><img src="https://i.imgur.com/LNvXtW0.png" height="80%" width="80%"/></p>
<br />
<p>Enable IIS by clicking "Internet Information Services" then click the dropdown box to the left with the + symbol</p>
<p><img src="https://i.imgur.com/ED9YVEE.png" height="80%" width="80%"/></p>
<br />
<p>Ensure the boxes next to Web Management Tools and World Wide Web Services are checked. Click the dropbox next to World Wide Web Services.</p>
<p><img src="https://i.imgur.com/hqQRyUk.png" height="80%" width="80%"/></p>
<br />
<p>Check the box next to Application Developement Features, Click the dropdown box and check the box next to CGI.</p>
<p><img src="https://i.imgur.com/WpApS9s.png" height="80%" width="80%"/></p>
<br />
<p>Open a browser and enter 127.0.0.1 to verify internet information services are enabled. The screen should look like the following image.</p>
<p><img src="https://i.imgur.com/n82Wwzn.png" height="80%" width="80%"/></p>
<br />
<p>From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)</p>
<p><img src="https://i.imgur.com/f6ZNt9Y.png" height="80%" width="80%"/></p>
<br />
<p>From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)</p>
<p><img src="https://i.imgur.com/AGDoyx2.png" height="80%" width="80%"/></p>
<br />
<p>Create the directory C:\PHP, then from the “osTicket-Installation-Files” folder, extract PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder</p>
<p><img src="https://i.imgur.com/Hu2kBHY.png" height="80%" width="80%"/></p>
<p><img src="https://i.imgur.com/ktIqHKn.png" height="80%" width="80%"/></p>
<br />
<p>From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.</p>
<p><img src="https://i.imgur.com/jP9nKeN.png" height="80%" width="80%"/></p>
<p>From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi). When going through the install wizard, select the following options: Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration -> Username: root, Password: root</p>
<p><img src="https://i.imgur.com/K5YaimU.png" height="80%" width="80%"/></p>
<br />
<p>Open IIS as an admin.</p>
<p><img src="https://i.imgur.com/rx3W9xm.png" height="80%" width="80%"/></p>
<br />
<p>Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe), then restart the server.</p>
<p><img src="https://i.imgur.com/mJjdXrR.png" height="80%" width="80%"/></p>
<p><img src="blob:https://imgur.com/b5d92073-005c-48da-8b97-b0fff8aaa8cb" height="80%" width="80%"/></p>
<br />
<p>From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” to the desktop</p>
<p><img src="https://i.imgur.com/xzOjFZ3.png" height="80%" width="80%"/></p>
<br />
<p>copy the “upload” folder into “c:\inetpub\wwwroot”.</p>
<p><img src="https://i.imgur.com/TDZTysZ.png" height="80%" width="80%"/></p>
<br />
<p>Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”</p>
<p><img src="https://i.imgur.com/7LljKPX.png" height="80%" width="80%"/></p>
<p>Restart the server</p>
<p>Go to sites -> Default -> osTicket. On the right, click “Browse *:80”</p>
<p><img src="https://i.imgur.com/EcU2nz2.png" height="80%" width="80%"/></p>
<br />
<p>Note that some extensions are not enabled</p>
<p><img src="https://i.imgur.com/SUJ3ExS.png" height="80%" width="80%"/></p>
<p>Go back to IIS, click sites, Default, osTicket, Double-click PHP Manager. Click “Enable or disable an extension”</p>
<br />
<p><img src="https://i.imgur.com/Pt7hKYH.png" height="80%" width="80%"/></p>
<br />
<p>Enable: php_imap.dll</p>
<p><img src="https://i.imgur.com/yv4n9En.png" height="80%" width="80%"/></p>
<br />
<p>Enable: php_intl.dll</p>
<p><img src="https://i.imgur.com/eHLxfXW.png" height="80%" width="80%"/></p>
<br />
<p>Enable: php_opcache.dll</p>
<p><img src="https://i.imgur.com/eKBzHf8.png" height="80%" width="80%"/></p>
<br />
Refresh the browser and observe the changes
<p><img src="https://i.imgur.com/riyGcEA.png" height="80%" width="80%"/></p>
<br />
<p>Rename: ost-config.php From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php To: C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>
<p><img src="https://i.imgur.com/sZedcME.png" height="80%" width="80%"/></p>
<br />
<p>Assign Permissions to ost-config.php by right-clicking the file, then click properties, "security" tab, advanced</p>
<p><img src="https://i.imgur.com/Xb1vzpa.png" height="80%" width="80%"/></p>
<br />
<p>Click disable inheritance, remove all permissions</p>
<p><img src="https://i.imgur.com/wtaXHQ9.png" height="80%" width="80%"/></p>
<p>Create new permissions, type Everyone, check the boxes read, write, and execute.</p>
<p><img src="https://i.imgur.com/0POwB3Q.png" height="80%" width="80%"/></p>
<p>Continue Setting up osTicket in the browser (click Continue). Enter helpdesk name. Enter default email address (receives email from customers)</p>
<p><img src="https://i.imgur.com/A1mOCwm.png" height="80%" width="80%"/></p>
<br />
<p>From the “osTicket-Installation-Files” folder, install HeidiSQL.</p>
<p><img src="https://i.imgur.com/HCv9iA2.png" height="80%" width="80%"/></p>
<br />
Open Heidi SQL, Create a new session using username : root and password : root, Connect to the session.
<p><img src="https://i.imgur.com/P4pBisT.png" height="80%" width="80%"/></p>
<p>Create a database called “osTicket”</p>
<p><img src="https://i.imgur.com/p58FC2H.png" height="80%" width="80%"/></p>
<p><img src="https://i.imgur.com/NXqa2dj.png" height="80%" width="80%"/></p>
<br />
<p>Continue Setting up osTicket in the browser, MySQL Database: osTicket, MySQL Username: root, MySQL Password: root, Click “Install Now!”</p>
<p><img src="https://i.imgur.com/k42jEDI.png" height="80%" width="80%"/></p>
<p><img src="https://i.imgur.com/9GPXPPe.png" height="80%" width="80%"/></p>
<p>Browse to your <a href="http://localhost/osTicket/scp/login.php">help desk login page</a>

<a href="http://localhost/osTicket/">End Users osTicket URL</a>
<br />
