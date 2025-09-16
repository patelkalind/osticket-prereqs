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

 
After completing that activity, provide a unique username and password for the virtual machine and configure the inbound port.

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/b8fac93b-8e5d-468a-b588-cb79850b991d" />

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/543ab280-7f4f-4312-a978-c5e250d7b756" />

 
After configuring the settings, go to Review+Create and click Create.

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/4563da6e-b94b-4fde-b53b-581c1a721f54" />

 
After clicking Review+Create, please take a look at the deployment of the virtual machine.

<img width="975" height="468" alt="image" src="https://github.com/user-attachments/assets/2a3fd04b-653a-4ccc-afc7-618a773aea50" />

 
Please verify that the deployment was successful.

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

 
After you install the MySQL Server, please go ahead and launch the configuration wizard of MySQL.

<img width="975" height="744" alt="image" src="https://github.com/user-attachments/assets/e09cee87-bbf9-41a9-a4b6-e938643d105b" />

 
After clicking “Next”, go with the Standard configuration to keep things simple.

<img width="975" height="744" alt="image" src="https://github.com/user-attachments/assets/4eb95c69-9fa8-49ae-bbd8-be621dfff70f" />

 
After clicking the Standard Configuration Wizard, the next step is creating a username and password. Please note that your password and username shouldn’t be the same, as you would typically use a strong password and a unique username when accessing your ticketing system. The example below was strictly for the lab assignment created for an online course.

<img width="975" height="744" alt="image" src="https://github.com/user-attachments/assets/a3c37edf-0e72-4348-a4d2-f70522441f77" />

 
After creating the username/password for MySQL, the next step is to run IIS (Internet Information Systems) as an administrator. Go to the Start menu in the virtual machine and type in IIS and click “Run as Administrator”

<img width="975" height="845" alt="image" src="https://github.com/user-attachments/assets/037f0895-756b-4368-b9c3-540f408c8d0d" />

 
After opening IIS as an admin, the next step is to register PHP within IIS.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/7f3f9cf8-137c-40e3-ad0d-756c625b03c5" />

 
After clicking “Register new PHP version”, search for php-cgi.exe within the PHP folder on the C: drive in the VM to register it in IIS.

<img width="975" height="420" alt="image" src="https://github.com/user-attachments/assets/15f6d606-7335-4c0c-9636-985b15c461a5" />

 
After registering the new PHP within IIS, stop the server briefly. This is primarily a manual restart.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/273176c2-01ec-4766-9e73-2d3e2385329b" />

 
After clicking “Stop”, click “Start” to complete the process.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/46eb5c6b-b3cd-408b-95fe-8b044acae40a" />

 
So that you know, the next step is unzipping the osTicket installation software.

<img width="975" height="816" alt="image" src="https://github.com/user-attachments/assets/669f24f0-7258-4348-b832-13d9b9485461" />

 
After unzipping the osTicket Installation Files, the next step is to go to the C: drive. From there, go to inetpub  wwwroot. In the wwwroot folder, click the upload folder and rename it to osTicket

<img width="975" height="514" alt="image" src="https://github.com/user-attachments/assets/94ac947d-6f36-4ff8-90c1-d74abf3f35a2" />

<img width="975" height="514" alt="image" src="https://github.com/user-attachments/assets/1d086f30-0f57-47e0-bc61-e3a3ff80323b" />
 

 
Return to the IIS. Go to sites -> Default -> osTicket. On the right, click “Browse *:80”

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/d629037f-ee1f-423a-a34d-e21af9032bea" />

 
After this, launch osTicket for the first time and observe the landing page.

<img width="975" height="524" alt="image" src="https://github.com/user-attachments/assets/088eb253-3200-452b-b888-8097ae1f57b1" />

 
As you can see, some recommended extensions are not enabled in the system as of yet. So, we'll need to install these extensions to make sure osTicket runs smoothly. 


Therefore, we must return to the IIS and go to the PHP manager.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/364229a3-231e-4069-8aba-4919e5a1ecfc" />

 
Within PHP Manager, click “Enable or Disable an extension.”

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/e937fe89-65e9-4abb-a55d-adc9467342f0" />

 
Click to Enable: php_imap.dll

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/9d75c9f8-c30a-46fb-a947-50c0f72b7af8" />
 


Click to Enable: php_intl.dll

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/dd7192bb-6f94-4f41-93c7-7dc2a0710f2f" />
 


Click to Enable: php_opcache.dll

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/c71c286b-ca23-4158-b4da-3330e9e6bbad" />
 


After you enable the extensions on the PHP Manager, you can refresh the osTicket site in your browser to observe the changes.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/47d3468b-17d7-4639-937e-bfb1cdb8d690" />

 
After viewing the changes in osTicket, the next step is to rename ost-config.php
-	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

<img width="975" height="514" alt="image" src="https://github.com/user-attachments/assets/c9bf707b-7451-4c01-875c-ec14fb821a88" />
 


