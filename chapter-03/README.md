Link to main page : [back-to-main](../README.md)

Go to previous chapter : [Chapter-02](../chapter-02/README.md)

## Chapter 03: Learn IAM (Identity and Access Management) in AWS   

## Identity - what is allowed by them   

<img width="531" alt="image" src="https://github.com/user-attachments/assets/01c7f098-f15e-434d-b63e-21e27765ae5e" />

## Group, Role and Policy   
- Group is a way to organize user
- Policy defines permission   
- User can get permission directly or via group
- Roles are for delegation and are assumed
- With assumed roles, we can talk to other services

### Root User
- the email with which SignUp AWS
- has full permission and cannot be reduced the permission(so better avoid using root user)
- should be avoided
- enabled MFA

### Creare New User   
- from root user we can create **new user**
- by default no permission
- can create around 5000+ accounts
- use policies and prefer groups
- ARN : Amazon Resource Name (unique name for resource)
- username/password or access keys

### Creating Groups
<img width="991" alt="image" src="https://github.com/user-attachments/assets/1e09a62f-5b72-4353-acfd-2269d2cfdc41" />










