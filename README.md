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

- Create a Virtual Machine in Azure
  1. Create a resource group and create a windows 10 Virtual Machine
- Install and Enable Internet Information Services(IIS) 
  1. with CGI and Common HTTP features
- Install PHP Manager for IIS
- Install Rewrite Module
- Install PHP 7.3.8
- Install MySQL 5.5.62
- Install osTicket v1.15.8
- Install HeidiSQL

<h2>Create a Resource Group and Virtual Machine</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/110eb958-21a5-4cf1-ad27-df2d55c4117a) 

Search for "resource groups" in the Azure Portal and create a new resource group specifically for your osTicket deployment. 

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/6225e3fb-22db-4744-9587-114be8049fea)

Start by searching for "Virtual Machine" in the Azure Portal. Select your subscription and the newly created resource group.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/2e3fe46c-9fdb-4655-a609-e06b2be25e9f)

In the instance details section, provide the following information:
- Set your desired Virtual Machine Name.
- Choose a region for your Virtual Machine.
- Change the image to "Windows 10 Pro" to use this operating system.
- Select a suitable size for your Virtual Machine, with 2-4 vCPUs to ensure optimal performance.
- Create a username and password that you can easily remember; you will use these credentials to sign in to your remote desktop.
- Make sure to check the licensing box for Windows 10/11 to ensure proper licensing for your operating system.

By following these steps, you will have configured the necessary settings for your osTicket environment in Azure, including setting up a suitable Virtual Machine with the specified operating system and resources.
</p>
<p>
</p>
<br />

<h2>Log into Remote Desktop</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/0a9d14dd-b9ae-402c-9602-f6a8ffc7c2e0)

Search for "Virtual Machine" in the search bar within the Azure Portal and copy your VM's public IP address.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5126c3c5-2410-4120-ad22-274c8b84a049)

On your local computer, search for "Remote Desktop" and paste your VM's IPv4 address into the computer section, then press "Connect." A login box will appear; click on "Use a different account" and sign in using the username and password you created when setting up your Virtual Machine.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7e24bd23-21a8-4862-89eb-1f9df0bf649d)

After successfully logging in, you will be greeted with the remote desktop welcome screen.

</p>
<p>
</p>
<br />

<h2>Download Your Files & Access IIS Features</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/3b86ed80-8cf2-4d5b-81a1-b5916ebe8bd0)

In this section, download all the necessary files required for a proper osTicket installation.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/6a292035-0f81-48d7-8739-d3bc203f7827)

Search for "Control Panel" in your Windows operating system and click on it. Within the Control Panel, locate and click on "Programs."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/22789a54-6c93-4877-8162-6bedb3390dfa)

From the Programs section, select "Turn Windows features on or off."
</p>
<p>

</p>
<br />

<h2>Enable IIS Features</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1064037a-ef0c-4726-91e2-f1ede6e8b6e7)

Click on the "Internet Information Services" box to ensure it is checked (blackened). Then, click on "World Wide Web Services."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/67a09350-57f1-4678-a1d0-681fb63fc146)

Within the "World Wide Web Services" section, click on the "Application Development Features" drop-down and check the boxes for "CGI" and "Common HTTP Features."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/be0e7553-78fe-46b3-85b0-c91ed0ea7f28)

After selecting these features, click "OK" and wait for the changes to be applied.


</p>
<p>

</p>
<br />

<h2>Download PHP Manager</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/8fc8c4b0-9a91-46ff-b533-b2342ddaf089)

</p>
<p>
Download PHP Manager and ensure that you accept all the terms and conditions during the installation process. If the installation encounters any issues, go back to the Windows Features panel and verify that the IIS (Internet Information Services) feature is enabled. After confirming the IIS feature is enabled, attempt to install PHP Manager again.
</p>
<br />

<h2>Download Rewrite_amd64_en-US</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1ecbe895-c4fa-4315-bb7b-88d14d24ed7d)

