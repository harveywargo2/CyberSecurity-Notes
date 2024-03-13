## MSDT 
- https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/msdt
- https://www.file.net/process/msdt.exe.html
- The genuine msdt.exe file is a software component of Microsoft Windows Operating System by Microsoft Corporation.
- "Msdt.exe" is Microsoft's Diagnostic Troubleshooting Wizard.
- [LOLBAS-MSDT](https://lolbas-project.github.io/lolbas/Binaries/Msdt/)
- https://irsl.medium.com/the-trouble-with-microsofts-troubleshooters-6e32fc80b8bd
- [T1218 - System Binary Proxy Execution](https://attack.mitre.org/techniques/T1218/)
- [T1202 - Indirect Command Execution](https://attack.mitre.org/techniques/T1202/)
- MSDT is commonly used to execute scripts or bypass defenses via Proxy Execution from a Trusted Binary.  

Typical Paths:
~~~
C:\Windows\System32\Msdt.exe
C:\Windows\SysWOW64\Msdt.exe
~~~

Example Command Line from LOLBAS Project
~~~
msdt.exe -path C:\WINDOWS\diagnostics\index\PCWDiagnostic.xml -af C:\PCW8E57.xml /skip TRUE
~~~

