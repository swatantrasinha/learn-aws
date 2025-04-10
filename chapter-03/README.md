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

### IAM Roles   
- Roles are assumed by users/applications/services
- gain the permission of " **role** " only

### IAM Policies   
- Policies are JSON documents
- Implicitly denied
- Identity based(this is common) and resource based(only few services support this)
- AWS support 6 types of policies- see below screenshot      
<img width="501" alt="image" src="https://github.com/user-attachments/assets/c70c2f6d-787c-4e25-bb45-9f4b5223a981" />

### Account Access
There are two ways how we can give permission/access to an account   
- AWS Console
- AWS API
<img width="1147" alt="image" src="https://github.com/user-attachments/assets/217786d7-52cb-4afd-9457-2ddd51818e90" />

### AWS Authentication   
Core policy is :   
<img width="796" alt="image" src="https://github.com/user-attachments/assets/a827e389-be1e-45bf-b675-bba569df45f0" />   

### SCP (Service Control Policies)  
As we saw in **IAM Policies**  above, it limits the permission but do not grant the permission.
<img width="1154" alt="image" src="https://github.com/user-attachments/assets/ab29fb89-1516-479f-8402-e8f46c4f5a5d" />





















