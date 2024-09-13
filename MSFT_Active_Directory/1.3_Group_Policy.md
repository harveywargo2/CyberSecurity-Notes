# References
- https://www.youtube.com/watch?v=rEhTzP-ScBo
- https://rootdse.org/posts/active-directory-basics-3/

## GPO 
- contains the Group Policy settings and represents the files related to policy settings in the file system and in the Active Directory
- Default Domain Policy
- Default Domain Controllers Policy
- Group policy objects are a set of policies that are grouped together and applied to either computer or user objects
- GPO Refresh Interval
	- default is 90 minutes
- Group Policy Management Console
```
gpedit.msc
```

## Common GPO
- Security Policy
- IT Policy
- Audit/Logging Policy
- Password policy
- automations & network drive mapping


## SYSVOL
- Network Share
- Stores GPO Templates
- default location
~~~
%SYSTEMROOT%\SYSVOL\sysvol
~~~
- Network location
~~~
\\<domain_name>\SYSVOL
~~~
- The SYSVOL policies folder contains all the GPOs. 
	- And folder name for each GPO is same as that GPO’s GUID.
- Since everyone has read access to SYSVOL, it is just a matter of finding the `cpassword` in the XML files and decrypting the passwords.