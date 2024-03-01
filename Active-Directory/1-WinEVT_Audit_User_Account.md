# Skill Check
- 4720
- 4722
- 4723
- 4724
- 4725
- 4726
- 4738
- 4740
- 4767
- 4798
- 5376
- 5377

#### EID 4738

| Index | HEX | DEC | Const Enabled | Const Disabled | Meaning |
|---|---|---|---|---|---|
|0 | 0x01 | 1 | 2080 | 2048 | Account Disabled |
| 2 | 0x04| 4 | 2082 | 2050 | Password Not Required |
| 4 | 0x10 | 16 | 2084 | 2052 | Normal Account | 
| 9 | 0x200 | 512 | 2089 | 2057 | Don't Expire Password | 

-    Old UAC Value : 0x10  -> New UAC Value: 0x210
-    Old UAC Value : 0x11 -> New UAC Value: 0x210
-    Old UAC Value : 0x15 -> New UAC Value: 0x210

0x10: Account Enabled
0x11: Account Disabled
0x210: Account Enabled, Password Never Expires
0x15: Account Disabled, Password Not Required 
0x211: Account Disabled, Password Never Expires

## References
- https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-10/security/threat-protection/auditing/audit-user-account-management
- https://blog.menasec.net/2019/02/threat-hunting-26-persistent-password.html
- https://vdoc.pub/documents/windows-security-monitoring-scenarios-and-patterns-6k5pema91320
- https://learn.microsoft.com/en-us/troubleshoot/windows-server/identity/useraccountcontrol-manipulate-account-properties
- https://www.reddit.com/r/sysadmin/comments/f67o6o/windows_event_id_4738/