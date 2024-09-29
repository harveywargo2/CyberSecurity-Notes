# References
- https://rootdse.org/posts/active-directory-basics-2/

## User Objects
- user accounts
- DistinguishedName 
	- CN=Joe Green ,CN=Users,DC=pburgh, DC=steelers
- UPN
	- Joe.Green@pburgh.steelers

## Computer Objects
-  machine that is joined to the domain
- SamAccountName
	- HostName$
	- typically end with Dollar sign in logs
- A Domain has three types of objects that can be counted as computer objects:
	- Domain Controllers
	- Domain Computers (Workstations)
	- Member servers

## Group Objects
- Used to contain a number of different Active Directory Objects such as users, computers and other groups
- Hierarchical
- Nesting allowed

### Distribution Group
- Used to include multiple users into group
- Email Group

### Security Group
- Provide access & permissions for users/computers in the group
- Scopes
	- Domain Local
		- Used to manage access permissions to different domain resources only in the domain where it was created
	- Global
		- Used to provide access to resources in another domain. A global group can be added to other global and local groups
	- Universal
		- Used to define roles and manage resources that are distributed across multiple domains. If a network has multiple branches connected, it is desirable to use universal groups only for rarely changing groups

### Admin Groups
- Domain Admins
	- Admin Privileges to members in the domain
- Enterprise Admins
	- Admin Privileges to the whole forest
- Schema Admins
	- can modify active directory database schema
- DNSAdmins
- Print Operators
- Protected Users
- Server Operators
- Account Operators
- Backup Operators
- Remote Desktop Users
	- can use RDP 
- Group Policy Creator Owners

## Shared Folders 
- Shared folders are objects in AD
