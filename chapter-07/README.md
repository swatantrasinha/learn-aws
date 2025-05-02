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
We can see in levtNav the different option on EC2 page   

- one of the option is **Instance Type**   
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

- key-pair login -->  We earlier discussed that we can generate key-pair and we need to store those and change permission   
<img width="302" alt="image" src="https://github.com/user-attachments/assets/150a93a0-ba96-4cc8-8dbf-dbf374e26048" />        

Here we can enter name, keep type as RSA and download as .pem and then we need to change permission to login    
Note: for now, we will select radio button **Proceed without key pair**    
     


- Network Settings --> below are the defaults, need not to change ( let it be) :  
<img width="539" alt="image" src="https://github.com/user-attachments/assets/a144f8c9-4ad0-4c5f-bc1d-26391db6b7d3" />

- Configure Storage --> we will go with defaults:   
<img width="345" alt="image" src="https://github.com/user-attachments/assets/51c9ff0a-678c-474a-8094-981ccd28053b" />

- Advanced details --> if we scroll then at the end  we can see meta-data section and this has user-data   
<img width="472" alt="image" src="https://github.com/user-attachments/assets/bbdb3adb-43c6-4922-8872-0610a28fac2f" />    

(No need to fill anything here just for info)   

3. Click on **Launch Instance**

- Once we click , we will see error
<img width="242" alt="image" src="https://github.com/user-attachments/assets/648525c4-534e-47d8-be8c-26095e59ce0e" />   

So, for this error we will click **Create New Key Pair** and choose  **Proceed without key pair**   
Lecture video screenshot below:   
<img width="325" alt="image" src="https://github.com/user-attachments/assets/f01f5405-a60a-4341-8f2d-6dd342979440" />   
- click on **Launch Instance** again and it will be success 

> [!CAUTION]    
> <code style="color:red"> The above option - **Proceed without key pair** was shown by lecturer
but I am not able to find it while doing practical. So not able to launch instance </code>

---

For this problem lets follow some other course for EC2 instance creation:   
[AWS in ONE VIDEO](https://www.youtube.com/watch?v=N4sJj-SxX00&t=2368s) --> forward to **1:20:00** and follow:      
<img width="970" alt="image" src="https://github.com/user-attachments/assets/7724c0d8-02e7-4866-a2b6-1de8a5d535fa" />   

<img width="936" alt="image" src="https://github.com/user-attachments/assets/b2058101-1cea-41c8-8db3-7b38c9693bda" />


<img width="1070" alt="image" src="https://github.com/user-attachments/assets/ff5db860-0509-43ed-8608-533cd0ee20fd" />   


- In IAM, search for EC2 -> click on **Launch Instance**   
- number of instance --> 1   
- give name --> **mywebserver**   
- Amazon Machine Image --> Amazon Linux is selected (let it be)       
- Architecture --> 64-bit(x86) would be selected- let it be   
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/4c629bc5-291b-4a54-bc3b-debd35de1c84" />

- Next is key-pair, since VM is in cloud and not physically available to us so we need this key-pair to access it.   
Click on **Create New Key Pair**   
<img width="493" alt="image" src="https://github.com/user-attachments/assets/12742ad5-5761-404c-9bac-ed4df5277b11" />
   
Once we click on **Create Key Pair** button in the modal it will download pem file, save it in computer   









