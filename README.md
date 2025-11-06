<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines a lab I created to showcase the skills I've gained through my never-ending studies of Tech. This is a prerequisite for installing the open-source help desk ticketing system, osTicket.
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Virtual machines
- osTicket
- Heidi SQL

<h2>Installation Steps</h2>

<p>
<img 1>
</p>
<p>
Download and install osTicket. Right-click and extract all of the files from the zip file onto the desktop
Install/Enable IIS in Windows with CGI, the web server on which osTicket will run, turning the PC into a web server. Go to Control Panel→Programs→Programs & Features→Turn Windows features on or off. Select and expand the following boxes→Internet Information Serveices→World Wide Web Services→Application Development Features→CGI. Click OK.


</p>
<br />

<p>
<img 2>
</p>
<p>
The next step is to install the PHP Manager for IIS. PHP is a backend web server language that osTicket uses. Open the osTicket file that was unzipped earlier. Double-click and install PHPManagerForIIS_V1.5.0.
</p>
<br />

<p>
<img 3>
</p>
<p>
Install rewrite, open rewrite_amd64_en-US file. Accept the terms in the License Agreement and install.
</p>
<br />

<p>
<img 4>
</p>
<p>
Create a folder named PHP on the C: Drive. Right-click and extract all the PHP-7.3.8-nts-Win-VC15-x86 into the new C: Drive.
</p>
<br />

<p>
<img 5>
</p>
<p>
Open the CV_redist.x86 file and install.
Open and install the Mysql-5.5.62-win32, select typical setup, standard config, create user username ROOT and password ROOT, select execute.
</p>
<br />

<p>
<img 6>
</p>
<p>
Open ISS as an admin. Search for Internet Information Services, Right-click, and run as admin.
</p>
<br />

<p>
<img 7>
</p>
<p>
Register PHP from within ISS by opening PHP
</p>
<br />

<p>
<img 8>
</p>
<p>
Click the register PHP version. Browse by clicking the three dots and selecting C:\PHP\php-cgi.exe.
</p>
<br />

<p>
<img 9>
</p>
<p>
Reload ISS by stopping and starting the server.
</p>
<br />

<p>
<img 10>
</p>
<p>
Install osTicket v1.15.8. From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, rename “upload” to “osTicket”

</p>
<br />

<p>
<img 11 but use image 9>
</p>
<p>
Reload ISS by stopping and starting the server.
</p>
<br />

<p>
<img 12>
</p>
<p>
Load the osTicket website, go to sites→Default→osTicket. On the right, click “Browse*:80 (http)”
</p>
<br />

<p>
<img13>
</p>
<p>
Note the extensions that need to be installed.
</p>
<br />

<p>
<img 14>
</p>
<p>
Go back to ISS manager and select Sites→Default→osTicket. Double-click PGP Manager
</p>
<br />

<p>
<img 15>
</p>
<p>
Scroll through the options and enable: php_imap.dll, php_intl.dll, and php_opcache.dll.
</p>
<br />

<p>
<img 16>
</p>
<p>
Refresh the osTicket installer.
</p>
<br />

<p>
<img 17>
</p>
<p>
Rename: “ost-sampleconfig.php” to “ost-config.php.” Open file explorer→C: drive→inetpub→wwwroot→osTicket→include. Find and rename ost-sampleconfig.php to ost-config.php.
</p>
<br />

<p>
<img 18>
</p>
<p>
Assign osTicket permissions to modify the config file. Right-click ost-config.php→properties→security→advanced→disable inheritance→remove all permissions. 
</p>
<br />

<p>
<img 19>
</p>
<p>
Add new permissions, click add, type “everyone”, and select OK. 
</p>
<br />

<p>
<img 20>
</p>
<p>
Select Full Control, click OK, and apply.
</p>
<br />

<p>
<img 21>
</p>
<p>
Go back to osTicket and continue the installation. 
</p>
<br />

<p>
<img 22>
</p>
<p>
Name the Helpdesk any generic name and any generic default email. Admin user name and password need to be remembered for future projects.
</p>
<br />

<p>
<img 23>
</p>
<p>
Install HeidiSQL
</p>
<br />

<p>
<img 24>
</p>
<p>
Connect and set up a database for osTicket, and click New.
</p>
<br />

<p>
<img 25>
</p>
<p>
Enter the user name and password as “root”. User name and password need to be remembered for future projects. 
</p>
<br />

<p>
<img 26>
</p>
<p>
Create a database called osTicket by right-clicking the unnamed database•create new→database.
</p>
<br />

<p>
<img 27>
</p>
<p>
Name it osTicket and click OK
</p>
<br />

<p>
<img 28>
</p>
<p>
Go back to the osTicket browser and enter the database settings—MySQL Database:osTicket MySQL Database: root, MySQL Password: root. 
This was the final step for installing osTicket. Next lab will be setting up users in osTicket.
</p>
<br />




