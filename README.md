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
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
