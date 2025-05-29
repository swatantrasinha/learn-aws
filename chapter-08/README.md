## Chapter 08: AWS EBS Service

EBS stands for **Elastic Block Store**. It is a cloud based storage service that provides durable, high-performance block storage for use with Amazon EC2 instances.   
It works like virtual hard-drive and allows store & data access data even when EC2 instance are stopped or terminated.   

Here we will see:      
- How to add storage in EC2 instance 
- How to increase size of storage
- add additional disk in storage
- backup for disk space
- retrieve from backup
- transfer snapshot backup from one region to another

While creating EC2 instance, we saw section **Configure Storage** ,    
<img width="1251" alt="image" src="https://github.com/user-attachments/assets/89da2c32-73ce-47fa-8988-519ce04c41b0" />   
this 8 GB general purpose is of form EBS   
If we click on Advance, it will show **EBS Volumne**   
<img width="807" alt="image" src="https://github.com/user-attachments/assets/40d339d2-19d0-4456-b52d-6c119c8d2fec" />   

Note: 
1. We can attach multiple EBS for an EC2 instance.   
2. EBS provides persistent, fasts-storage that ensures your data is saved even if the EC2 instance is stopped or restarted, making it ideal for database workloads.   
<ins>usecase:</ins> We are hosting a MySQl or PostgresSQL database and need reliable high performance storage to handle frequent readwrite operations.   

3. Region and AZ specific

4. Build-in Redundancy

5. Different Volume Types   
<img width="807" alt="image" src="https://github.com/user-attachments/assets/e0615075-bf66-4cc3-be06-96c22f8cb9ef" />


6. Allows encryption and snapshot for backup
<img width="807" alt="image" src="https://github.com/user-attachments/assets/a5435d2c-6d11-462c-9548-5f81f9501871" />

7. Scalaable(Volume can be resizeable)
- No data loss will occur during resizing
- No need to restart EC2 instance during the process











