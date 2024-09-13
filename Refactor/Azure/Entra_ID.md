## Guest Accounts
- https://learn.microsoft.com/en-us/azure/active-directory/external-identities/b2b-quickstart-add-guest-users-portal   

Allow Policy List Blade 
**Default Setting** 
> Guest users have limited access to properties and memberships of directory objects

**Best Practice Mitigation Setting**
> Guest user access is restricted to properties and memberships of their own directory objects (most restrictive)


## Domain Trust
- https://learn.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/how-to-connect-fed-azure-adfs
- https://learn.microsoft.com/en-us/windows-server/identity/active-directory-federation-services
- https://learn.microsoft.com/en-us/microsoft-365/troubleshoot/active-directory/update-federated-domain-office-365
- https://learn.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-monitor-federation-changes

When you federate your on-premises environment with Azure AD, you establish a trust relationship between the on-premises identity provider and Azure AD. Adversaries may add new domain trusts or modify the properties of existing domain trusts to evade defenses and/or elevate privileges. Domain trust details, such as whether or not a domain is federated, allow authentication and authorization properties to apply between domains for the purpose of accessing shared resources.  These trust objects may include accounts, credentials, and other authentication material applied to servers, tokens, and domains. Manipulating the domain trusts may allow an adversary to escalate privileges and/or evade defenses by modifying settings to add objects which they control.Due to this established trust, Azure AD honors the security token issued by the on-premises identity provider post authentication, to grant access to resources protected by Azure AD

Active Directory Federation Service (AD FS) enables Federated Identity and Access Management by securely sharing digital identity and entitlements rights across security and enterprise boundaries. 

AD FS extends the ability to use single sign-on functionality that is available within a single security or enterprise boundary to Internet-facing applications to enable customers, partners, and suppliers a streamlined user experience while accessing the web-based applications of an organization.


## CAP 
- https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/overview


## Audit Log
- https://learn.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-audit-logs
- https://learn.microsoft.com/en-us/graph/api/resources/directoryaudit?view=graph-rest-1.0
- https://learn.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-reporting-api
- https://learn.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory
- https://learn.microsoft.com/en-us/azure/active-directory/reports-monitoring/reference-audit-activities
- https://learn.microsoft.com/en-us/azure/active-directory/reports-monitoring/concept-audit-logs

DirectoryAudits API Endpoint
~~~

https://graph.microsoft.com/v1.0/auditLogs/directoryAudits

~~~

The audit activity report is available in all editions of Azure AD. To access the audit logs, you need to have one of the following roles:
- Report Reader
- Security Reader
- Security Administrator
- Global Reader
- Global Administrator

## AAD Sandbox Activation via LEARN Module
- https://learn.microsoft.com/en-us/training/modules/create-users-and-groups-in-azure-active-directory/3-exercise-add-delete-users-azure-ad

Windows Azure Active Directory - Client - ID00000002-0000-0000-c000-000000000000