# Design and implement SQL Server Database security

## Configure firewalls
SQL Server uses port 1433, there are numerous others ports (See link below for MS details) but depending on if you use dynamic ports or specify ports in the SQL Server Configuration Manager will also help re-fine which ports should be opened. 

## Manage logins, users, and roles
BP to use AD groups for logins and link users and logins to roles. to simplify and standardize access.  

- assign permissions 
- configure auditing

## Configure Transparent Database Encryption (TDE)
Encrypts the database at rest (encluding backups). You need to create a master certificate, the encrypt the database. You can only restore the database to an intance that has the same master certificate. 

- configure row-level security
- configure data encryption
- configure data masking
- configure Always Encrypted  

[Return to Design and implement Security](readme.md)  
[Return to Home](./readme.md)

