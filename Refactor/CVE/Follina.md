## CVE-2022-30190 
- RCE Via MSDT.EXE Follina 
- A remote code execution vulnerability exists when MSDT is called using the URL protocol from a calling application such as Word. 
- An attacker who successfully exploits this vulnerability can run arbitrary code with the privileges of the calling application. 
- The attacker can then install programs, view, change, or delete data, or create new accounts in the context allowed by the user’s rights.
- [Huntress - Exploitation Example](https://www.huntress.com/blog/microsoft-office-remote-code-execution-follina-msdt-bug)
- [Bleeping Computer - Expoloitation Example](https://www.bleepingcomputer.com/news/security/new-microsoft-office-zero-day-used-in-attacks-to-execute-powershell/)
- [NVD - CVE-2022-30190](https://nvd.nist.gov/vuln/detail/CVE-2022-30190)
- [MSFT Update Guide](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2022-30190)
- [Exploitation Example](https://doublepulsar.com/follina-a-microsoft-office-code-execution-vulnerability-1a47fce5629e)
- https://irsl.medium.com/the-trouble-with-microsofts-troubleshooters-6e32fc80b8bd
- https://www.securonix.com/blog/detecting-microsoft-msdt-dogwalk/
- [MDE Mitigation](https://docs.microsoft.com/en-us/microsoft-365/security/defender-endpoint/attack-surface-reduction-rules-reference?view=o365-worldwide#block-all-office-applications-from-creating-child-processes)
- [MSFT Guidance](https://msrc-blog.microsoft.com/2022/05/30/guidance-for-cve-2022-30190-microsoft-support-diagnostic-tool-vulnerability/)

Example Command Line LOLBAS Project
~~~
msdt.exe /id PCWDiagnostic /skip force /param "IT_LaunchMethod=ContextMenu IT_BrowseForFile=/../../$(calc).exe"
~~~