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

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/28101e43-a4d9-4b14-ad28-37f87ee82094" />
 
After that, provide a unique name for the Resource Group

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/f86c31f7-2cc3-4bd9-bd2e-5f861e4ca083" />
 
Once that is completed, you may view the Resource Group within the Azure Directory at any time

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/a2545967-4aa2-4dad-b49f-aadcb03c90af" />
 
After creating the Resource Group, return to the Azure Directory to create a Virtual Machine

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/72cf5215-293a-44b4-b16a-4e35e4ce41eb" />
 
Click Create, and from there, provide a name for the virtual machine and assign it to a resource group that was previously created

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/4e29acc9-8c23-42be-bbd7-c6f23d753a88" />
 
You can customize the virtual machine to fit the settings that you prefer. In this case, the VM will be imaged under Windows 10

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/bf27cfc8-f989-46aa-afe5-1797677bc5b0" />
 
After completing that activity, provide a unique username and password for the virtual machine and configure the inbound port

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/b8fac93b-8e5d-468a-b588-cb79850b991d" />

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/543ab280-7f4f-4312-a978-c5e250d7b756" />
 
After configuring the settings, go to Review+Create and click Create

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/4563da6e-b94b-4fde-b53b-581c1a721f54" />
 
After clicking Review+Create, observe the deployment of the virtual machine

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/2a3fd04b-653a-4ccc-afc7-618a773aea50" />
 
Verify to see if the deployment was successful

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/56b783fc-ce11-4f3d-932c-e9f8786b8522" />
 
After the deployment succeeds, please go ahead and log in to the Windows VM using the Remote Desktop Connection app (or equivalent) on your PC.

<b>Download osTicket Installation Files.</b>

After logging in to your VM, download the osTicket installation file as shown below:

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/16386eb5-42a3-4c78-b02b-50abc89c310e" />
 
From there, you can extract the zip file to your desktop.

<img width="975" height="816" alt="image" src="https://github.com/user-attachments/assets/9d4d23d4-c17e-436f-9651-e3033a24e112" />
 
Next, navigate to the Start Menu and select Control Panel. From there, go to Programs and “Turn Windows Features On or Off”. Next, navigate to Internet Information Services --> World Wide Web Services --> Application Development Features --> CGI. From there, you can install CGI.

<img width="975" height="281" alt="image" src="https://github.com/user-attachments/assets/92a607c2-9023-459c-9420-372c159cd0d0" />

After installing CGI, you can view the IIS by typing the virtual machine's IP address into your web browser.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/ac026c3d-b3e0-465b-ba73-f95f77e1895e" />
 
The next step is installing the PHP Manager from the osTicket Installation Files.

<img width="974" height="799" alt="image" src="https://github.com/user-attachments/assets/71916f26-5f0e-42ed-a9bc-b3c5528e48b9" />
 
After installing the PHP Manager, install the Rewrite Module from the installation files folder.

<img width="966" height="755" alt="image" src="https://github.com/user-attachments/assets/4a71ba53-d70c-45ff-b721-2e965273ca8d" />
 
After installing the previous two items, go to Windows Explorer and head to the C: folder. From there, create a PHP folder within the C: drive of the VM, as shown here:

<img width="975" height="514" alt="image" src="https://github.com/user-attachments/assets/ab21e3f8-560b-412e-b965-dda1d90884d5" />
 
After creating the PHP folder on the C: drive, return to the osTicket Installation folder and unzip the PHP zip file into the folder that was just created

<img width="975" height="816" alt="image" src="https://github.com/user-attachments/assets/b17e7877-112d-4f28-a5d5-5b4d96eca885" />
 
After unzipping the PHP zip file into the folder in the C: drive, the next step is installing Microsoft Visual C++ from the installation files folder

<img width="938" height="581" alt="image" src="https://github.com/user-attachments/assets/15c9d571-17eb-4896-9a7d-bf018f13f2ac" />
 
After installing this, the next step is installing the MySQL Server application from the installation files folder.

<img width="966" height="755" alt="image" src="https://github.com/user-attachments/assets/2c552022-1818-431b-bc8d-552b67cb25a1" />
 
After installing the MySQL Server, please go ahead and launch the configuration wizard of MySQL.

<img width="975" height="744" alt="image" src="https://github.com/user-attachments/assets/e09cee87-bbf9-41a9-a4b6-e938643d105b" />
 
After clicking “Next”, go with the Standard configuration to keep things simple.

<img width="975" height="744" alt="image" src="https://github.com/user-attachments/assets/4eb95c69-9fa8-49ae-bbd8-be621dfff70f" />
 
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
