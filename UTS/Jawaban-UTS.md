# UTS System Administrasi Server
#### Bryan pratma Putra (1202190037)

### Objectives
- [Instalasi windows server 2022](https://github.com/bryanpratama/Sistem-Administrasi-Server/blob/Progress-UTS2/UTS/Jawaban-UTS.md#instalasi-windows-server-2022)
- [Instalasi Active Directory Domain Services](https://github.com/bryanpratama/Sistem-Administrasi-Server/blob/Progress-UTS2/UTS/Jawaban-UTS.md#instalasi-active-directory-domain-services)
- [Instalasi DNS server](https://github.com/bryanpratama/Sistem-Administrasi-Server/blob/Progress-UTS2/UTS/Jawaban-UTS.md#Instalasi-DNS-server)
- [Instalasi Net Framework 3.5](https://github.com/bryanpratama/Sistem-Administrasi-Server/blob/Progress-UTS2/UTS/Jawaban-UTS.md#instalasi-net-framework-35)
- [Promote Server to a Domain Controller](https://github.com/bryanpratama/Sistem-Administrasi-Server/blob/Progress-UTS2/UTS/Jawaban-UTS.md#Promote-Server-to-a-Domain-Controller)
------

* ## Instalasi Windows Server 2022
  Required :
  + File ISO [Windows Server 2022](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022)
  + Snack :cake: :beers:
  
  Lauch Virtual Box and Click button NEW
  
  ![1](Assets/Instalasi-windows-server-2022/tombol-new.png)
  
  Create Virtual Machine, Enter the name of machine, machine location , type, and version use ```windows 2019```
  
  ![2](Assets/Instalasi-windows-server-2022/name-operating-system.png)
  
  then install as usual
  
  Click VM and go to setting, at network changes attached to ```Bridged Adapter```
  
  ![2](Assets/Instalasi-windows-server-2022/network-bridged-adapter.png)
  
  Start VM, you will see a pop up Select start-up disk, add the previously downloaded iso file
  
  ![2](Assets/Instalasi-windows-server-2022/add-iso.png)
  
  Setting language, time and country, click Next
  
  ![2](Assets/Instalasi-windows-server-2022/set-language.png)
  
  Click Install now
  
  ![2](Assets/Instalasi-windows-server-2022/install.png)
  
  Select the Operating system you want to install , i am select ```Windows Server 2022 Standard Evaluation``` with ```Desktop experience```, click next
  
  ![2](Assets/Instalasi-windows-server-2022/desktop-expreience.png)
  
  Accept Applicable notices and License terms, click next <p></p>
  In which type of installation use ```Custom``` , click next</p>
  
  ![2](Assets/Instalasi-windows-server-2022/type-installation.png)
  
  Partition location just click Next
  
  ![2](Assets/Instalasi-windows-server-2022/partisi-location.png)
  
  waiting for installation, it takes 10 - 30 minutes, get out your snack and relax a bit :cake: :beers:
  
  ![2](Assets/Instalasi-windows-server-2022/installing-oprating-system.png)
  
  After installation conplete, Enter the Customize settings. and click finish
  
  ![2](Assets/Instalasi-windows-server-2022/administrator.png)
  
  On top click ``` input ``` > ```keyboard``` select ```Insert Ctrl+Alt+Del``` now you can insert password
  
  ![2](Assets/Instalasi-windows-server-2022/login.png)
  
  If you see pop up click ```X``` and minimize Server manager
  
  ![2](Assets/Instalasi-windows-server-2022/server-manager.png)
  
  On top click ```Devices``` > ```Insert Guest Additions CD images```
  
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/new-insert-guest-additional.png)
  
  Go to ```Document``` > ```CD Drive``` select application ```VBoxWindowsAdditions```
  
  ![2](Assets/Instalasi-windows-server-2022/cd-vbox-additons.png)
  
  Just click Next, Next, install and Finish, VM will reboot <p></p>
  Type in search ```winver``` for check Windows Server 2022 is complete to install
  
  ![2](Assets/Instalasi-windows-server-2022/run-winver.png)
  
  
  ![2](Assets/Instalasi-windows-server-2022/about-windows.png)
  
  ### Congratulation ! 	:tada:
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
------
* ## Instalasi Active Directory Domain Services
  Enter into Server Manager, if you not see anything aftar login windows clik widows button and you can see Server Manager
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/open-server-manager.png)
  
  In dasboard click ```Add roles and features```
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/add-roles-andreatures.png)
  
  In ```Before you begin``` just clik next
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/berofe-you-begin.png)
  
  Select installation type ```Role-based or feature-based installation``` click next
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/select-install-type.png)
  
  Select destination server
  Choose ```Select a server from the server pool```
  Server Pool select your pc names
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/select-destination.png)
  
  if you are not sure, you can chek at your Device Sprecifications
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/check-pc-name.png)
  
  Next is Select server roles, tick ```Active Directory Domain Services```click next
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/server-roles.png)
  
  In Select features just click next
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/features.png)
  
  Active Directory Domain Services just click next
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/ad-as.png)
  
  
  Ignore warning, and Install
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/click-install.png)
  
  You need restart your VM 
  
  ![2](Assets/Instalasi-Active-Directory-Domain-Services/restart.png)
  
  ### Congratulation ! :confetti_ball:
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
------
* ## Instalasi DNS server

  do the same thing as when [Instalasi Active Directory Domain Services](https://github.com/bryanpratama/Sistem-Administrasi-Server/blob/Progress-UTS2/UTS/Jawaban-UTS.md#instalasi-active-directory-domain-services)
  but now in ```Select server roles``` tick ```DNS Server```
  
  After installation done
  ![2](Assets/Instalasi-DNS-server/Untitled.png)
  
  ### Congratulation ! :sparkles:
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
------
* ## Instalasi Net Framework 3.5


  do the same thing as when [Instalasi Active Directory Domain Services](https://github.com/bryanpratama/Sistem-Administrasi-Server/blob/Progress-UTS2/UTS/Jawaban-UTS.md#instalasi-active-directory-domain-services)
  
  but now in ```Select features``` tick ```Net Framework 3.5 Features```
  
  ![2](Assets/Instalasi-Net-Framework-3.5/untitled.png)
  
  Confirm installation selection, just click install
  
  ![2](Assets/Instalasi-Net-Framework-3.5/confirm-installation.png)
  ![2](Assets/Instalasi-Net-Framework-3.5/done.png)
  
  ### Congratulation ! :1st_place_medal:
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
------
* ## Promote Server to a Domain Controller
  Enter into Server Manager, click on flag with yellow warning, <br>
  
  and you will see a notification ```Post deployment Configuration``` click ```Promote this server to a domain controller```
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/post-deployment.png)
  
  In Deployment Configuration select ```Add a new forest``` and Root domain name : ```whatever```.local
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/deployment-configuration.png)
  
  In Domain controller options fill in password, confirm, and click next
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/domain-controller-options.png)
  
  
  Ignore warning and click next
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/dns%20option.png)
  
  Additional options fill in NetBIOS domain name :```whatever```
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/additional-options.png)
  
  Path just click next
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/paths.png)
  
  Review Option, next
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/review-options.png)
  
  In Prerequisites Check if you see green tick, juct click install
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/prerequisites-check.png)
  
  Now restart your VM
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/restart2.png)
  
  Login with new client
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/bryanadmin.png)
  
  Run CMD and use command sconfig, select ```Network settings```
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/sconfig.png)
  
  Select 1
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/network-setting.png)
  
  Select 1
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/network-adapter-setting.png)
  
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/setting-adapter.png)
  
  In network Sharing center
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/network-sharing-center.png)
  
  Open CMD use command ```netdom query fsmo```
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/cmd-netdom-query-fsmo.png)
  
  ![2](Assets/Promote-Server-to-a-Domain-Controller/before.png)


  ### Congratulation ! :trophy:
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
------
