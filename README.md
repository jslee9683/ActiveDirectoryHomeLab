<h1>Active Directory Home Lab</h1>

<h2>Description</h2>
This project consists of utilizing Oracle VirtualBox to virtually install Windows Server19 and Windows 10 Pro to build a functioning Active Directory environment. Most of the settings are on default for easiest management and configuration. Setting up this lab will help develop a deeper understanding of Active Directory and networking within a Windows Environment. Please feel free to ask any questions!
<br />


<h2>Utilities Used</h2>

- <b>Domain Controller - Windows Server19 on Oracle VirtualBox</b>
- <b>Client1 (PC) - Windows 10 Pro on Oracle VirtualBox</b>

<h2>Environments Used </h2>

- <b>Main System - Windows 10 Pro</b> 

<h2>Project Walk-Through:</h2>

<p align="center">
Launch Oracle VirtualBox and prepare to install Server19. I will name this machine "DomCon", short for Domain Controller, and skip unattended installation: <br/>
<img src="https://i.imgur.com/zKrpE9g.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Adjust hardware settings: I'm giving this machine 2GB (2048MB) of RAM and 4 processors for quciker processing. Adjust based on your system!:  <br/>
<img src="https://i.imgur.com/gzQ6VC7.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
Allow Bidirectional clipboard and "drag'n'drop" for easier access from main system to virtual machine (VM): <br/>
<img src="https://i.imgur.com/gzwehgn.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
We will enable two networks: One for the public Internet:  <br/>
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
For this lab, I will be using "Password1" as my default password for all password settings. DO NOT DO THIS IN AN ACTUAL ENVIORNMENT. PRACTICE SAFE PASSWORD MANAGEMENT AND INFORMATION SECURITY BEST PRACTICES!:  <br/>
<img src="https://i.imgur.com/VGGq1gR.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
<br />
<br />
To optimize the VM performance, I will insert VirtualBox Guest Additions. This will improve performance and allow VirtualBox to adjust the screen resolution automatically (Highly Recommend 10/10):  <br/>
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
Here is a layout of our target network diagram:  <br/>
<img src="https://i.imgur.com/cRKedy1.png" height="80%" width="80%" alt="Active Directory Home Lab"/>
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