-	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<img width="975" height="514" alt="image" src="https://github.com/user-attachments/assets/5cc3e974-c77e-48c6-a017-65ec15198ef7" />

 
After renaming the file, what we need to do next is to "Assign Permissions" within ost-config.php. Follow these steps below:

<img width="975" height="610" alt="image" src="https://github.com/user-attachments/assets/c1644f68-7b38-45ac-b057-8611ae348f89" />
 


-	Disable inheritance -> Remove All

<img width="975" height="561" alt="image" src="https://github.com/user-attachments/assets/a61f81fe-9dc4-4aad-a4f1-bbaf35d3fc3c" />
 


After removing permissions, click Add. Followed by New Permissions -> Everyone -> All (which will be elaborated further below)

<img width="975" height="610" alt="image" src="https://github.com/user-attachments/assets/ac04ffd6-3e81-4e47-a6b9-8caa9bd666be" />

 
After that, select a principal in Permission Entry.

<img width="975" height="582" alt="image" src="https://github.com/user-attachments/assets/81796a09-aa4e-417c-ae7c-7c967b492f73" />

 
Type “Everyone” in the box. Note, this is not encouraged for real-world ticketing systems, as this is an example of a lab assignment for an online course.

<img width="950" height="483" alt="image" src="https://github.com/user-attachments/assets/e2b245f4-2e26-44b0-8a87-14f79bbee868" />

 
After granting Everyone permission, click Full Control.

<img width="975" height="582" alt="image" src="https://github.com/user-attachments/assets/58b365dd-93c9-4b12-b2a4-4dfbb2ef065f" />

 
These are now the new permissions after changing the settings.

<img width="975" height="610" alt="image" src="https://github.com/user-attachments/assets/0be9c2c8-e6bf-4be0-824f-206750a9d6f0" />

 
After changing the settings, it’s now time to return to osTicket and click “Continue” with the setup.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/e9d8a67a-f5bd-48ab-b315-0386f2b69f9c" />

 
From there, provide a name for the Helpdesk and contact information for people to email you in this simulation. In addition, create an admin user account named “adminuser” and a password of your choosing.

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/bb714ce7-3bc4-4744-aa13-a334ee13df6c" />

 
After completing those steps, return to the osTicket Installation Files folder to install HeidiSQL.

<img width="975" height="514" alt="image" src="https://github.com/user-attachments/assets/79fd4667-24c3-4639-b7ba-dc2b6fbda0a4" />

 
Begin the installation process of HeidiSQL.

<img width="975" height="797" alt="image" src="https://github.com/user-attachments/assets/06a82a50-fc9b-427d-8eda-84f0a43aa443" />

 
After installing HeidiSQL, open the program.

<img width="975" height="685" alt="image" src="https://github.com/user-attachments/assets/3f9b6a8e-673f-47df-bad8-3c484dc277b2" />

 
Please create a new session, along with a username and password. (NOTE: Passwords should be strong and long enough to be secure.) This is only an example from a lab assignment in an online course.

<img width="975" height="685" alt="image" src="https://github.com/user-attachments/assets/b6a713bd-5930-4067-9d4c-592e80869ad8" />

 
Connect to a session on HeidiSQL.

<img width="975" height="617" alt="image" src="https://github.com/user-attachments/assets/96a7f0b8-fcd4-4fff-bda9-0f7a2aeb3fea" />

 
Create a database called “osTicket”

<img width="623" height="505" alt="image" src="https://github.com/user-attachments/assets/1fae917d-19e8-41b7-82ef-54c1c870fc8a" />

 
After creating the database in HeidiSQL, return to osTicket to finish the setup for MySQL.

<img width="975" height="284" alt="image" src="https://github.com/user-attachments/assets/dfa5694d-e8b6-401e-885e-506ee8cc4e29" />

 
After inputting the information into MySQL, click Install Now and let the process play itself out.

<img width="975" height="498" alt="image" src="https://github.com/user-attachments/assets/07403256-0d5f-42c1-b6e0-01017234882d" />

 
While the installation occurs on osTicket, you may check back on HeidiSQL to see how the osTicket database looks 

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/4746344d-bc3d-42ee-bc3a-4cc4f45b0832" />

 
Congratulations! You have successfully installed osTicket within the VM. 

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/82a481a0-e56f-4d40-a454-670ec80b504f" />

 
After installing osTicket, test the page of the help desk admin

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/94af1c58-423c-43bf-bcd1-da0d3a312948" />

 
As the help desk admin, log in with your username and password. Once you do, you shall see what the page looks like 

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/bc344d0c-e4ea-4987-8935-8a0ea190dae6" />

 
After testing osTicket as a help desk admin, the next step is to test the End User page. This is where people submit their tickets if they have a computer problem of any kind

<img width="975" height="523" alt="image" src="https://github.com/user-attachments/assets/108acfeb-9339-4489-9493-1e87a7cb0864" />

 
This concludes the prerequisites and installation of the osTicket tutorial. The following tutorial will explain the “post installation lifestyle,” where the help desk administrator will assign roles for the organization to assist in resolving issues within the ticketing software.




</p>
<br />
