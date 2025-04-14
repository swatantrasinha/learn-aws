Link to main page : [back-to-main](../README.md)

Go to previous chapter : [Chapter-03](../chapter-03/README.md)

Go to next chapter : [Chapter-05](../chapter-05/README.md)


## Chapter 04: IAM Handson Walkthrough   

Go to - [What is AWS](https://aws.amazon.com/what-is-aws/)   

Go to AWS Console - [AWS-Console](https://us-east-1.console.aws.amazon.com/console/home?region=us-east-1)   

1. in search bar -> search for iam   
<img width="1491" alt="image" src="https://github.com/user-attachments/assets/a2c76c0a-e6de-49cc-bce5-9d772c12776b" />   


2. As we logged in with root account, so lets create users account.
For this we will first create **user group**   
Left Nav -> Access Management -> User Groups   
We will landup here: [User Group](https://us-east-1.console.aws.amazon.com/iam/home?region=us-east-1#/groups)   
<img width="760" alt="image" src="https://github.com/user-attachments/assets/cc749515-ce8f-4501-98c8-d4dff5b78b47" />  

3. Click on Create Group
   
4. give name as say **admin**
   
5. we can add existing user to this group if we want but we dont have any users as of now
   
6. In attach permission, search for admin permissions and check on **administrator access**   
<img width="760" alt="image" src="https://github.com/user-attachments/assets/eaa15db1-0ad9-431a-99bf-b835627a7c03" />

7. if we click on + icon after checkbox we can see permission in json format as well
<img width="1165" alt="image" src="https://github.com/user-attachments/assets/5007f925-2d62-4fb0-a7ed-df82ae0bf6cf" />

8. scroll and click on create group   

9. so **user group** for all the admin has been created   

10. So after creating **user group** we will now create **user**   
- Left Nav -> Access Management -> Users and then click on **create user** button
- give some name say **youtube**   
- click on checkbox **Provide user access to the AWS Management Console**   
- select radio button ****I want to create an IAM use**   
- In console password - select custom password and give some valid password
- Click on Next   
<img width="1386" alt="image" src="https://github.com/user-attachments/assets/d9886bbb-8dd0-4213-b01c-32efde7b8659" />

11. It will navigate to **Set Permission**
- In Permission Option Section -> Click on Radio Button **Add user to group**
- In User groups Section -> check on **admins** to add this user(youtube) to admins group   
- In Set Permission Boundary -> dont do anything for now
- Click on Next

12. 


 












