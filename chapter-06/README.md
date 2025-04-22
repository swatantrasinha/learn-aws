## Chapter 06: EC2   


Link to main page : 
[back-to-main](../README.md)



Go to previous chapter : 
[Chapter-05](../chapter-05/README.md)


Go to next chapter : 
[Chapter-07](../chapter-07/README.md)


## Introduction to Amazon Elastic Compute Cloud EC2   

### Compute Services:   

1. Processor   
2. Memory   
3. Hard Disk Drive or SSD   
4. Network Interface Card (NIC) - card that allow connecting to internet - can be wifi/wireless card/wired ether port etc    
5. Network Switch or Router   

 <ins>Note:</ins> Server is not our regular laptop   

### Virtualization
By virtualization we can install some software on top of some hardware in the machine and this allows the ability of virtualization  

Type1 & Type 2 Virtualization   

<img width="232" alt="image" src="https://github.com/user-attachments/assets/407edc84-85b1-43a1-bb03-59523cd609dc" />

The main key thing in virtualization is ***HyperVisor***      
- Hypervisor is an abstraction of the hardware      
- Virtual Hardware is given to the OS   
- Portability   


### Amazon Elastic Compute Cloud - EC2   

<img width="263" alt="image" src="https://github.com/user-attachments/assets/ddd2281a-da50-4cef-a9db-93b72c095d82" />   
 <br />
<img width="230" alt="image" src="https://github.com/user-attachments/assets/1cbe77ba-5077-4f40-b014-bd08de8e578b" />   
 <br />

 While connecting the machines using SSH, please remember to change file/key permission to 400(read-only)   
 **chmod 400 key.pem**   

### EC2- user data and meta data
- user-data: when we spin-up an EC2 machine, we are given a user box where we can enter some commands/codes and these commands/codes are called user-data. It will run only when the first time instance starts.    

- meta-data: information about instance. 
url for meta data is http://169.254.269.254/latest/meta-data   
   
curl then above url will show meta-data
   


   


 
