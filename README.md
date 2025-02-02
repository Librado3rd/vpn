# Vitual Private Network (VPN)
<p align="center">
<img src="https://i.imgur.com/MntON5Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h1>VPN - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation ousing a VPN.<br />

<h2>Environments and Technologies Used</h2>

- A VPN (Proton VPN)
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>STEPS INCLUDED</h2>

- Locate Local IP
- Setting Up VM Using Azure
- Locating Current IP In The VM (Washington)
- Connecting to VPN Through VM
- Locating New IP Through VPN (Indiana)

<h2>Installation Steps</h2>

<p>
Locate Local IP
<img src="https://github.com/user-attachments/assets/d4d805c6-238a-42a2-b14e-62274688dd50" height="80%" width="100%"/>
</p>
<p>
We first need to identify our own IP address to establish a reference point and confirm whether the VPN has successfully changed it. You can do this by going to <a href="whatismyipaddress.com"> whatismyipaddress.com</a>
</p>
<br />

<p>
Setting Up VM Using Azure
<img src="https://github.com/user-attachments/assets/5ebe2f59-09e8-4785-8750-52349138738f" height="80%" width="100%"/>
</p>
<p>
Start By Accessing the Azure Portal
Open your web browser and navigate to the <a href="http://portal.azure.com">Azure Portal<a/>. Sign in with your Azure account credentials. If you are new, you get $200 as credit to play with! 
</p>
<br />

<p>
Setting Up VM Using Azure
<img src="https://github.com/user-attachments/assets/09b9f918-b2b8-45ff-b680-eb49d848decc" height="80%" width="100%"/>
</p>
<p>
Initiate the Virtual Machine Creation Process. In the Azure Portal, Click on the search bar on the top-center of the page. Search for “Virtual Machines” and click on the first service option. Click the Create dropdown and select Azure Virtual Machine
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/2209eee9-6e10-4e4f-bf7e-a5fcde269ac3" height="80%" width="100%"/>
</p>
<p>
Select your subscription from the dropdown menu. Create a new Resource Group to hold your virtual machine in, having multiple virtual machines in the same resource group allows them to communicate with each other. example name (eg., vm-test). Give your virtual machine a name (eg., vm-test-win-10). Select the Region nearest to you for optimal performance. Select an “image” this is the Operating System you would like installed in the virtual machine (eg., Windows 10 pro, Ubuntu Server, etc)
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5fac9902-00e5-4c1b-98a5-1de1985dcb1b" height="80%" width="100%"/>
</p>
<p>
Choose Virtual Machine Size. Click "See all sizes" to view available options. Select a size based on your requirements (e.g., Standard_D2s_v3 - 2vcpus, 8 GiB memory for general purpose
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/ef8b3431-4df5-415f-bf62-8873f52924e4" height="80%" width="100%"/>
</p>
<p>
Set Up Authentication. Create a username for the administrator account. (eg., vmuser). Choose either a password or SSH public key for authentication. If using a password, ensure it meets the complexity requirements (eg., Computerpass123!)
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/cf93aede-7eb1-4760-b313-5ee650dd05ac" height="80%" width="100%"/>
</p>
<p>
Configure Networking & Licensing. Allow selected inbound ports: typically RDP (3389) for Windows or SSH (22) for Linux. You can also allow HTTP (80) if you plan to host a web server. Check the “I confirm I have an eligible Windows 10/11 license with multi-tenant hosting rights.”
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/fb4da56a-03f6-4159-b824-3098f556b42e" height="80%" width="100%"/>
</p>
<p>
Review & Create. Review all the settings you've configured. Pat yourself in the back, you’ve done a great job. Click "Create" to deploy your virtual machine.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/3e56dc05-279c-4402-9eca-2caef33f92db" height="80%" width="100%"/>
</p>
<p>
Find your new Virtual Machine. In the Azure Portal, Click on the search bar on the top-center of the page. Search for “Virtual Machines” and click on the first service option.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/4f324f30-ee56-4252-9e5f-f6863ebc80e7" height="80%" width="100%"/>
</p>
<p>
Select your Virtual Machine.You will see a directory of all your virtual machines along with some critical information such as their status (whether the virtual machine is running or off) & the public IP address (which we will use to access it soon). Click on the name of the virtual machine you wish to access.  This will take you to that virtual machine’s overview pageopy your Virtual Machine’s IP Address</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/8908b5b0-e35c-4b3b-b605-ebb0d949d97f" height="80%" width="100%"/>
</p>
<p>
Look Under the Essentials Tab. You can find the IP address under the Essentials section labeled as Public IP Address
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/583eee08-00f0-40c2-a0cc-e593a4888eeb" height="80%" width="100%"/>
</p>
<p>
To access the  virtual machine we will be using the application “Remote Desktop Connection”. Open the application and type in your virtual machine’s IP address. into the computer section. Type in the Username you set when you created the virtual machine. You will then be prompted to type in the password. after which you will be connected to the virtual machine
</p>
<br />

<p>
Locating Current IP In VM (Washington)
<img src="https://github.com/user-attachments/assets/ad2489c8-e349-425b-899b-aed22b2b6fe2" height="80%" width="100%"/>
</p>
<p>
Open internet explorer and go to the website <a href="whatismyipaddress.com"> whatismyipaddress.com</a> to see your virtual machine’s IP address.
</p>
<br />

<p>
Connecting to VPN Through VM
<img src="https://github.com/user-attachments/assets/45fade4e-e8af-4364-ac51-81419dfd3307" height="80%" width="100%"/>
</p>
<p>
Using your virtual machine, go to [protonvpn.com](http://protonvpn.com) and create a free account. Once you are inside the dashboard click the Downloads section & choose the “Windows” version. On the left hand side will be a button labeled “connect” click on it to initiate the VPN</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/88e7c623-bea2-4747-9b3e-718a55bb8e87" height="80%" width="100%"/>
</p>
<p>
Your IP address has been successfully changed. ProtonVPN allows you to randomly switch to another server every minute, so you can easily update your IP address again whenever you'd like.
<br />

<p>
Locating New IP Through VPN (Indiana)
<img src="https://github.com/user-attachments/assets/fbdd95dd-3dbf-493d-9504-cc03c5a56f07" height="80%" width="100%"/>
</p>
<p>
Now, we return to <a href="whatismyipaddress.com"> whatismyipaddress.com</a>/ to verify that our IP address has changed—and it has. From this exercise, we can see that we’ve used three different IP addresses from a single local computer to connect to the internet. This concludes our tutorial!
</p>
<br />
