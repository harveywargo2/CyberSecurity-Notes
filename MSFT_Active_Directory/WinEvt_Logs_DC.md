# References
- https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise
- https://s0cm0nkey.gitbook.io/s0cm0nkeys-security-reference-guide/dfir-digital-forensics-and-incident-response/ir-event-log-cheatsheet
- https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/appendix-l--events-to-monitor
- Log References
	- https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx
	- https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/advanced-security-auditing-faq
- Audit Logon
	- https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/audit-user-account-management
- Audit Security Group
	- https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/audit-kerberos-authentication-service
- Audit User Account Changes
	- https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/audit-user-account-management
	- https://blog.menasec.net/2019/02/threat-hunting-26-persistent-password.html
	- https://vdoc.pub/documents/windows-security-monitoring-scenarios-and-patterns-6k5pema91320
	- https://learn.microsoft.com/en-us/troubleshoot/windows-server/identity/useraccountcontrol-manipulate-account-properties
	- https://www.reddit.com/r/sysadmin/comments/f67o6o/windows_event_id_4738/
- Audit Kerberos
	- https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/audit-kerberos-authentication-service

# Logging 
- EVTX Log location
~~~
System32\winevt\Logs
~~~
- Normally forwarded from domain controller to log storage source
- Certain Windows Security Logs only makes Sense on ADDS Domain Controllers 

| Group                        | EventID    | Name                                                     |
|------------------------------|------------|----------------------------------------------------------|
| Kerberos Auth Service        | 4768 (S,F) | A Kerberos authentication ticket (TGT) was requested     |
| Kerberos Auth Service        | 4771 (F)   | Kerberos pre-authentication failed                       |
| Kerberos Service Ticket Ops  | 4769 (S,F) | A Kerberos service ticket was requested                  |
| Kerberos Service Ticket Ops  | 4770 (S)   | A Kerberos service ticket was renewed                    |
| Security Group Management    | 4731 (S)   | A security-enabled local group was created               |
| Security Group Management    | 4732 (S)   | A member was added to a security-enabled local group     |
| Security Group Management    | 4733 (S)   | A member was removed from a security-enabled local group |
| Security Group Management    | 4734 (S)   | A security-enabled local group was deleted               |
| Security Group Management    | 4735 (S)   | A security-enabled local group was changed               | 
| Security Group Management    | 4764 (S)   | A group’s type was changed                               |
| Security Group Management    | 4799 (S)   | A security-enabled local group membership was enumerated |
| Logon                        | 4624 (S)   | An account was successfully logged on                    |
| Logon                        | 4625 (F)   | An account failed to log on                              |
| Logon                        | 4648 (S)   | A logon was attempted using explicit credentials         |
| User Account Management      |            |                                                          |
| Special Logon                |            |             |

## 4625 -  SubStatus Codes
- 0xC0000064 - User Logon with Misspelled or Bad User Account
- 0xC000006A - User Logon with Misspelled of Bad Password
- 0xC000006F - User Logon Outside Authorized Hours
- 0xC0000071 - User Logon with Expired Password
- 0xC0000072 - User Logon to Account Disabled by Administrator
- 0xC0000193 - User Logon with Expired Account
- 0xC0000234 - User Logon with Account Locked


## 4738 - Audit User Account Changes 
- 0x10: Account Enabled
- 0x11: Account Disabled
- 0x210: Account Enabled, Password Never Expires
- 0x15: Account Disabled, Password Not Required 
- 0x211: Account Disabled, Password Never Expires

| Index | HEX | DEC | Const Enabled | Const Disabled | Meaning |
|---|---|---|---|---|---|
|0 | 0x01 | 1 | 2080 | 2048 | Account Disabled |
| 2 | 0x04| 4 | 2082 | 2050 | Password Not Required |
| 4 | 0x10 | 16 | 2084 | 2052 | Normal Account | 
| 9 | 0x200 | 512 | 2089 | 2057 | Don't Expire Password | 

Old UAC Value : 0x10  -> New UAC Value: 0x210
Old UAC Value : 0x11 -> New UAC Value: 0x210
Old UAC Value : 0x15 -> New UAC Value: 0x210


## 4768 - Kerb Auth Ticket Requested
- 0x6 - User Name Doesn't Exist


## 4771 - Kerb Pre-Auth Failed
- 0x17 - Password Expired
- 0x18 - Invalid Pre Auth Info (Wrong Password)