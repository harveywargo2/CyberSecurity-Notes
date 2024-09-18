# References
- https://learn.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/how-to-connect-fed-azure-adfs
- https://learn.microsoft.com/en-us/windows-server/identity/active-directory-federation-services
- https://learn.microsoft.com/en-us/microsoft-365/troubleshoot/active-directory/update-federated-domain-office-365
- https://learn.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-monitor-federation-changes

When you federate your on-premises environment with Azure AD, you establish a trust relationship between the on-premises identity provider and Azure AD. Adversaries may add new domain trusts or modify the properties of existing domain trusts to evade defenses and/or elevate privileges. Domain trust details, such as whether or not a domain is federated, allow authentication and authorization properties to apply between domains for the purpose of accessing shared resources.  These trust objects may include accounts, credentials, and other authentication material applied to servers, tokens, and domains. Manipulating the domain trusts may allow an adversary to escalate privileges and/or evade defenses by modifying settings to add objects which they control.Due to this established trust, Azure AD honors the security token issued by the on-premises identity provider post authentication, to grant access to resources protected by Azure AD

Active Directory Federation Service (AD FS) enables Federated Identity and Access Management by securely sharing digital identity and entitlements rights across security and enterprise boundaries. 

AD FS extends the ability to use single sign-on functionality that is available within a single security or enterprise boundary to Internet-facing applications to enable customers, partners, and suppliers a streamlined user experience while accessing the web-based applications of an organization.