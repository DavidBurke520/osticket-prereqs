<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines a lab created to showcase the skills gained through the never-ending studies of Tech. This is a prerequisite for installing the open-source help desk ticketing system, osTicket.
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
<img width="1917" height="1079" alt="1" src="https://github.com/user-attachments/assets/6db86639-ad8b-46f2-a6b5-cc9f69869906" />
</p>
<p>
Download and install osTicket. Right-click and extract all of the files from the zip file onto the desktop
Install/Enable IIS in Windows with CGI, the web server on which osTicket will run, turning the PC into a web server. Go to Control Panel→Programs→Programs & Features→Turn Windows features on or off. Select and expand the following boxes→Internet Information Serveices→World Wide Web Services→Application Development Features→CGI. Click OK.
</p>
<br />

<p>
<img width="1913" height="1074" alt="2" src="https://github.com/user-attachments/assets/75cd8981-76dc-43d3-8bef-ff185b431640" />
</p>
<p>
The next step is to install the PHP Manager for IIS. PHP is a backend web server language that osTicket uses. Open the osTicket file that was unzipped earlier. Double-click and install PHPManagerForIIS_V1.5.0.
</p>
<br />

<p>
<img width="1912" height="1076" alt="3" src="https://github.com/user-attachments/assets/61edd222-89af-4e24-90d9-147c10af8c83" />
</p>
<p>
Install rewrite, open rewrite_amd64_en-US file. Accept the terms in the License Agreement and install.
</p>
<br />

<p>
<img width="1917" height="1078" alt="4" src="https://github.com/user-attachments/assets/4cf4ead9-7535-4e65-a0b3-7b51ee9b8fe3" />
</p>
<p>
Create a folder named PHP on the C: Drive. Right-click and extract all the PHP-7.3.8-nts-Win-VC15-x86 into the new C: Drive.
</p>
<br />

<p>
<img width="1912" height="1079" alt="5" src="https://github.com/user-attachments/assets/b84b7c88-6585-48b3-ad9a-d310cfe90e68" />
</p>
<p>
Open the CV_redist.x86 file and install.
Open and install the Mysql-5.5.62-win32, select typical setup, standard config, create user username ROOT and password ROOT, select execute.
</p>
<br />

<p>
<img width="1913" height="1079" alt="6" src="https://github.com/user-attachments/assets/81212846-79bd-471a-934d-050ec1fd74f3" />
</p>
<p>
Open ISS as an admin. Search for Internet Information Services, Right-click, and run as admin.
</p>
<br />

<p>
<img width="1919" height="1079" alt="7" src="https://github.com/user-attachments/assets/71bbe7c5-4ac1-48b3-bc78-182c94738681" />
</p>
<p>
Register PHP from within ISS by opening PHP
</p>
<br />

<p>
<img width="1919" height="1079" alt="8" src="https://github.com/user-attachments/assets/7dfadbe0-60a6-4c17-920b-4ac307a20a0c" />
</p>
<p>
Click the register PHP version. Browse by clicking the three dots and selecting C:\PHP\php-cgi.exe.
</p>
<br />

<p>
<img width="1915" height="1079" alt="9" src="https://github.com/user-attachments/assets/516c1c44-3b20-4362-b9a5-70c87f39c8dc" />
</p>
<p>
Reload ISS by stopping and starting the server.
</p>
<br />

<p>
<img width="1916" height="1079" alt="11" src="https://github.com/user-attachments/assets/768cb4cb-6999-427f-bf8d-aa9ac6aef337" />
</p>
<p>
Install osTicket v1.15.8. From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, rename “upload” to “osTicket”
</p>
<br />

<p>
<img width="1915" height="1079" alt="9" src="https://github.com/user-attachments/assets/a5e05a1c-058b-4d76-8858-14b5f0d3189a" />
</p>
<p>
Reload ISS by stopping and starting the server.
</p>
<br />

<p>
<img width="1910" height="1079" alt="12" src="https://github.com/user-attachments/assets/a1195fc8-a922-4510-994b-910b5630ab03" />
</p>
<p>
Load the osTicket website, go to sites→Default→osTicket. On the right, click “Browse*:80 (http)”
</p>
<br />

<p>
<img width="474" height="525" alt="13" src="https://github.com/user-attachments/assets/b76ed48a-6808-40b6-b06b-c1d4aeb93a1c" />
</p>
<p>
Note the extensions that need to be installed.
</p>
<br />

