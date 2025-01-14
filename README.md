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

<h2>Prerequisites</h2>

- Log in to your Azure account, it will take you to the homepage.
  ![image](https://github.com/user-attachments/assets/4658959f-388e-4c97-84f4-e1d323393b68)
  Click on Resource Group, click create, name your Resource Group, select a region or use the default, and click on "review and create" at the bottom of the screen.
![image](https://github.com/user-attachments/assets/91b5979c-7b81-44f0-bcef-d8bd11d5b2c4)
If validation passes, click create at the bottom of screen.
![image](https://github.com/user-attachments/assets/4d91db54-d29b-472d-ab3a-885a66ce24a4)
Click "Home" and then "Virtual Machine", click create, then select "Azure Virtual Machine".
![image](https://github.com/user-attachments/assets/6d3d0f2d-1e0d-44c0-b9c9-58ee6d4cf046)
Select the Resource Group you created, name your Virtual Machine, select an available zone, select an image (operating system or server).
![image](https://github.com/user-attachments/assets/6dbb5228-7baf-4e02-b8e6-be79c9ba780c)
Select a Vcpu (recommend 2 more for faster speeds), create username and password, click the check box at the bottom left, click next until you get to the "review and create" tab, click "review and create".
![image](https://github.com/user-attachments/assets/1ba1bef7-3f58-4dfd-be6e-60e44bf72927)
If validation passes, click "create".
![image](https://github.com/user-attachments/assets/6c7662b3-3362-4992-aac0-33730177a9e4)
Wait for successful deployment of your Virtual Machine, then click "Home > Virtual Machine".
![image](https://github.com/user-attachments/assets/da969b47-d94f-49c2-a095-1ab0370cdd87)
<h2>Connect VM to RDP</h2>

-Your VM should be listed under the VM tab. Scroll right to find the IP address for your VM, and copy it.
![image](https://github.com/user-attachments/assets/d2ce6de9-9786-4764-9a46-186367a1d6b7)
Open Remote Desktop and paste your VM's IP Address in the box that says "Computer" and enter the username you created for your VM the click "Connect", enter your password the click "OK".
![image](https://github.com/user-attachments/assets/d3f1937f-6f52-444f-8db8-28234c70cb42)
![image](https://github.com/user-attachments/assets/5ef55f91-f143-4105-a596-84f4948f9456)
Click "Yes", you will now be remotely logged into the VM you just created.
![image](https://github.com/user-attachments/assets/338ad9f6-b47a-43fd-9991-9a761fb1db73)
![image](https://github.com/user-attachments/assets/1ed26a1b-4846-4a11-ac90-f0023b3e7cd9)
<h2>osTicket Installation File Download</h2>

- Download and Unzip os Ticket Installation files (Can be found online)
  ![image](https://github.com/user-attachments/assets/3027f0fb-902c-4a45-999e-54fe51a215ce)
  ![image](https://github.com/user-attachments/assets/9ebad70b-3ac7-434a-9969-c6b3840e04f9)
![image](https://github.com/user-attachments/assets/9560521c-a3fd-4529-b786-070412e1ed1a)
![image](https://github.com/user-attachments/assets/865b51e4-67fe-4ed3-9078-da32c1df2970)

<h2>IIS Install/Enable </h2>

-Go to "Start"> Control Panel> Programs> Turn Windows Features ON/OFF". A box will pop up, scroll down and select "Internet Information Services" and expand the (+) sign next to it. Click the box next to Web Management Tools, and "World Wide Web Services". Expand the (+) next to World Wide Web Services, expand (+) next to "Application Development Features", select box next to CGI. Make sure boxes next to Common HTTP Features, Health and Diagnostics, and Performance Features, and Security are all checked as shown in the image below before clicking "OK".
![image](https://github.com/user-attachments/assets/b12f17a4-1a49-4ad7-ab43-0cc3fb65dcaf)
![image](https://github.com/user-attachments/assets/c718a6a6-8583-4ad3-951e-211c1954ed54)

![image](https://github.com/user-attachments/assets/476b1ed7-034b-49d8-8d08-9cbfb56956cf)
![image](https://github.com/user-attachments/assets/e6a71c62-318e-4115-9b6c-a4096b52a3d9)
Install PHP Manager
![image](https://github.com/user-attachments/assets/422d71d3-cd61-4122-8065-afe364ff0315)

- Rewrite Module
  ![image](https://github.com/user-attachments/assets/cfbfaa14-328d-46ad-afd4-36c8e527813b)

- Create "PHP" Folder on C:\ drive
- 
- PHP Unzip in PHP Folder, PHP Manager
- VC_redist
- MySQL
- HeidiSQL
- osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
