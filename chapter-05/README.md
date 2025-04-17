Link to main page : [back-to-main](../README.md)

Go to previous chapter : [Chapter-04](../chapter-04/README.md)

Go to next chapter : [Chapter-06](../chapter-06/README.md)


## Chapter 05: Configure AWS CLI Keys  
AWS CLI is command-line interface which we can use to do a lot of things programatically or via command-line in the AWS account. 
 
Before AWS CLI installation , in terminal if we type   
   
> aws   
   
It will give - command not found   

Steps to install AWS CLI:   

#### 1. click on  this link : [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)   
#### 2. In the LeftNav -> getting started => Install/Update   
#### 3. go to section **AWS CLI install and update instructions**   
#### 4. Expand **macOS**   
#### 5. Scroll to **Install or update the AWS CLI**
#### 6. There are 3 options:   
- GUI Installer
- Command Line Installer - All users
- Command Line - Current user

I followed GUI installer(downloaded .pkg file and next-next-next)   

<ins>Note:</ins> For my windows laptop,
On [this page](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html), I expanded
the **Windows** and clicked on below highlighted link to download windows installer package
and installed it  
<img width="604" alt="image" src="https://github.com/user-attachments/assets/2f4e46a5-9add-4c43-a0cf-4b8a820dd875" />

once installation is done(either in mac or windows), in terminal type   

> aws   

It will show :    

<img width="549" alt="image" src="https://github.com/user-attachments/assets/d7267cf2-8899-48f5-a044-1ffa8e534c9a" />
   
this means its installed   

Now we will configure  
in terminal type   

> aws configure

it will ask for **AWS Access Key Id**    
 
For this, we will go to aws console and then IAM   

---
 
[IAM](https://us-east-1.console.aws.amazon.com/iam/home?region=us-east-1#/home)      

### 1. Inside LeftNav -> Access Management ->  Users -> Create User   
- in username type: **developer**   
- dont click on checkbox **Provide user access to the AWS Management Console - optional**
- click Next   
<img width="1555" alt="image" src="https://github.com/user-attachments/assets/1fb4adc2-4230-44f2-8657-2e16d850dee3" />

### 2. In next page **Set Permission**
- Inside **Permissions Options** section, the first radio button **Add user to group** would be selected (let it be no need to change)   
- In **User groups**, click on checkbox for admins   
**Note:**  ideally this should not be good step as user is for developer so there should be a developer group
(but for now let it be)   
- Inside **Set permissions boundary** section,no action needed   
- Click on **Next**   

<img width="1567" alt="image" src="https://github.com/user-attachments/assets/b1c41fcf-a8d6-4f2a-9ccf-a2470d12846c" />   

### 3. In **Review and create** page no action needed, just click on **Create User** button   
<img width="1566" alt="image" src="https://github.com/user-attachments/assets/109ca7cd-e328-43b5-b256-a4801fe603fb" />

### 4. After submit, we can see user is created   
<img width="1790" alt="image" src="https://github.com/user-attachments/assets/5e28c232-cee9-4a3d-856e-1f29e41bb5f7" />   
   
<ins>Note:</ins> the other user youtube was created in Chapter04 - Point 13   

### 5. Creating Access Key:   

#### a. Click on the user **developer**   
<img width="1664" alt="image" src="https://github.com/user-attachments/assets/d96f2817-c414-4816-8889-fcf81154a3cc" />    

#### b. Click on above highlighted link for **Create Access key**

#### c. new page will appear -->  **Access key best practices & alternatives**
- in usecase -> select for CLI   
- and also check the confirmation checkbox
- click on Next (ignore warning- Alternative Recommended)
<img width="1379" alt="image" src="https://github.com/user-attachments/assets/9a97d352-82f2-47a9-937d-8668e2887e84" />    

#### d. it would take to next page **Set description tag - optional**
<img width="1340" alt="image" src="https://github.com/user-attachments/assets/2498058e-d0e8-4fad-bbf2-b6f67f82423f" />    
this is optional and we can directly click on **Click Access Key** button

#### e. next page it will show access key and secret
<img width="1353" alt="image" src="https://github.com/user-attachments/assets/97f25f10-f1c6-4de7-84ea-2583880dd7a4" />
save this access key & secret (or download .csv file)

#### f. click on Done

--- 

### Configure AWS with access key

in terminal give command,   
> aws configure

it will ask for:
- AWS Access Key ID - paste (created above)

- AWS Secret Access Key - paste (created above)

- Default region name : ap-south-1 (we can see in topNav if we click Global -> nearest is Mumbai)
<img width="278" alt="image" src="https://github.com/user-attachments/assets/72227181-30f6-4c90-a35c-51127cfb396c" />

- Default output format - json   

 thats it **Done**   
<img width="505" alt="image" src="https://github.com/user-attachments/assets/e70ff6f4-67e5-4ae9-b953-f471f4b6d07a" />  

---
### Check for "Configure AWS"   
Now if we type in terminal:   

> aws s3 ls

it will give list of s3 buckets   
<img width="280" alt="image" src="https://github.com/user-attachments/assets/8815a938-5e2a-4d65-ac42-55a991f1db52" />   

<ins>Note: </ins> although its not showing anything because there is no S3 bucket yet but the command is **valid**   

---

## Precautions: What Not To Do

**Be very very careful for credentials**

### 1. Say we are developers then untill we really know that we need this access key we should not be storing it.
There are other options to access EC2 instance and other features(which we may see later)

### 2. In mac or linux, if we go to terminal (there will be similar in windows- need to check)   

then there is a hidden folder with name **.aws** 
below command can expose the credentials   
<img width="495" alt="image" src="https://github.com/user-attachments/assets/53820182-5ab3-4e29-8cb0-01e6b8126642" />

### 3. <ins>Please Note: </ins> **Anybody working with EC2 machine should never go to an EC2 instance and configure credentials in EC2 machines**.
Doing this **even accidently could be a nightmare**. This can **really impact the bill**

### 4. To deactivate access keys go to IAM:
- Access management -> users
- click on the user
- go to tab -> **Security credentials**
- scroll to section  **Access keys**
- inside the dropdown **Actions**, there is option **deactivate**

<img width="1757" alt="image" src="https://github.com/user-attachments/assets/ce5c2fc0-9b01-471e-9588-3d50436402de" />    

Here, we can deactivate and then using same dropdown we can delete the access key
Once deleted, we cannot get results for    
> aws s3 ls