</p>
<p>
Download the "Rewrite_amd64_en-US" package and make sure to accept all the terms and conditions during the installation process.
</p>
<br />

<h2>Create PHP Folder </h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/95e5f68a-390d-417a-851c-ffb5dbbbac02)

</p>
<p>
Open File Explorer, click on "This PC," then select the "Windows C" drive. Right-click on an empty space within the drive, choose "New," and then select "Folder." Finally, name the newly created folder as "PHP."
</p>
<br />

<h2>Download PHP-7.3.8 file</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/dd634c81-4284-42d9-bf7a-4f30d49dcc50)

After you have downloaded the PHP-7.3.8 file, right-click on it and select "Extract All."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/2b222a1b-41ef-42ba-b614-7a5eca41a5fe)

Browse to locate the folder you created earlier, named "PHP," and select it. Then, click "Extract" to unzip the contents into the "PHP" folder.
</p>
<p>

</p>
<br />

<h2>Download VC-redist.x86.exe </h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/0873adea-1cad-43fa-b2db-f70b00e3827a)

</p>
<p>
Download and install the file named "VC_redist.x86.exe," and be sure to accept all the terms and conditions during the installation process.
</p>
<br />

<h2>Download MySQL & Creat MSQL Password</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7c71ccfe-5c31-40f9-be9e-c3c578b55b48)

Download and install MySQL version 5.5.62.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/a9894a87-258e-42aa-b35e-8e529560d691)

During the installation process, select the "Typical" option to install the most common features

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/0a635f97-0990-4006-b9d6-c036cb7d1c7c)

Choose the standard configuration

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/70c0a8d2-e344-4304-9f68-635deb4255f8)

Set up your password for root login

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5989272a-6c2e-4f22-b203-4183f370597e)

And finally, click "Execute" to proceed with the installation.
</p>
<p>
</p>


<h2>Open IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/8f1144c4-6b3a-404d-a17c-545235cd9345)

</p>
<p>
Open the Internet Information Services Manager (IIS) as an administrator.
</p>

<h2>Register PHP from within IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5b760977-78f2-4549-a4eb-278e0e7ee83d)

Once the Internet Information Services (IIS) Manager is open, double-click on "PHP," then click on "Register new PHP."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/09e34002-e414-4f99-8bd3-dce6b2b0e14a)

Browse to the C drive, navigate to the "PHP" folder, select the "php-cgi" executable, and press "OK."

</p>
<p>
</p>

<h2>Reload IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1e19f3c9-1fdb-464b-978f-ab5668c77c8e)
</p>
<p>
Restart the server by clicking on vm-osticket to your left and then to your right select restart
</p>

<h2>Install osTicket v1.15.8</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/75732403-b436-41bb-b2d6-542a5decf5c2)

Download the osTicket installation files. Open two folders in Windows Explorer.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/48cd4bcb-eec3-4f35-8a39-cc03cf297bd1)

In one folder, navigate to "This PC" and select the C drive. Inside the other folder, open the osTicket folder. 

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/b60b59ca-e725-46fd-8b3c-f5a00af6e217)

Drag the "upload" folder from the osTicket folder to the "wwwroot" folder within the C drive's "inetpub" directory.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/e44b7680-6643-46a4-ac42-a6fd7d1c1c9c)

Finally, rename the "upload" folder by right-clicking it and selecting "Rename."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/a4d835a6-3c17-4827-bc11-362b6116f18d)

</p>
<p>

</p>


<h2>Restart IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/25baf2b2-f33d-4f95-88c7-08a001b86804)


</p>
<p>
To reset IIS, you can either click on "Restart" to the right or choose to stop it first and then start it again.  
</p>

<h2>Click on "Browse*:80"</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1777d6b8-96a8-4220-a2ce-a5afbf617ca5)

