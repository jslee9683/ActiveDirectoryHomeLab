<h1>Active Directory Home Lab</h1>

<h2>Description</h2>
This project consists of utilizing Oracle VirtualBox to virtually install Windows Server19 and Windows 10 Pro to build a functioning Active Directory environment. Most of the settings are on default for easiest management and configuration. Setting up this lab will help develop a deeper understanding of Active Directory and networking within a Windows Environment. Please feel free to ask any questions!
<br />


<h2>Utilities Used</h2>

- <b>Virtual Machine (VM) - Oracle VirtualBox</b>
- <b>Domain Controller - Windows Server19 on Oracle VirtualBox</b>
- <b>Client1 (PC) - Windows 10 Pro on Oracle VirtualBox</b>
- <b>Server19 - Windows Server 2019 ISO</b>
- <b>Windows 10 - Windows 10 ISO</b>

<h2>Environments Used </h2>

- <b>Main System - Windows 10 Pro</b> 

<h2>Project Walk-Through:</h2>

<p align="center">
Launch Oracle VirtualBox and prepare to install Server19. I named this machine "DomCon", short for Domain Controller, and skipped unattended installation: <br/>
<img src="https://i.imgur.com/zKrpE9g.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Adjust hardware settings: I gave this machine 2GB (2048MB) of RAM and 4 processors for quciker processing. Adjust based on your system!:  <br/>
<img src="https://i.imgur.com/gzQ6VC7.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Allow Bidirectional clipboard and "drag'n'drop" for easier access from main system to VM: <br/>
<img src="https://i.imgur.com/gzwehgn.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Enable two networks: One for the public Internet:  <br/>
<img src="https://i.imgur.com/8vrkotC.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
and one for the internal network:  <br/>
<img src="https://i.imgur.com/Djz9Otc.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Once the settings are complete, run the machine:  <br/>
<img src="https://i.imgur.com/DOzuRfw.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
During the setup, select "Windows Server 2019 Standard Evolution (Desktop Experience) to utilize the GUI:  <br/>
<img src="https://i.imgur.com/dUIYiRG.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
For this lab, I used "Password1" as my default password for all password settings. DO NOT DO THIS IN AN ACTUAL ENVIORNMENT. PRACTICE SAFE PASSWORD MANAGEMENT AND INFORMATION SECURITY BEST PRACTICES!:  <br/>
<img src="https://i.imgur.com/VGGq1gR.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
To optimize the VM performance, insert VirtualBox Guest Additions. This will improve performance and allow VirtualBox to adjust the screen resolution automatically (Highly Recommend 10/10):  <br/>
<img src="https://i.imgur.com/LDOkQIM.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Double-click the Guest Additions:  <br/>
<img src="https://i.imgur.com/RpEmWnG.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Install the amd64 application:  <br/>
<img src="https://i.imgur.com/GFSGSs2.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Here is a layout of the target network diagram:  <br/>
<img src="https://i.imgur.com/cRKedy1.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Since the Domain Controller was set to have two networks (one for the public Internet and one for internal), there are two Ethernet options available:  <br/>
<img src="https://i.imgur.com/ASSZaqC.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
First Ethernet option displays an APIPA (Automatic Private IP Addressing) address (169.254.0.1 to 169.254.255.254) because DHCP has not been configured yet. This option will serve as our internal network:  <br/>
<img src="https://i.imgur.com/08DmMLQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
The second Ethernet option is connected to the Internet with a private IP address:  <br/>
<img src="https://i.imgur.com/fT3mLoW.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Renaming at least one of the networks will ease identifying:  <br/>
<img src="https://i.imgur.com/orpF3fx.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Now, time to configure the private network addressing, based on the target network diagram:  <br/>
<img src="https://i.imgur.com/OhuAuud.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Configure the IPv4 settings based on the target network diagram. The default gateway will be left blank because the Domain Controller will serve as the default gateway:  <br/>
<img src="https://i.imgur.com/M70qXQ4.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Rename the PC for easier viewing and management. Renaming will require reboot:  <br/>
<img src="https://i.imgur.com/mVtCLer.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
After reboot, let's set up the domain:  <br/>
<img src="https://i.imgur.com/tAKdXz9.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Launch the Server Manager and click on "Add roles and features":  <br/>
<img src="https://i.imgur.com/hMPVest.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Select "Active Directory Domain Services". This will install the software for Active Directory Domain Services, not set up the actual domain. As mentioned in the description of this project, I used the default settings and options for all unmentioned options and features for simplicity:  <br/>
<img src="https://i.imgur.com/s7YBi5p.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Once the installation is complete, time to set up the domain:  <br/>
<img src="https://i.imgur.com/HlwfXtU.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Click on the flag icon for post deployment configurations and select "Promote this server to a domain controller":  <br/>
<img src="https://i.imgur.com/0ezNQpA.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Select "Add a new forest" and enter in the domain of your choice:  <br/>
<img src="https://i.imgur.com/1gzRfSt.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Using the default settings, create a password and begin the deployment:  <br/>
<img src="https://i.imgur.com/8whYYlT.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Once the deployment is completed, the machine will reboot:  <br/>
<img src="https://i.imgur.com/BCTjqEO.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
After reboot, select "Active Directory Users and Computers" under "Tools":  <br/>
<img src="https://i.imgur.com/U0KNVBt.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Add an Organizational Unit:  <br/>
<img src="https://i.imgur.com/MQ7QOrs.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
This OU will be used for administrator accounts:  <br/>
<img src="https://i.imgur.com/nDFepSm.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Create a new User:  <br/>
<img src="https://i.imgur.com/rgQBsQc.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Add in the name and create a user logon name. To differentiate, I used the "a-" suffix to indicate that his user will be an admin:  <br/>
<img src="https://i.imgur.com/mR6DlXu.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Create a password. For the ease of the project, I removed the additional password options and configured the password not to expire:  <br/>
<img src="https://i.imgur.com/CXzN4wm.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Once the user is created, you must add the admin status of the account by adding member feature:  <br/>
<img src="https://i.imgur.com/OxbtaU5.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Enter in the object name "domain admin" and select "Check Names". This should give you the option of adding the "Domain Admins" group:  <br/>
<img src="https://i.imgur.com/cU44tSu.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Once adding the group, apply the changes and now, your new user should have admin privileges:  <br/>
<img src="https://i.imgur.com/CzEePhz.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Sign out of the default admin account you were working on and try signing in, using the new admin account credentials:  <br/>
<img src="https://i.imgur.com/GSrcBlU.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
After confirming the admin account, now it's time to set up the RAS (Remote Access Services) on Active Directory and the NAT (Network Address Translation):  <br/>
<img src="https://i.imgur.com/fJNgkuq.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
To install RAS in Active Directory, launch the Server Manager and select "Add roles and features":  <br/>
<img src="https://i.imgur.com/gwzgU6B.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Keeping all default settings, select Remote Access:  <br/>
<img src="https://i.imgur.com/BoyvfMJ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
For Role Services, select "Routing" and it should automatically include "DirectAccess and VPN (RAS):  <br/>
<img src="https://i.imgur.com/DHkNul9.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Finish the installation:  <br/>
<img src="https://i.imgur.com/w0bAKHL.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Now, to configure NAT, select "Routing and Remote Access" under "Tools":  <br/>
<img src="https://i.imgur.com/VTnYEHs.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Right-click the machine (DOMCON) and select "Configure and Enable Routing and Remote Access":  <br/>
<img src="https://i.imgur.com/PbZmNme.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Select NAT:  <br/>
<img src="https://i.imgur.com/hAhrJid.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
You should see your two Internet options available for the NAT Internet Connection. If the first option is blocked out and you are unable to use it, exit the Setup Wizard and open up "Routing and Remote Access" under "Tools" again. Sometimes, the Server Manager may not recognize settings immediately:  <br/>
<img src="https://i.imgur.com/1uwDhts.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Go through the default settings and once the Setup Wizard is completed, NAT should be set up and ready:  <br/>
<img src="https://i.imgur.com/Bj0MenS.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Next up is to set up the DHCP server, using the scope details from the network diagram:  <br/>
<img src="https://i.imgur.com/sEvW0f5.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Launch the Server Manager and select "Add roles and features":  <br/>
<img src="https://i.imgur.com/jZM86ri.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Select "DHCP Server" and go through the default settings:  <br/>
<img src="https://i.imgur.com/r0AVYFV.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Complete the installation:  <br/>
<img src="https://i.imgur.com/DnfMUie.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Select "DHCP" under "Tools":  <br/>
<img src="https://i.imgur.com/uy3IVHu.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Add a new scope to the DHCP IPv4 by launching the "New Scope Wizard":  <br/>
<img src="https://i.imgur.com/MIkTiGe.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Add a name of the scope. I used the scope range as the name:  <br/>
<img src="https://i.imgur.com/RzUsuQD.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Enter in the IP Address Range, based on the target network diagram:  <br/>
<img src="https://i.imgur.com/qYWjQtq.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Add the router IP address, which will serve as the default gateway:  <br/>
<img src="https://i.imgur.com/KFHly4Y.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Make sure to add the domain controller's IP address for Domain Name and DNS Servers, if not already added:  <br/>
<img src="https://i.imgur.com/JVydfg2.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Once the Setup Wizard is completed, "Authorize" the domain:  <br/>
<img src="https://i.imgur.com/qfc05uf.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
and refresh:  <br/>
<img src="https://i.imgur.com/aiRJlsw.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Now, both IPv4 and IPv6 should be marked green, indicating that the DHCP server is up and running:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Now, you will populate users using a PowerShell Script and a text file containing the list of names you would like to use. I premade the script on my main machine and copied it onto DomCon:  <br/>
<img src="https://i.imgur.com/LEoDeSi.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
I used a random name generating website to generate 1000 names and copied them onto a text file:  <br/>
<img src="https://i.imgur.com/3Xs4D7V.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Here is the PowerShell script I will be using. I have a separate project repository to detail how the script works for Active Directory, here:  <br/>
<img src="https://i.imgur.com/iYSKSaS.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Launch Windows PowerShell ISE as admin:  <br/>
<img src="https://i.imgur.com/33ImKDk.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Open the PowerShell script. If you try to run it immediately, you may run into this error message:  <br/>
<img src="https://i.imgur.com/wEFRYUX.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
To avoid this error, type in "Set-Execution Policy unrestricted" and select "Yes to All". In a normal environment, this shouild not be configured for safe handling of the environment, but for the purpose of this lab, go for it!:  <br/>
<img src="https://i.imgur.com/TfuMZSD.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Change directories to wherever you created/copied the script and text file. I had my files on my desktop so I cd'd to the Desktop. This is so that the script can properly locate the files:  <br/>
<img src="https://i.imgur.com/ubPG6WW.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Once you are prepared to run the script, begin the process and it should look something like this:  <br/>
<img src="https://github.com/jslee9683/ActiveDirectoryHomeLab/assets/139186768/1fc0298d-a7ae-461f-8292-bc0350b19f3e" height="80%" width="80%" alt="Active Directory Home Lab"/>







 
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Reboot the machine:  <br/>
<img src="https://i.imgur.com/1uFrZ4X.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
