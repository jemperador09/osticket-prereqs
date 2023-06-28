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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS)
- Install PHP Manager
- Install Rewrite Module
- Install Microsoft Visual C++ Redistributable
- Install MySQL 5.5.62
- Install osTicket v1.15.8

<h2>Installation Steps</h2>

<p>
<b>1) Enable Internet Information Services (IIS)</b>
  
- Go into <b>Control Panel</b> and click <b>Programs</b>
  - Click "Turn Windows features on or off"
  - Check the box for <b>Internet Information Services</b> and expand <b>World Wide Web Services</b>
    - Under <b>Application Development Features</b> check the box for <b>CGI</b>
    - Under <b>Common HTTP Features</b> make sure all boxes are checked
</p>
<p>
<img src="https://i.imgur.com/hYzZNtw.png" height="20%" width="20%"  alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/wknP9jl.png" height="20%" width="20%"  alt="Disk Sanitization Steps"/>
</p>
<p>
  
  - After, click <b>OK</b> to enable IIS
    - To test if IIS is enabled, go into a web browser and enter <b>127.0.0.1</b> into the search bar. You should get something like this:
</p>
<p>
<img src="https://i.imgur.com/Xfw48Z7.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>2) Download and install <a href="https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link">PHP Manager for IIS</a> </b>
</p>
<p>
<b>3) Download and install <a href="https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link">Rewrite Module</a> </b>
</p>
<p>
<b>4) Create the directory C:\PHP</b>
</p>

<p>
<img src="https://imgur.com/39W1hmK.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
  - Download <a href="https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link">PHP 7.3.8</a> and unzip the contents into C:\PHP
<img src="https://imgur.com/MZcnT4d.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>5) Download and install <a href="https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link">Microsoft Visual C++ Redistributable</a></b>
</p>

<p>
<b>6) Download and install <a href="https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link">MySQL 5.5.62</a></b>
  
  - Choose <b>Typical</b> setup
  - Launch Configuration Wizard (after install)
  - Choose <b>Standard</b> configuration
  - Create a password (default username given is <b>root</b>)
  - Click <b>Execute</b> to finish installation
<img src="https://i.imgur.com/vBzEZCS.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>7) Open IIS as Admin</b>
</p>
<p>
<img src="https://i.imgur.com/OsVVKtA.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>8) Register PHP from within IIS</b>

  - Click on PHP Manager
  - Register new PHP version
  - Select <b>php.cgi</b> inside of C:\PHP
</p>
<p>
<img src="https://i.imgur.com/wjXro2z.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
  - Reload IIS (Open IIS, Stop and Start the server)
</p>
<p>
<b>9) Install <a href="https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view?usp=drive_link">osTicket v1.15.8</a></b>

  - Once downloaded, extract and copy "upload" into folder <b>C:\inetpub\wwwroot</b>
<img src="https://i.imgur.com/yMXjLAH.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
  
  - Rename "uploud" to "osTicket"
<img src="https://i.imgur.com/PYWHvlm.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
  - Reload IIS (Open IIS, Stop and Start the server)
  - In IIS, go to <b>Sites</b> -> <b>Default</b> -> <b>osTicket</b>
    - On the right, click on <b>Browse *:80 (http)</b>
<img src="https://i.imgur.com/SS9vZ3z.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

- Progress on osTicket installer should pop up in a browser
      
<img src="https://i.imgur.com/RZk9qYi.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>10) Enable some extensions in IIS</b>

  - Go back to IIS, go to <b>Sites</b> -> <b>Default</b> -> <b>osTicket</b>
  - Double-click PHP Manager
  - Click "Enable or disable an extenstion"
    - Enable: php_imap.dll
    - Enable: php_intl.dll
    - Enable: php_opcache.dll

<img src="https://i.imgur.com/Dgs5TLr.png" height="20%" width="20%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/TZIpVEY.png" height="20%" width="20%" alt="Disk Sanitization Steps"/>
  - Refresh the osTicket site in your browser, observe the changes
  - Rename: <b>ost-config.php</b>
    - From: C:\inetpub\wwwroot\osTicket\include\ <b>ost-sampleconfig</b>.php
    - To: C:\inetpub\wwwroot\osTicket\include\ <b>ost-config</b>.php
<img src="https://i.imgur.com/KdaxR7G.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>

  - <b>Assign Permissions for ost-config.php</b>
    - Right click ost-config.php -> Properties -> Security -> Advanced
      - Click <b>Disable inheritance</b> -> Remove all
      - For new permissions, click Add -> Select Principal
          - Enter in "Everyone", click OK, check box for "Full Control"
<img src="https://i.imgur.com/SczfIDR.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>

<p>
<b>11) Continue Setting up osTicket in the browser (click Continue)</b>
  
  - Name Help Desk
  - Default email (receives email from customers)
</p>

<p>
<b>12) Before continuing, download and install <a href="https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe">HeidiSQL</a></b>

  - Open Heidi SQL
  - Create a new session, Username: root / Password: (pw created from MySQL)
  - Connect to session
  - Create a database called "osTicket"

<img src="https://i.imgur.com/2fZ1MJH.png" height="35%" width="35%" alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/BU2UyZe.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>13) Continue setting up osTicket on browser</b>

  - MySQL Database: osTicket
  - MySQL Username: root
  - MySQL Password: (pw created from MySQL)
  - Click “Install Now!”

<img src="https://i.imgur.com/kHckfES.png" height="35%" width="35%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>Congratulations, hopefully osTicket installed with no errors!</b>

  - Browse to your help desk login page: http://localhost/osTicket/scp/login.php
  - End Users osTicket URL: http://localhost/osTicket/
<img src="https://i.imgur.com/XkxFcjf.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
<b>*Clean up*</b>

  - Delete: C:\inetpub\wwwroot\osTicket\setup (just the "setup" folder)
  - Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
<img src="https://i.imgur.com/p4NNR2o.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<br />
