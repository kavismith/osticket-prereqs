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
After your Microsoft Azure account has been created, search for resource groups  and crea7te you a resource group for osTicket. Once your resource group is created, search for Virtual Machine. First select your subscription and resource group. For the instance details, create your Virtual Machine Name, set your region, and change your image to Wondows 10 Pro, then you want to set your size to 2-4 vcpus to make sure that your VM is running fast. Last, create you a username and passowrd taht you can rememeber to sign into your remote desktop with and make sure your check the licensing box for windows 10/11.
</p>
<br />

<h2>Actions and Observations</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/0a9d14dd-b9ae-402c-9602-f6a8ffc7c2e0)

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5126c3c5-2410-4120-ad22-274c8b84a049)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7e24bd23-21a8-4862-89eb-1f9df0bf649d)

</p>
<p>
Once your resouce group and VM is created. Search for Virtual Machine in the search bar and copy your public Ip address. Then, search on your computer Remote Desktop and paste your VM IPv4 address in the colouter section; and then press connect. You will then see a login box. Click on "use a different account" and sign in using your username and password you created when you created your Virtual Machine. After you have logged im successfully your remote desktop welcome screen will appear</p>
<br />

<h2>Actions and Observations</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/3b86ed80-8cf2-4d5b-81a1-b5916ebe8bd0)

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/6a292035-0f81-48d7-8739-d3bc203f7827)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/22789a54-6c93-4877-8162-6bedb3390dfa)


</p>
<p>
After you are logged into your remote desktop, dowload your files to setup osTicket.  
</p>
<br />

<h2>Actions and Observations</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1064037a-ef0c-4726-91e2-f1ede6e8b6e7)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/67a09350-57f1-4678-a1d0-681fb63fc146)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/be0e7553-78fe-46b3-85b0-c91ed0ea7f28)


</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />

h2>Actions and Observations</h2>


![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/a9f52464-4be5-4cdd-b533-6bbbf3481138)

</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />

<h2>Actions and Observations</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7e8b874c-e129-4d33-af51-9cfc5064e75c)

</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />
<h2>Actions and Observations</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/261fac47-1cbe-4cdc-8a6a-38145795f2bc)
</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />

<h2>Actions and Observations</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/261fac47-1cbe-4cdc-8a6a-38145795f2bc)
</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />

<h2>Actions and Observations</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/f62d24a8-7842-47ec-959d-b7fa59fa7c4d)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/624d431f-32fd-4b15-8682-e5082b22ec93)

</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />

<h2>Actions and Observations</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5636d95b-3db9-44ab-836a-e19ed80cadf9)

</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>

<h2>Install VC_redist.x86.exe</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/c6c2c6b0-4c65-4298-966d-0288005e028a)


</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>

<h2>Install MySQL 5.5.62</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/3210073f-f4bb-4965-b93f-6fc497eed603)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/7f0edffe-dbfa-433d-8efb-8dd044f276a4)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/cefdda3d-011c-49b1-aa2c-43e676f500c2)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/936d4464-8fc0-4370-96bd-ce4ed4fcef81)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/8bab6fe5-8299-4028-bb19-3c991fae7c66)

</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />

<h2>Open IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/8f1144c4-6b3a-404d-a17c-545235cd9345)



</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>

<h2>Register PHP from within IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5b760977-78f2-4549-a4eb-278e0e7ee83d)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/09e34002-e414-4f99-8bd3-dce6b2b0e14a)




</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>

<h2>Reload IIS</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/1e19f3c9-1fdb-464b-978f-ab5668c77c8e)
</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<h2>Install osTicket v1.15.8</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/75732403-b436-41bb-b2d6-542a5decf5c2)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/48cd4bcb-eec3-4f35-8a39-cc03cf297bd1)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/b60b59ca-e725-46fd-8b3c-f5a00af6e217)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/e44b7680-6643-46a4-ac42-a6fd7d1c1c9c)
![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/a4d835a6-3c17-4827-bc11-362b6116f18d)



</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
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