To access the osTicket installer, navigate to the left in the "Connections" section, go to "Sites," select "Default," and click on "osTicket." Then, on the right, you'll see the "Browse" section; click on "Browse*:80(http)."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/45497ef9-5526-4844-ab55-26ba53d7cd39)

This action will open the osTicket Installer in your web browser, where you'll be able to view the prerequisites and recommended features.

</p>
<p>
</p>

<h2>Enable PHP features for osTicket instillation </h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/f94959c6-4f0e-4d91-823e-392901617ea8)

To enable the necessary PHP extensions for osTicket to run smoothly, you should open IIS (Internet Information Services), then access PHP. Once in the PHP settings, click on "Enable and Disable Extensions."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1b7a967f-03c7-4e9e-964a-c2ff366e0977)

To ensure the smooth operation of osTicket, the "php_imap.dll" extension needs to be enabled.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/268060a7-d59a-4a4f-aa15-60b08d476343)

Additionally, there are two other extensions that require enabling: "php_intl.dll" and "php_opcache.dll."
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/4151115b-dc04-4938-8611-6989aac77f02)

After enabling all these extensions, refresh the osTicket browser, and you will notice that the extensions we just enabled will change from red "X"s to green checkmarks.

</p>
<p>
</p>

<h2>Rename ost-sampleconfig</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/3e9ab952-2e21-4444-ab61-c3117bb78c9c)

Open File Explorer and navigate to "This PC." Click on the "Windows C" drive. Navigate further to "inetpub," "wwwroot," and then "osTicket." Locate the "include" folder within the osTicket directory. Scroll down to find the file named "ost-sampleconfig.php." Right-click on "ost-sampleconfig.php" and select "Rename."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/6ef37dc1-9a4a-4312-9db8-4a664c2f269c)

Now, rename the file to "ostconfig.php."
</p>
<p>

</p>

<h2>Assignn Permission: ost-config.php</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/d252f2a3-059b-4a42-846b-65f6ad40793e)

Right-click on the "ostconfig.php" file and select "Properties." In the Properties window, go to the "Advanced" tab.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/15ada31a-e450-415a-b100-e103e20d2c43)

Click on "Disable inheritance."

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/e50f6d4e-57a0-4f34-b46a-1b1d6c49a1e0)

Next, select "Add a principal" and type in "Everyone" to provide permission to everyone. Click "OK" to confirm the "Everyone" permission.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/dfbecf00-7682-458a-bbab-6bd44a21055b)

In the "Basic permissions" section, check the box for "Full control." Finally, click "OK" to apply the changes and grant full control permission to the "ostconfig.php" file for everyone.

</p>
<p> 
</p>

<h2>Continue setting Up osTicket in the browser(click) continue</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/2f1b212c-e176-46d3-a215-70f2a4308535)


</p>
<p>
Set up your system settings by adding the helpdesk URL, name, and a default email address. Additionally, configure your admin user settings, including the first and last name, email address, username, and password.
</p>


<h2>Download HeidiSQL</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/eb4b68d6-c19e-4fe4-9469-5907d315303d)

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/8191a1a8-9fd4-4a6c-8346-64f748e43153)

Download HeidiSQL 

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/66d19d73-ef37-4bae-a534-c8548acd6ef0)

Create a new database by right-clicking on "unnamed," selecting "Create," then clicking on "Database,".

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7c4eb2a5-638d-4657-978b-b5e9c8d24d3d)

Finally, naming the database as "osTicket."

</p>
<p>   
</p>

<h2>Set up Database Settings on osTicket</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/75f38ffe-f2d9-42ef-94e3-00ba4cec1f1e)

Set up the MySQL information within the osTicket installer. Use the username "root" and the password obtained during the MySQL download. Enter the database name as "osTicket,".

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/91e1633f-ff00-499d-8b8e-5147617a986a)

Finally, click "Install Now" to proceed with the installation.

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/9e7b2ea6-cc00-4cb9-b0c1-e66670f948f7)

</p>
<p>

</p>
