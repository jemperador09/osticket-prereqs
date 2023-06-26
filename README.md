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

<h2>Installation Steps</h2>

<p>
<b>1) Enable Internet Information Services (IIS)</b>
  
- Go into <b>Control Panel</b> and click <b>Programs</b>
  - Click "Turn Windows features on or off"
  - Under <b>World Wide Web Services</b> make sure to check the boxes shown below:
</p>
<p>
<img src="https://i.imgur.com/g4H6M9R.png" height="20%" width="20%"  alt="Disk Sanitization Steps"/><img src="https://i.imgur.com/wknP9jl.png" height="20%" width="20%"  alt="Disk Sanitization Steps"/>
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
  - Create a password
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


<br />

<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<p>
[<img src="https://i.imgur.com/DJmEXEB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>]
</p>
<br />

<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