<p>
<img width="1919" height="1079" alt="14" src="https://github.com/user-attachments/assets/4d7e4cc6-e375-49fc-8553-007bb0ca66a6" />
</p>
<p>
Go back to ISS manager and select Sites→Default→osTicket. Double-click PGP Manager
</p>
<br />

<p>
<img width="1424" height="752" alt="15" src="https://github.com/user-attachments/assets/3c7a1317-1d16-457c-bf48-f2e9dff2b379" />
</p>
<p>
Scroll through the options and enable: php_imap.dll, php_intl.dll, and php_opcache.dll.
</p>
<br />

<p>
<img width="1916" height="1079" alt="16" src="https://github.com/user-attachments/assets/48d05ec6-485a-4906-81c7-4ba9408d49f1" />
</p>
<p>
Refresh the osTicket installer.
</p>
<br />

<p>
<img width="1918" height="1076" alt="17" src="https://github.com/user-attachments/assets/63aff653-27ac-4990-86a8-d3309dd1046e" />
</p>
<p>
Rename: “ost-sampleconfig.php” to “ost-config.php.” Open file explorer→C: drive→inetpub→wwwroot→osTicket→include. Find and rename ost-sampleconfig.php to ost-config.php.
</p>
<br />

<p>
<img width="2552" height="1436" alt="18" src="https://github.com/user-attachments/assets/50a6e2d3-1acd-4a8d-b200-7e43eb0c4765" />
</p>
<p>
Assign osTicket permissions to modify the config file. Right-click ost-config.php→properties→security→advanced→disable inheritance→remove all permissions. 
</p>
<br />

<p>
<img width="1919" height="1079" alt="19" src="https://github.com/user-attachments/assets/24c13535-1eec-4b9b-a7da-9062b2a1251a" />
</p>
<p>
Add new permissions, click add, type “everyone”, and select OK. 
</p>
<br />

<p>
<img width="1919" height="1079" alt="20" src="https://github.com/user-attachments/assets/ff07793f-6d2b-470b-9c82-241d01f44769" />
</p>
<p>
Select Full Control, click OK, and apply.
</p>
<br />

<p>
<img width="1915" height="1079" alt="21" src="https://github.com/user-attachments/assets/b8ac1a58-3fba-4a10-bfab-aca4bfbc831c" />
</p>
<p>
Go back to osTicket and continue the installation. 
</p>
<br />

<p>
<img width="1918" height="1078" alt="22" src="https://github.com/user-attachments/assets/cdb3682a-16d8-4b47-a4f7-a0020ba1ae90" />
</p>
<p>
Name the Helpdesk any generic name and any generic default email. Admin user name and password need to be remembered for future projects.
</p>
<br />

<p>
<img width="1913" height="1076" alt="23" src="https://github.com/user-attachments/assets/42928aaf-19bd-4fb7-adce-7e12d574e5d2" />
</p>
<p>
Install HeidiSQL
</p>
<br />

<p>
<img width="1917" height="1077" alt="24" src="https://github.com/user-attachments/assets/0f072455-e87f-4409-baf7-802b83dc40ff" />
</p>
<p>
Connect and set up a database for osTicket, and click New.
</p>
<br />

<p>
<img width="1911" height="1079" alt="25" src="https://github.com/user-attachments/assets/f4e5d3da-c2a1-42b4-8b93-0432b8147f48" />
</p>
<p>
Enter the user name and password as “root”. User name and password need to be remembered for future projects. 
</p>
<br />

<p>
<img width="1916" height="1078" alt="26" src="https://github.com/user-attachments/assets/008f071e-6eed-4f56-b577-032de21933cb" />
</p>
<p>
Create a database called osTicket by right-clicking the unnamed database•create new→database.
</p>
<br />

<p>
<img width="1913" height="1079" alt="27" src="https://github.com/user-attachments/assets/eeda866e-826f-41c6-b672-8c97474cddb9" />
</p>
<p>
Name it osTicket and click OK
</p>
<br />

<p>
<img width="1919" height="1079" alt="28" src="https://github.com/user-attachments/assets/d281bb95-c994-4abf-9fde-cd69f7e950c4" />
</p>
<p>
Go back to the osTicket browser and enter the database settings—MySQL Database:osTicket MySQL Database: root, MySQL Password: root. 
This was the final step for installing osTicket. The next lab will be setting up users in osTicket.
</p>
<br />




