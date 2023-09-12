<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

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
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/6225e3fb-22db-4744-9587-114be8049fea)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/2e3fe46c-9fdb-4655-a609-e06b2be25e9f)

</p>
<p>
After your Microsoft Azure account has been created, search for resource groups  and create you a resource group for osTicket. Once your resource group is created, search for Virtual Machine. First select your subscription and resource group. For the instance details, create your Virtual Machine Name, set your region, and change your image to Wondows 10 Pro, then you want to set your size to 2-4 vcpus to make sure that your VM is running fast. Last, create you a username and passowrd taht you can rememeber to sign into your remote desktop with and make sure your check the licensing box for windows 10/11.
</p>
<br />

<h2>Log into Remote Desktop</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/0a9d14dd-b9ae-402c-9602-f6a8ffc7c2e0)

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5126c3c5-2410-4120-ad22-274c8b84a049)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7e24bd23-21a8-4862-89eb-1f9df0bf649d)

</p>
<p>
Once your resouce group and VM is created. Search for Virtual Machine in the search bar and copy your public Ip address. Then, search on your computer Remote Desktop and paste your VM IPv4 address in the colouter section; and then press connect. You will then see a login box. Click on "use a different account" and sign in using your username and password you created when you created your Virtual Machine. After you have logged im successfully your remote desktop welcome screen will appear</p>
<br />

<h2>Download Your Files & Access IIS Features</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/3b86ed80-8cf2-4d5b-81a1-b5916ebe8bd0)

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/6a292035-0f81-48d7-8739-d3bc203f7827)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/22789a54-6c93-4877-8162-6bedb3390dfa)


</p>
<p>
In this section download all files that is need to properly install osTicket. Once files are downloaded seach for control panel. Click on programs. Then select turn Windows features on or off. 
</p>
<br />

<h2>Enable IIS Features</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1064037a-ef0c-4726-91e2-f1ede6e8b6e7)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/67a09350-57f1-4678-a1d0-681fb63fc146)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/be0e7553-78fe-46b3-85b0-c91ed0ea7f28)


</p>
<p>
Once the Windows feature panel is up, click on Internet Information Services box to make sure it it black. Click on World Wide Web Services. Then, click on Application Development Feature drop down and check the CGI and Common HTTP Feature. Select ok and then wait until changes have been made.
</p>
<br />

h2>Download PHP Manager</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/8fc8c4b0-9a91-46ff-b533-b2342ddaf089)



</p>
<p>
Download PHP Manager and make sure you accept all terms and then install. If it does not install, then go back to the Windows feature and make sure ISS feature and enabled. Then try again to install PHP Manager
</p>
<br />

<h2>Download Rewrite_amd64_en-US</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1ecbe895-c4fa-4315-bb7b-88d14d24ed7d)


</p>
<p>
Download Rewirte_amd64_en-US and accept all term and then install 
</p>
<br />

<h2>Create PHP Folder </h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/95e5f68a-390d-417a-851c-ffb5dbbbac02)

</p>
<p>
Open up file explore and click on this PC, then select Windows C and right lock on the empty space. Select new and then folder, then name the new folder PHP
</p>
<br />

<h2>Download PHP-7.3.8 file</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/dd634c81-4284-42d9-bf7a-4f30d49dcc50)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/2b222a1b-41ef-42ba-b614-7a5eca41a5fe)

</p>
<p>
After you have downloaded PHP-7.3.8 file, right click and select extract all.  Browse the folder for the PHP folder you created, then select it and click extract
</p>
<br />

<h2>Download VC-redist.x86.exe </h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/0873adea-1cad-43fa-b2db-f70b00e3827a)

</p>
<p>
Download and install VC_redist.x86.exe. Make sure to accept all terms.
</p>
<br />

<h2>Download MySQL & Creat MSQL Password</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7c71ccfe-5c31-40f9-be9e-c3c578b55b48)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/a9894a87-258e-42aa-b35e-8e529560d691)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/0a635f97-0990-4006-b9d6-c036cb7d1c7c)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/70c0a8d2-e344-4304-9f68-635deb4255f8)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5989272a-6c2e-4f22-b203-4183f370597e)


</p>
<p>
  Download and install MYSQAL 5.5.62. Select Typical to instal the most common features. Select the standard configuration. Set up your password for root login. Last click execute
</p>


<h2>Open IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/8f1144c4-6b3a-404d-a17c-545235cd9345)



</p>
<p>
Open IIS (Internet Information Services Manager) as an administrator
</p>

<h2>Register PHP from within IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5b760977-78f2-4549-a4eb-278e0e7ee83d)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/09e34002-e414-4f99-8bd3-dce6b2b0e14a)




</p>
<p>
Once IIS is open, double click on PHP. Click on register new PHP. browse  and go to C drive, PHP, click on php-cgithen press ok
</p>

<h2>Reload IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1e19f3c9-1fdb-464b-978f-ab5668c77c8e)
</p>
<p>
Restart the server by clicking on vm-osticket to your left and then to your right select restart
</p>

<h2>Install osTicket v1.15.8</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/75732403-b436-41bb-b2d6-542a5decf5c2)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/48cd4bcb-eec3-4f35-8a39-cc03cf297bd1)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/b60b59ca-e725-46fd-8b3c-f5a00af6e217)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/e44b7680-6643-46a4-ac42-a6fd7d1c1c9c)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/a4d835a6-3c17-4827-bc11-362b6116f18d)



</p>
<p>

  Download OS-Ticket from the installation files. Ooen up two folders in windows explorer. Go to This pc and select windows drice C in one folder, select inetpub and then wwwroot. On the second folder open osTickek and drag the upload folder to wwwroot. Then rename the upload folder by right clicking the folder and select rename
</p>



<h2>Restart IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/25baf2b2-f33d-4f95-88c7-08a001b86804)


</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>

<h2>Click on "Brows*:80"</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1777d6b8-96a8-4220-a2ce-a5afbf617ca5)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/45497ef9-5526-4844-ab55-26ba53d7cd39)


</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>

<h2>Click on "Browse*:80"</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/f94959c6-4f0e-4d91-823e-392901617ea8)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1b7a967f-03c7-4e9e-964a-c2ff366e0977)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/268060a7-d59a-4a4f-aa15-60b08d476343)



</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
