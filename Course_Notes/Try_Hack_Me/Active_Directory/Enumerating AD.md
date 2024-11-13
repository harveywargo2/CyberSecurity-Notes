 # References


# Notes

# Commands 
~~~
systemd-resolve --interface <interface> --set-dns <ipaddress> --set-domain <rootdomain>
~~~

~~~
runas.exe /netonly /user:<domain>\<username> cmd.exe
~~~

Rdp
~~~
xfreerdp /u:<uname> /p:<pwd> /v:<IP>
~~~


PowerShell
~~~
Get-ADUser -Filter 'Name -like "*string"' -Server <DC> | Format-Table Name, SamAccountName -A
~~~


