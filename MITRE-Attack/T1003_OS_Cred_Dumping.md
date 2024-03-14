## References
 - https://book.hacktricks.xyz/windows-hardening/stealing-credentials
 - https://attack.mitre.org/techniques/T1003/
 - https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/hh994565(v=ws.11)
- https://www.reliaquest.com/blog/credential-dumping-part-1-a-closer-look-at-vulnerabilities-with-windows-authentication-and-credential-management/

## T1003.001 LSASS
- https://redcanary.com/threat-detection-report/techniques/lsass-memory/
- https://pentestlab.blog/2021/05/24/dumping-rdp-credentials/
- https://www.slideshare.net/heirhabarov/hunting-for-credentials-dumping-in-windows-environment
- https://threathunterplaybook.com/hunts/windows/170105-LSASSMemoryReadAccess/notebook.html
- https://clymb3r.wordpress.com/2013/04/09/modifying-mimikatz-to-be-loaded-using-invoke-reflectivedllinjection-ps1/
- https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1003.001/T1003.001.md
- https://attack.mitre.org/techniques/T1003/001/

LSASS stores credentials in memory on behalf of users with active Windows sessions. The purpose of storing these credentials is so that users can access network resources, file shares, mail, and more without having to re-authenticate to each individual service.

LSASS stores credential material in various forms, including:
-   Reversibly encrypted plaintext
-   Kerberos Tickets
-   NT hashes
-   LM hashes

Credentials are cached to LSASS whenever a user authenticated in an interactive manner. The following types of activity will put the user’s credential material into memory:
-   Starting a local session
-   Starting an RDP session
-   Running a task via RunAs
-   Running an active Windows Service
-   Running a scheduled task
-   Running a batch job
-   Running a task by utilizing a remote administration tool

#### TaskManager, ProcDump & Comsvc.dll
- https://lolbas-project.github.io/lolbas/Libraries/comsvcs/
- https://modexp.wordpress.com/2019/08/30/minidumpwritedump-via-com-services-dll/
- https://www.ired.team/offensive-security/credential-access-and-credential-dumping/dump-credentials-from-lsass-process-without-mimikatz

Typical Paths of DLL & Binaries
~~~
c:\windows\system32\comsvcs.dll

c:\windows\system32\lsass.exe
~~~

#### Using ADPlus
- https://lolbas-project.github.io/lolbas/OtherMSBinaries/Adplus
- https://mrd0x.com/adplus-debugging-tool-lsass-dump/
~~~
C:\Program Files (x86)\Windows Kits\10\Debuggers\x64\adplus.exe

C:\Program Files (x86)\Windows Kits\10\Debuggers\x86\adplus.exe
~~~

#### Silent Process Exit
- https://github.com/deepinstinct/LsassSilentProcessExit
- https://www.deepinstinct.com/blog/lsass-memory-dumps-are-stealthier-than-ever-before-part-2

#### WerFault/Shtinkering
- https://media.defcon.org/DEF%20CON%2030/DEF%20CON%2030%20presentations/Asaf%20Gilboa%20-%20LSASS%20Shtinkering%20Abusing%20Windows%20Error%20Reporting%20to%20Dump%20LSASS.pdf

#### Nanodump
- https://github.com/helpsystems/nanodump

#### Dumpert
- https://github.com/outflanknl/Dumpert
- https://outflank.nl/blog/2019/06/19/red-team-tactics-combining-direct-system-calls-and-srdi-to-bypass-av-edr/

#### Pypykatz
- https://andreafortuna.org/2020/03/20/pypykatz-a-mimikatz-python-implementation/
- https://github.com/skelsec/pypykatz

### Keymgr
- https://systemweakness.com/windows-credential-manager-for-hackers-e67aad9c2a75


## T1003.002 Security Account Manager
- https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1003.002/T1003.002.md
- https://attack.mitre.org/techniques/T1003/002/

## T1003.003 NTDS
- https://attack.mitre.org/techniques/T1003/003/
- https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1003.003/T1003.003.md

## T1003.004 LSA Secrets 
- https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1003.004/T1003.004.md
- https://attack.mitre.org/techniques/T1003/004/

## T1003.006 DCSync
- https://www.alteredsecurity.com/post/a-primer-on-dcsync-attack-and-detection
- https://www.proofpoint.com/us/blog/email-and-cloud-threats/behavioral-analysis-and-aiml-threat-detection-going-behind-scenes
-  https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-drsr/f977faaa-673e-4f66-b9bf-48c640241d47
- https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1003.006/T1003.006.md

Permissions Needed
- DS-Replication-Get-Changes
- DS-Replication-Get-Changes-All
- DS-Replication-Get-Changes-Infiltered-Set

(Domain Admin, Administrators, Enterprise Admins, DC Computer Accounts)
