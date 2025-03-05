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

- Download and Unzip os Ticket Installation files (Can be found online).
  ![image](https://github.com/user-attachments/assets/3027f0fb-902c-4a45-999e-54fe51a215ce)
  Once downloaded, move the downloaded file to your desktop.
  ![image](https://github.com/user-attachments/assets/9ebad70b-3ac7-434a-9969-c6b3840e04f9)
  Right click on the file on desktop and click "extract all", click extract. This will create an unzipped version of the file on your desktop that you will use for the installation.
![image](https://github.com/user-attachments/assets/9560521c-a3fd-4529-b786-070412e1ed1a)
![image](https://github.com/user-attachments/assets/865b51e4-67fe-4ed3-9078-da32c1df2970)

<h2>IIS Install/Enable </h2>

-Go to "Start"> Control Panel> Programs> Turn Windows Features ON/OFF". A box will pop up, scroll down and select "Internet Information Services" and expand the (+) sign next to it. Click the box next to Web Management Tools, and "World Wide Web Services". Expand the (+) next to World Wide Web Services, expand (+) next to "Application Development Features", select box next to CGI. Make sure boxes next to Common HTTP Features, Health and Diagnostics, and Performance Features, and Security are all checked as shown in the image below before clicking "OK".
![image](https://github.com/user-attachments/assets/b12f17a4-1a49-4ad7-ab43-0cc3fb65dcaf)
![image](https://github.com/user-attachments/assets/c718a6a6-8583-4ad3-951e-211c1954ed54)
![image](https://github.com/user-attachments/assets/476b1ed7-034b-49d8-8d08-9cbfb56956cf)

-Test the IIS installation by typing 127.0.0.1 into your web address bar. It should display the image below.
![image](https://github.com/user-attachments/assets/e6a71c62-318e-4115-9b6c-a4096b52a3d9)

<h2>Install PHP Manager </h2>

-Open osTicket installation files, double click on PHP Manager file, click next, click agree, click install, then close/finish.
![image](https://github.com/user-attachments/assets/422d71d3-cd61-4122-8065-afe364ff0315)

<h2>Install Rewrite Module </h2>

- Open osTicket installation files, double click on rewrite_amd file , click accept, click install, then finish.
![image](https://github.com/user-attachments/assets/b65dcab1-375d-47ab-a28c-c1c8baace888)

<h2>Create PHP Folder on Windows and Unzip PHP file (C:) Drive </h2>

- Right click the folder icon, and open file explorer. CLick "This PC"> Windows (C:) drive, click the folder icon at the top left of the page and create a new folder called "PHP". 
  ![image](https://github.com/user-attachments/assets/0dceb0a9-11df-4014-9a43-26952f4a99b1)
![image](https://github.com/user-attachments/assets/3901d5eb-53a5-44e7-8350-3f97e3c9a4c5)
-Go back to os Ticket installation files find php zip file, right click on it and selcet extract all. Click browse, go to windows (C:) drive and select the PHP file you created, then click "select folder", then "extract. The files will now be extracted inside of the PHP folder.
![image](https://github.com/user-attachments/assets/917e41da-1aa5-4a82-8028-5756eaa5ec28)
![image](https://github.com/user-attachments/assets/55b7171c-e208-426e-81ac-cb6ca81b04b7)
![image](https://github.com/user-attachments/assets/f2b8ac1e-6fb9-4507-895e-46fd38a5fe47)
![image](https://github.com/user-attachments/assets/daf425c4-5b9e-48b3-bf68-30de7b91e9ab)

<h2>Install VC_redist</h2>

-Go back to os Ticket installation files find the VC_redist file, double click on it. Click agree, install, and then close.
![image](https://github.com/user-attachments/assets/41b41175-175e-4e94-b32a-aa328541f8ab)

<h2>Install MySQL</h2>

-Go back to os Ticket installation files find the MySQL file, double click on it. Click next, click agree, click next, select typical, click install, click finish. 
![image](https://github.com/user-attachments/assets/c96873cc-4070-4347-90a4-4f3e20e106a1)
![image](https://github.com/user-attachments/assets/9a4d3d1d-d64d-454a-9315-f023bcc80193)
Click next, select standard configuration, click next, enter password, then click next, then execute, and click finish.
![image](https://github.com/user-attachments/assets/613d6ca7-be84-46a4-ae9c-3d0b08bf6e3c)
![image](https://github.com/user-attachments/assets/258878c1-bbf6-4f86-b4f0-9d1a4b3ebc8f)
![image](https://github.com/user-attachments/assets/61ef76a9-f3c8-4642-908a-0dbfef8c44f8)

<h2>Register PHP</h2>

-Open IIS as an admin.
![image](https://github.com/user-attachments/assets/3c8ae687-49ad-40b1-8eae-11eb9a9b094f)
![image](https://github.com/user-attachments/assets/c1989fd6-7357-4121-b327-9c09e6a0dade)
-Click on PHP manager, select "Register New PHP Version", click on the 3 dots to browse folders, select PHP, scroll down to select PHP-CGI, click open.
![image](https://github.com/user-attachments/assets/ace8ee32-93d5-4435-8622-675c2cff32cb)
![image](https://github.com/user-attachments/assets/f28a239e-da80-453a-8457-50152548881b)
-Reload IIS (Open IIS, Stop and Start the server) then minimize the IIS screen.
![image](https://github.com/user-attachments/assets/37176cb7-e8be-48a1-a433-8086ba401aeb)

<h2>Install osTicket v1.15.8</h2>


-Open the osTicket-Installation folder, and unzip or extract the "osTicket-v1.15.8" file.
![image](https://github.com/user-attachments/assets/15f951a5-fcf5-42ef-a114-d1734b6fe10a)
-Copy the “upload” folder into “c:\inetpub\wwwroot” by opening File Explorer, select "This PC"> select "Windows C:"> select "Inetpub"> select "wwwroot". 
-Go back to the osTicket-v1.15.8 folder and drag the "Upload" file into the "wwwroot" folder.
![image](https://github.com/user-attachments/assets/7375229e-5523-45f0-af70-c9eec1d402e9)
![image](https://github.com/user-attachments/assets/cd0bfa9d-40c0-4103-bbe3-5cebc12f9a73)
![image](https://github.com/user-attachments/assets/d41a512f-10d4-4aa7-812e-31121905fada)
![image](https://github.com/user-attachments/assets/42e89a19-cf44-4a63-aa25-a2e8274f1243)
![image](https://github.com/user-attachments/assets/ce256ee1-419c-4bbe-a956-a1f7847bad75)

-Within the “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
![image](https://github.com/user-attachments/assets/5a54ee87-b5b9-4ec0-9ac3-b6bb68bdbd07)
![image](https://github.com/user-attachments/assets/58c7a13d-09b0-4f18-8337-989b7dc6c11d)


<h2>Reload IIS </h2>


-Open IIS, Stop and Start the server. 
-Go to sites -> Default -> osTicket
-On the right, click “Browse *:80”.
![image](https://github.com/user-attachments/assets/37176cb7-e8be-48a1-a433-8086ba401aeb)
![image](https://github.com/user-attachments/assets/667bb79c-a1f1-49a5-beca-32d6a02159b8)
![image](https://github.com/user-attachments/assets/dfc25d30-5067-42d9-a4e4-c82649198d11)

-Note that some extensions are not enabled. Go back to IIS, sites -> Default -> osTicket. Double-click PHP Manager. Click “Enable or disable an extension”. Enable: php_imap.dll (example below). Enable: php_intl.dll. Enable: php_opcache.dll. Refresh the osTicket site in your browser, observe the changes


![image](https://github.com/user-attachments/assets/5e2a8c77-e635-44e8-a185-6e71bd626ada)
![image](https://github.com/user-attachments/assets/c8d35c4a-ccc9-49a6-9028-29a225eca95e)
![image](https://github.com/user-attachments/assets/6ce24e24-12a7-4528-8974-393352fbef82)
![image](https://github.com/user-attachments/assets/73d585f9-4e33-4e3d-99a5-71b99bc81e01)


<h2>Rename and Configure ost-config.php</h2>


-Rename: ost-sampleconfig.php to ost-config.php. Go to File Explorer-> This PC -> Windows C:-> inetpub ->wwwroot -> osTicket -> include ->ost-sampleconfig.php. Right-click on "ost-sampleconfig.php" and click rename.
![image](https://github.com/user-attachments/assets/e99d44ef-a62e-4b20-8b43-0cca725bb3e2)
-Assign Permissions: Find the ost-config.php folder and right click ->select Properties-> Security -> Advanced -> Disable inheritance -> Remove all Permissions from this objects 

![image](https://github.com/user-attachments/assets/da126ed4-9357-49a9-b4f5-647e05de359d)
![image](https://github.com/user-attachments/assets/37b86d9e-f1a4-412e-9537-794874c4f3c5)
![image](https://github.com/user-attachments/assets/506a3ab5-34f9-468b-a534-e6f3be4dc698)
![image](https://github.com/user-attachments/assets/35f6118f-1465-48c2-a0d2-b152970e09a0)
-Add new permission
Select add -> Select a principal -> Type Everyone in the box below -> select check names and "Everyone" will become underlined -> select Ok -> select Full control -> select OK -> select apply -> Ok -> click ok on the properties box to close it out.
![image](https://github.com/user-attachments/assets/18c65e13-492b-460a-8f39-0a29e0f88102)
![image](https://github.com/user-attachments/assets/ccab97a0-4f69-44d7-9f47-75d6f97af5b4)
![image](https://github.com/user-attachments/assets/91545661-ef28-45c9-8348-c1b2185e53c8)
![image](https://github.com/user-attachments/assets/c44da8b7-7852-4ec2-9ebc-b0620081a8aa)
![image](https://github.com/user-attachments/assets/0609dc34-1766-4aed-80f6-984a9244021c)


<h2>Continue Setting up osTicket in the browser</h2>
-Click continue -> name the helpdesk -> enter the default email (receives email from customers)

![image](https://github.com/user-attachments/assets/4aebc17f-4702-4aa9-bf5e-52339a09d27e)
![image](https://github.com/user-attachments/assets/df68fa6c-692f-4986-9a98-59ccdcb47f0d)


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
