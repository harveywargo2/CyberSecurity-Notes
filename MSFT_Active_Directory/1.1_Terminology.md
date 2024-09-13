# References
- https://rootdse.org/posts/active-directory-basics-1/
- Youtube Overview
	- https://www.youtube.com/watch?v=4qC7H-y7oKI
	- https://www.youtube.com/watch?v=85-bp7XxWDQ&t=1455s

# Terminology
## Active Directory
- Active Directory is a Directory service that acts as a centralised repository and holds all the data related to Active Directory objects
- stores all the data related to objects like Active Directory users, computers, servers, and other resources within an organization 
- primary function is to provide a way to authenticate users and machines in a domain environment
- Active Directory acts like a phone book for the org
- Hierarchical structure 
	- classes/schema

## Domain
- domain is a collection of all Active Directory objects 
- managed by Domain controller
- machinename.domain
- domains can create boundaries 
- objects in a Domain
	- user
	- computers
	- groups
	- GPO
	- DNS
	- DHCP
	- OUs
	- Security Groups

## Domain Controller
- Windows Server 
- Domain Controllers host the service that responds to the authentication requests in a domain
- DCs authenticates and validates the user/computer/ticket access 
- DC validates info like username & password 

## NTDS.dit
- Active directory database is stored in the file 
```
C:\Windows\NTDS\ntds.dit
```
- All ad objects stored in this file
- NTDS is NT Directory Services
- DIT is Directory Information Tree

## Forest
- Collection of multiple domain trees that share a common schema and all domains are connected together through a trust
- If a forest contains a single domain, then that domain itself is the root domain

## Trust
- In a forest, domains are interconnected by connections called as trusts
- Once a trust is established between two domains
	- it grants access to resources to the users, groups and computers across entities
- Trust can be one-way or two-way
- Trust can be transitive or non-transitive
- Transitive
	- Domain 1 TRUST Domain 2 AND Domain 2 TRUST Domain 3 
		- Domain 1 Implied TRUST to Domain 3
- Non-Transitive
	- Domain 1 TRUST Domain 2 AND Domain 2 TRUST Domain 3 
		- Domain 1 DOES NOT TRUST Domain 3

## Organizational Unit (OU)
- Containers/Folders
- Heirarchical
- Nesting allowed
- group objects like user accounts, computers, and groups together
- used to manage resources 
- used to apply GPO 
- used to control access

## Global Catalog
- The root domain controller in a domain is considered as the Global Catalog server by default
- global catalog server has replica of its own domain and read-only partitions with objects of other domains