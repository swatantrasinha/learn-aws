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


In IAM, search for EC2 -> click on **Launch Instance**   
- number of instance --> 1   
- give name --> **mywebserver**   
- Amazon Machine Image --> Amazon Linux is selected (let it be)       
- Architecture --> 64-bit(x86) would be selected- let it be   
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/4c629bc5-291b-4a54-bc3b-debd35de1c84" />

- Next is key-pair, since VM is in cloud and not physically available to us so we need this key-pair to access it.   
Click on **Create New Key Pair**   
<img width="493" alt="image" src="https://github.com/user-attachments/assets/12742ad5-5761-404c-9bac-ed4df5277b11" />
   
Once we click on **Create Key Pair** button in the modal it will download pem file, save it in computer   

- For Sections - **Network Setting** and **Configure Storage** -> whatever is populated let it be
<img width="873" alt="image" src="https://github.com/user-attachments/assets/c86439c3-e84c-4c1d-9b0c-b67ab33d0430" />
<ins>Note</ins> **Ensure Auto-assign public IP** is **enabled** 

## Advanced details
This is optional. Here we are creating a server, if we want that some task will also be there on server when its created then we can use **User Data** in this section.   

<ins>User Data - </ins>  For adding scripts to be executed when the instance starts   

So, in this section of Advanced Details, scroll down to --> **User data - optional**      
and write below in the large textarea   

```script
#!/bin/bash
sudo yum update -y

# Install Apache web server(httpd)
sudo yum install -y httpd

# Start Apache Service
sudo systemctl start httpd

# Enable Apache to start on boot
sudo systemctl enable httpd

# Sample HTML to verify server is runnin
echo "<html><h1>Welcome to Apache Web Server on Amazon Linux</h1></html>">/var/www/html/index.html   

```

- Click on **Launch Instance** button   

<img width="1778" alt="image" src="https://github.com/user-attachments/assets/7613d279-14b7-4ecb-a88c-8c656e6f8259" />    

If we go to EC2 --> we can see the instance running as 1   
<img width="1233" alt="image" src="https://github.com/user-attachments/assets/b9a145a8-420e-4ef7-93b5-c3609dd93a89" />   

Click on this   
It will show the instace created with the name given and the instance will have an **Instance ID** as well   
<img width="1663" alt="image" src="https://github.com/user-attachments/assets/53288967-20c5-4608-a062-28cfbe4999e7" />   

To get more information about instance we can click on the instance id and it will show info like public IP   
<img width="1313" alt="image" src="https://github.com/user-attachments/assets/b49e2611-607b-4566-b13d-7a757e074b68" />   

if we copy the ip and paste in new tab - we should be able to see the HTML   
<ins>Note:</ins> For me when i copy-paste the IP its showing  - This site can’t be reached   

**Security Groups:**   
Network firewall rules that control inbound and outbound traffic for instances.   
To access this in the pahe where we saw public IP(on click of instance id), scroll down and click on 
tab **Security**   

Click on link for Security Group   
<img width="827" alt="image" src="https://github.com/user-attachments/assets/89aa277b-c849-43aa-8f7a-8c6ec0c8665c" />   
In Inbound rules, Port Range 22 and 80 would be there
If its not there (like in my case) then click on Edit Inbound rules -> Add rule   
  
- type: HTTP
- protocol: TCP
- port range: 80
- source : Anywhere-IPv4 and 0.0.0.0/0 will come by itself let it be
  
  Click on **Save Rules**

Now if we go back to the public IP of instance and copy paste in new tab it will show   
<img width="572" alt="image" src="https://github.com/user-attachments/assets/15b2e2d5-a90a-4f4e-9bf4-e8100d91ad5c" />

<ins>Note: </ins> In the address bar, we may need to add **http://** before the ip address   


<img width="415" alt="image" src="https://github.com/user-attachments/assets/6266c531-eaa2-4323-a8ae-e430526941f5" />   

<img width="401" alt="image" src="https://github.com/user-attachments/assets/2d2a5bd8-b13a-4305-ba33-535f73b70567" />   

----
How to SSH into EC2 instance ?   
SSH allows you to control/access a remote machine   
Go to EC2 dashboard --> select instance --> click on **Connect**   
 
<img width="946" alt="image" src="https://github.com/user-attachments/assets/b6fbff4c-c8c7-4f9b-bd54-69acff53bb0d" />

In the Next Page with title **Connect to instance**, in the tabs --> **EC2 Instance Connect** would be selected (let it be)
we will also see **SSH client** (highlighted below) soon  
Note : there would be some username **ec2-user** - let it be  
<img width="902" alt="image" src="https://github.com/user-attachments/assets/1e2f5e9f-3807-43e0-849a-7fbd1f04b2ad" />   



