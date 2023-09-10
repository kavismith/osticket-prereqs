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
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
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

<h2>Actions and Observations</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5636d95b-3db9-44ab-836a-e19ed80cadf9)

</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>

<h2>Actions and Observations</h2>

![image](https://github.com/kavismith/osticket-prereqs/assets/143667203/5636d95b-3db9-44ab-836a-e19ed80cadf9)

</p>
<p>
Go to Whatismyipaddress.com to see what your personal computers IPv4 address is. Take note of this. 
</p>
<br />
