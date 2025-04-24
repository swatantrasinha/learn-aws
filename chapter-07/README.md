## Chapter 07: Hands on Practice with EC2 machines   


Link to main page : 
[back-to-main](../README.md)



Go to previous chapter : 
[Chapter-06](../chapter-06/README.md)


Go to next chapter : 
[Chapter-08](../chapter-08/README.md)

 Go to [AWS-Console](https://us-east-1.console.aws.amazon.com/console)
and search for EC2


Note: Any machine that we create lets say in us-east-1 region, the moment we migrate to other region say ap-south-1 those machines would be running but won't be shown as region is different. So machines are tied to region.

<img width="981" alt="image" src="https://github.com/user-attachments/assets/e913192b-12e7-42dd-97fc-bced3d1c8b32" />
We can see in nevtNav the different option on EC2 page   

- one the option is **Instance Type**   
<img width="730" alt="image" src="https://github.com/user-attachments/assets/c8bad9ae-9ddb-473e-b85f-432e923b822d" />

- in **Reserved Instances** we can get maximum discount

- images -> **AMI** : Amazon Machine Image   

- **Elactic Block Store** : determines what kind of storage will be used 

Lets go back to  EC2 Dashboard  (in leftNav) 

## launch instance  
 
1. Click on dropdown next to Launch Instance Button   
<img width="679" alt="image" src="https://github.com/user-attachments/assets/810ea633-d193-47d7-a16c-84ff6ec684af" />

As We don't have any template to select, so directly click on **Launch Instance**    

2.   so we will populate required fields here   

- Name -->  my machine 1

- Number of instance --> 1

- Application and OS Images --> select **Amazon Linux**

- Architecture --> In Dropdown - 64-bit (x86) is selected - let it be
  <img width="887" alt="image" src="https://github.com/user-attachments/assets/53286d8d-384a-470e-ae1c-76f2061aa049" />

- Instance Type -> turn on switch button for **all generations**. Select the below instance type:   
  <img width="521" alt="image" src="https://github.com/user-attachments/assets/999ea43f-62c7-4313-b7e9-1a84b28ebebb" />

- key-pair login -->  we discussed that we can generate key-pair and we need to store those and change permission
<img width="302" alt="image" src="https://github.com/user-attachments/assets/150a93a0-ba96-4cc8-8dbf-dbf374e26048" />   
Here we can enter name, keep type as RSA and download as .pem and then we need to change permission to login
Note: for now, we will select radio button **Proceed without key pair** (in video its mentioned but not able to find it- see above screenshot)

- Network Settings --> below are the defaults, need not to change ( let it be) :  
<img width="539" alt="image" src="https://github.com/user-attachments/assets/a144f8c9-4ad0-4c5f-bc1d-26391db6b7d3" />

- Configure Storage --> we will go with defaults:   
<img width="345" alt="image" src="https://github.com/user-attachments/assets/51c9ff0a-678c-474a-8094-981ccd28053b" />


 






   


   


 
