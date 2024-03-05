# Skill Up
- Certain Windows Security Logs only makes Sense on ADDS Domain Controllers 
- Log Location `System32\winevt\Logs`
- Event Viewer 

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
| Special Logon                |            |                                                          |


## References
- https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise
- https://s0cm0nkey.gitbook.io/s0cm0nkeys-security-reference-guide/dfir-digital-forensics-and-incident-response/ir-event-log-cheatsheet
- https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx
- https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/appendix-l--events-to-monitor




