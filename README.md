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

<h2>List of Prerequisites</h2>

- Item 1 – Create an Azure Virtual Machine Windows 10
- Item 2 – Download osTicket Installation Files
- Item 3 – Enable IIS in Windows with CGI
- Item 4 – Install Microsoft Visual C+++ from osTicket Installation Files Folder
- Item 5 – Install MySQL Server from osTicket Installation Files Folder

<h2>Installation Steps</h2>
<br>Create a Resource Group and Virtual Machine</br>
To get started with this exercise of osTicket, we must first create a Resource Group and a Virtual Machine within Azure. The very first step is to create a Resource Group by clicking Create New in the directory
 
After that, provide a unique name for the Resource Group
 
Once that is completed, you may view the Resource Group within the Azure Directory at any time
 
After creating the Resource Group, return to the Azure Directory to create a Virtual Machine
 
Click Create and from there, provide a name of the virtual machine and assign it to a resource group that was previously created
 
Customize the virtual machine to fit the settings that you prefer. In this case, the VM will be imaged under Windows 10
 
After completing that activity, provide a unique username and password for the virtual machine and configure the inbound port
 
 
After configuring the settings, go to Review+Create and click Create
 
After clicking Review+Create, observe the deployment of the virtual machine
 
Verify to see if the deployment is successful
 
After the deployment succeeded, please proceed to log in to the Windows VM using the Remote Desktop Connection app (or equivalent) on your PC.
Download osTicket Installation Files
After logging in to your VM, download the osTicket installation file as shown below
 
From there, extract the zip file onto the desktop
 
After that, go to the Start Menu and go to Control Panel. From there, go to Programs and “Turn Windows Features On or Off”. After that, click Internet Information Services  World Wide Web Services  Application Development Features  CGI. From there, you can install CGI
 
After installing CGI, you can see what the IIS looks like once you type in the IP address of the virtual machine on the web browser
 
The next step is installing the PHP Manager from the osTicket Installation Files
 
After installing the PHP Manager, install the Rewrite Module from the installation files folder
 
After installing the previous two items, go to Windows Explorer and head to the C: folder. From there, create a PHP folder within the C: drive of the VM as shown here
 
After creating the PHP folder on the C: drive, return to the osTicket Installation folder and unzip the PHP zip file onto the folder that was just created
 
After unzipping the PHP zip file onto the folder in the C: drive, the next step is installing Microsoft Visual C++ from the installation files folder
 
After installing this, the next step is installing the MySQL Server application from the installation files folder
 
After installing the MySQL Server, please proceed to launch the configuration wizard of MySQL
 
After clicking “Next”, go with the Standard configuration to keep things simple
 
After clicking the Standard Configuration Wizard, the next step is creating a username and password. Just to inform you all, the password and username shouldn’t be the same as you must have a strong password and unique username in the real world when signing into your ticketing system. The example below was strictly for the lab assignment created for an online course.
 
After creating the username/password for MySQL, the next step is to run IIS (Internet Information Systems) as an administrator. Go to the start menu in the virtual machine and type in IIS and click “Run as Administrator”
 
After opening up IIS as an admin, the next thing to do is register PHP within the IIS
 
After clicking “Register new PHP version”, be sure to search for php-cgi.exe within the PHP folder on the C: drive in the VM to register it in the IIS
 
After registering the new PHP within IIS, stop the server briefly. This is primarily a manual restart
 
After clicking “Stop”, the next thing to do is click “Start” to complete the process
 
Please note that the next step is unzipping the osTicket installation software
 
After unzipping the osTicket Installation Files, the next step is going to the C: drive. From there, go to inetpub  wwwroot. On the wwwroot folder, click the upload folder and rename it to osTicket
 
 
Return to the IIS. Go to sites -> Default -> osTicket. On the right, click “Browse *:80”
 
After this, launch osTicket for the first time and observe the landing page
 
As you can see, there are some recommended extensions that are not enabled in the system as of yet. Thus, we must install these extensions to ensure osTicket runs smooth. 
Therefore, we must return to the IIS and go to PHP manager
 
Within PHP Manager, click “Enable or Disable an extension”
 
Click to Enable: php_imap.dll
 

Click to Enable: php_intl.dll
 

Click to Enable: php_opcache.dll
 

After enabling the extensions on PHP Manager, refresh the osTicket site in your browser and observe the changes
 
After viewing the changes in osTicket, the next step is to rename ost-config.php
-	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
 

-	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
 
After renaming the file, what we need to do next is to Assign Permissions within ost-config.php. Follow these steps below:
 

-	Disable inheritance -> Remove All
 

After removing permissions, click add. Followed by New Permissions -> Everyone -> All (which will be elaborated further below)
 
After that, select a principal in Permission Entry
 
Type “Everyone” in the box. Note, this is not encouraged for real world ticketing systems as this is an example of a lab assignment for an online course
 
After granting Everyone permission, click Full Control
 
These are now the new permissions after changing the settings
 
After changing the settings, now it’s time to return to osTicket and click “Continue” with the setup
 
From there, provide a name for the Helpdesk and contact information for people to email you in this simulation. In addition, create an admin user account named “adminuser” and a password of your choosing
 
After completing those steps, return to the osTicket Installation Files folder to install HeidiSQL
 
Begin the installation process of HeidiSQL
 
After installing HeidiSQL, open the program
 
Create a new session as well as a username and password. (NOTE: passwords should be strong and long enough to be secure. This is only an example from a lab assignment in an online course)
 
Connect to a session on HeidiSQL
 
Create a database called “osTicket”
 
After creating the database in HeidiSQL, return to osTicket to finish setup for MySQL
 
After inputting the information into MySQL, click Install Now and let the process play itself out
 
While the installation occurs on osTicket, you may check back on HeidiSQL to see how the osTicket database looks 
 
Congratulations! You have successfully installed osTicket within the VM. 
 
After installing osTicket, test the page of the help desk admin
 
As the help desk admin, login with your username and password. Once you do, you shall see what the page looks like 
 
After testing out osTicket as a help desk admin, the next thing is to test out the End User page. This is where people submit their tickets if they have a computer problem of any kind
 
This concludes the prerequisites and installation of osTicket tutorial. The next tutorial will be explaining the “post installation lifestyle” where the help desk administrator will assign roles for the organization to assist in resolving issues within the ticketing software.




</p>
<br />
