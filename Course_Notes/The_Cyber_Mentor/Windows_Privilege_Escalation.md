# References
- https://academy.tcm-sec.com/courses/enrolled/1154361
- https://github.com/Gr1mmie/Windows-Priviledge-Escalation-Resources
- Fuzzy Security
	- https://www.fuzzysecurity.com/tutorials/16.html
- Payload all the things
	- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Windows%20-%20Privilege%20Escalation.md
- Win PrivE Guide
	- https://www.absolomb.com/2018-01-26-Windows-Privilege-Escalation-Guide/
- Sushant 747 
	- https://sushant747.gitbooks.io/total-oscp-guide/content/privilege_escalation_windows.html
- Course Github
	- https://github.com/Gr1mmie/Windows-Priviledge-Escalation-Resources)
- Windows PrivEsc Checklist
	- https://book.hacktricks.xyz/windows/checklist-windows-privilege-escalation
- WinPEAS
	- https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS
- Sherlock
	- https://github.com/rasta-mouse/Sherlock
- Watson
	- https://github.com/rasta-mouse/Watson
- PowerUp
	- https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc
- JAWS
	- https://github.com/411Hall/JAWS)
- Windows Exploit Suggester
	- https://github.com/AonCyberLabs/Windows-Exploit-Suggester
- Metasploit Local Exploit Suggester
	- https://blog.rapid7.com/2015/08/11/metasploit-local-exploit-suggester-do-less-get-more/
- Seatbelt
	- https://github.com/GhostPack/Seatbelt
- SharpUp
	- https://github.com/GhostPack/SharpUp
- Windows PrivEsc Lab
	- https://tryhackme.com/room/windowsprivescarena\


# Initial Enum
## System
- systeminfo
- wmic qfe
- wmic logicaldisk
- wmic logicaldisk get caption
- wmic logicaldisk get caption, description, providername
- hostname

## User
- whoami
- whoami /priv
- whoami /groups
- net user
- net user uname 
- net localgroup
- net user administrator

## Network
- ipconfig
- ipconfig /all
- arp -a 
- arp -all
- route print
- netstat -ano

## Password
- findstr /si 
- findstr /si password *.txt *.ini *.config

## FW & AV Enum
- windefend
- sc queryex type= service
- netsh advfirewall firewall dump
- netsh firewall show state
- netsh firewall show config
- sc query windefend

## Enum Tools
- winPEAS.exe
- Seatbelt.exe
- Watson.exe
- SharpUp.exe
- Sherlock.ps1
- PowerUp.ps1
- jaws-enum.ps1
- windows-exploit-suggestor.py



## Kernel Exploits
- https://github.com/SecWiki/windows-kernel-exploits
- kernel is core of OS

  

## Passwords & Port Forwarding
- mostly enumeration
- registry enumeration


## RunAs
- cmdkey list

## AutoRuns
- autoruns64
- accesschk64
- powerup.ps1
- invoke-allchecks
- msfvenom
- regsvc

## DLL Hijacking
- stop & start dllsvc
  