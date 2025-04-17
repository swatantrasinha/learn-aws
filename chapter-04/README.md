Link to main page : [back-to-main](../README.md)

Go to previous chapter : [Chapter-03](../chapter-03/README.md)

Go to next chapter : [Chapter-05](../chapter-05/README.md)


## Chapter 04: IAM Handson Walkthrough   

Go to - [What is AWS](https://aws.amazon.com/what-is-aws/)   

Go to AWS Console - [AWS-Console](https://us-east-1.console.aws.amazon.com/console/home?region=us-east-1)  
 
### 1. In search bar -> search for iam   
<img width="1491" alt="image" src="https://github.com/user-attachments/assets/a2c76c0a-e6de-49cc-bce5-9d772c12776b" />   
   


### 2. We logged in with root account, so lets create users account.    

For this we will first create **user group**  
 
Left Nav -> Access Management -> User Groups   

We will landup here: [User Group](https://us-east-1.console.aws.amazon.com/iam/home?region=us-east-1#/groups)   
<img width="760" alt="image" src="https://github.com/user-attachments/assets/cc749515-ce8f-4501-98c8-d4dff5b78b47" />  

### 3. Click on Create Group
   
### 4. give name as say **admin**
   
### 5. we can add existing user to this group if we want but we dont have any users as of now
   
### 6. In attach permission, search for admin permissions and check on **administrator access**      
<img width="760" alt="image" src="https://github.com/user-attachments/assets/eaa15db1-0ad9-431a-99bf-b835627a7c03" />

### 7. if we click on + icon after checkbox we can see permission in json format as well
<img width="1165" alt="image" src="https://github.com/user-attachments/assets/5007f925-2d62-4fb0-a7ed-df82ae0bf6cf" />

### 8. scroll and click on create group   

### 9. so **user group** for all the admin has been created   

### 10. So after creating **user group** we will now create **user**   
- Left Nav -> Access Management -> Users and then click on **create user** button
- give some name say **youtube**   
- click on checkbox **Provide user access to the AWS Management Console**   
- select radio button ****I want to create an IAM user**   
- In console password - select custom password and give some valid password
- Click on Next   
<img width="1386" alt="image" src="https://github.com/user-attachments/assets/d9886bbb-8dd0-4213-b01c-32efde7b8659" />

### 11. It will navigate to **Set Permission**
- In Permission Option Section -> Click on Radio Button **Add user to group**
- In User groups Section -> check on **admins** to add this user(youtube) to admins group   
- In Set Permission Boundary -> don't do anything for now
- Click on Next
<img width="1415" alt="image" src="https://github.com/user-attachments/assets/f8d7b424-d25b-4304-a786-405aa92a4958" />


### 12.  This will take to Review and Create Page   

<img width="1428" alt="image" src="https://github.com/user-attachments/assets/1a56998f-8c75-4010-9a84-99eb94b6853f" />   
On scroll we will find the section ->  **Tags**  - optional -> skip it for now

### 13. Click On **Create User** Button   

<img width="1501" alt="image" src="https://github.com/user-attachments/assets/2145c421-712f-437e-ab3f-e040c7b85742" />

so the new user is created   

### 14. At the top navigation -> Click on Users    

<img width="1488" alt="image" src="https://github.com/user-attachments/assets/f717a8d7-e935-43e1-b986-cdb5d814f367" />

A doilog box will appear click on Continue   


### 15. When we click on the user(youtube), we will see many tabs -> click on Security Credentials   
   
<img width="1480" alt="image" src="https://github.com/user-attachments/assets/31ae04d3-8c61-4748-9443-e7121628c526" />
We can see options like:   
- Manage Console Access   
- Create Access Key   

### 16. Click on Access Key      
<img width="1188" alt="image" src="https://github.com/user-attachments/assets/87a99013-f3db-4a57-b6c0-6dcddca950d1" />   
   
- In use case -> select radio button for **CLI**   
- click on checkbox for **confirmation**   
- click on Next   

### 17. It will to to **Set description tag**
Inside textbox for  **Description tag value**, give some text say **this is for the code access**
<img width="1192" alt="image" src="https://github.com/user-attachments/assets/82f9a374-75bc-4769-8e55-89d2ec940da2" />

### 18. Click on Create Access Key. It will take to next page where it will show    
**access key** and **secret key**
<img width="1192" alt="image" src="https://github.com/user-attachments/assets/cc6579d1-2d02-4ed3-952a-a4d8b008bbb3" />
We need to save this or download as CSV

### 19. Click on **Done**

### 20. Activate IAM Access   
   
Go to Billing and Cost Management [Link](https://us-east-1.console.aws.amazon.com/billing/home#/account)   

- Scroll to section **IAM user and role access to Billing information **
- Click on Edit
- Click on checkbox **Activate IAM Access**
- Click on Update
<img width="761" alt="image" src="https://github.com/user-attachments/assets/fadf332b-9cbb-4fdc-8739-dae256df8fb7" />

