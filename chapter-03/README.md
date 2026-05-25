Link to main page : [back-to-main](../README.md)

Go to previous chapter : [Chapter-02](../chapter-02/README.md)

Go to next chapter : [Chapter-04](../chapter-04/README.md)


## Chapter 03: Learn IAM (Identity and Access Management) in AWS   

No body should have access from the **Root Account** . The **Root Account** is just to create the AWS account and then its rarely touched(that too when something goes seriously wrong).


## Identity - what is allowed by them   

<img width="531" alt="image" src="https://github.com/user-attachments/assets/01c7f098-f15e-434d-b63e-21e27765ae5e" />

## Group, Role and Policy   
- Group is a way to organize user
- Policy defines permission - what all you can do with you AWS account      
- User can get permission directly or via group - good practice is giving policies(permissions) via group   
- Roles are for delegation and are assumed
- With assumed roles, we can talk to other services   

<img width="1139" height="258" alt="image" src="https://github.com/user-attachments/assets/dc0a4b66-4c07-4d90-ba97-e3c3a5dbe3c8" />   
<details>
  <summary>Policy vs Permission in AWS</summary>
  <p>
  
Permission = What action is allowed or denied   
It defines what you can do on a resource   
Example actions: 
- s3:PutObject
- ec2:StartInstances
- dynamodb:Query

✅ Think of permissions as individual rules like:   
- Allow “read from S3”
- Deny “delete EC2 instances”

---

Policy = A document (JSON) that defines permissions

A policy is a container or set of permissions written in JSON format
Attached to: Users/Roles/Groups/Resources (like S3 bucket policies)   

✅ Think of a policy as: A package 📦  that contains multiple permissions   

<img width="655" height="247" alt="image" src="https://github.com/user-attachments/assets/9431515f-b1c2-4859-aa93-a38461e5b5cf" />   

  </p>
</details>

<hr/>

### <ins>Root User</ins>
- the email with which SignUp AWS
- has full permission and cannot reduce the permission(so better avoid using root user)
- should be avoided
- enabled MFA

### <ins>Create New User</ins>   
- from root user we can create **new user**
- by default no permission
- can create around 5000+ accounts
- use policies and prefer groups
- ARN : Amazon Resource Name (unique name for resource)
- username/password or access keys

### <ins>Creating Groups</ins>
<img width="991" alt="image" src="https://github.com/user-attachments/assets/1e09a62f-5b72-4353-acfd-2269d2cfdc41" />   

### <ins>IAM Roles</ins>   
- Roles are assumed by users/applications/services
- gain the permission of "**role**" only

### <ins>IAM Policies</ins>   
- Policies are JSON documents
- Implicitly denied
- Identity based(this is common) and resource based(only few services support this)
- AWS support 6 types of policies- see below screenshot      
<img width="501" alt="image" src="https://github.com/user-attachments/assets/c70c2f6d-787c-4e25-bb45-9f4b5223a981" />

<details>
  <summary>Summary : AWS Policies</summary>
  <p>
    <img width="461" height="579" alt="image" src="https://github.com/user-attachments/assets/b0499b4a-4b9b-416e-b5be-8f9b6002bdb9" />
    <hr />
    <img width="463" height="587" alt="image" src="https://github.com/user-attachments/assets/dc7146e7-88b4-4f2f-b69f-d252cdb2986a" />
    <hr />
    <img width="494" height="472" alt="image" src="https://github.com/user-attachments/assets/ae355706-5897-4824-895d-aaa29e2384b6" />
    <hr />
    <img width="475" height="717" alt="image" src="https://github.com/user-attachments/assets/330e66e4-39c1-4296-80aa-da3f8d653873" />
    <hr />
    <img width="475" height="764" alt="image" src="https://github.com/user-attachments/assets/655c808a-f27b-45d9-8b05-b1b3dac8cdd7" />
    <hr />
    <img width="451" height="572" alt="image" src="https://github.com/user-attachments/assets/2b626df0-aa20-409e-8f12-ba7117fd707a" />
    <hr />
    <img width="559" height="594" alt="image" src="https://github.com/user-attachments/assets/c6e61e7f-e71f-4131-b15a-eaa27a2082d4" />
    <hr />
    <img width="812" height="752" alt="image" src="https://github.com/user-attachments/assets/b1ac4556-bdf1-4629-8fa1-92ffa812e2b9" />
    <hr />
    <img width="685" height="396" alt="image" src="https://github.com/user-attachments/assets/f5466c91-daad-4a10-aa85-db9d911df1dd" />
    <hr />
  </p>
</details>

### <ins>Account Access</ins>
There are two ways how we can give permission/access to an account   
- AWS Console
- AWS API
<img width="1147" alt="image" src="https://github.com/user-attachments/assets/217786d7-52cb-4afd-9457-2ddd51818e90" />

### <ins>AWS Authentication</ins>   
Core policy is :   
<img width="796" alt="image" src="https://github.com/user-attachments/assets/a827e389-be1e-45bf-b675-bba569df45f0" />   

### <ins>SCP (Service Control Policies)</ins>  
As we saw in **IAM Policies**  above, it limits the permission but do not grant the permission.
<img width="1154" alt="image" src="https://github.com/user-attachments/assets/ab29fb89-1516-479f-8402-e8f46c4f5a5d" />   


### <ins> Best Practices </ins>
<img width="1126" alt="image" src="https://github.com/user-attachments/assets/65609b38-2153-4842-b311-dc0525996b4c" />























