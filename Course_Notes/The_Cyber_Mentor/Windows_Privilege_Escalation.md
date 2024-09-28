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


# Initial Enum
## System
- systeminfo
- wmic qfe
- wmic logicaldisk
- wmic logicaldisk get caption
## User
- whoami
- whoami /priv
- whoami /groups
- net user
- net user uname 
- net localgroup
## Network
- ipconfig
- ipconfig /all
- arp -a 
- route print
- netstat -ano
## Password
- findstr /si 
## FW & AV Enum
- windefend
- sc queryex type= service
- netsh advfirewall firewall dump
- netsh firewall show state
- netsh firewall show config