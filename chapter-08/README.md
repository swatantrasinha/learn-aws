## Chapter 08: AWS EBS Service
<details>
  <summary>EBS Overview</summary>

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
</details>

<details>
  <summary>Important Notes: </summary>

1. We can attach multiple EBS for an EC2 instance.   
2. EBS provides persistent, fasts-storage that ensures your data is saved even if the EC2 instance is stopped or restarted, making it ideal for database workloads.   
<ins>usecase:</ins> We are hosting a MySQl or PostgresSQL database and need reliable high performance storage to handle frequent readwrite operations.   

3. Region and AZ specific - Lets say Region Mumbai has 3 AZs - A,B and C. If we create EBS on AZ 'A', and create EC2 instance on AZ 'B' then the EC2 instance can't use the EBS.

4. Build-in Redundancy

5. Different Volume Types   
<img width="807" alt="image" src="https://github.com/user-attachments/assets/e0615075-bf66-4cc3-be06-96c22f8cb9ef" />


6. Allows encryption and snapshot for backup
<img width="807" alt="image" src="https://github.com/user-attachments/assets/a5435d2c-6d11-462c-9548-5f81f9501871" />

7. Scalaable(Volume can be resizeable)
- No data loss will occur during resizing   
- No need to restart EC2 instance during the process

</details>

---
<ins>Practical</ins>   

<details>
  <summary>1. Create EBS while creating EC2 instance </summary>
Here we will see EBS behaviour when EC2 instance is deleted

In EC2 dashboard --> Left Nav -> Elastic Block Store --> Volumes
It will show no volumes   

Lets create an instance first   
Case A:      
We will create as we used to do in previous chapter - lets give instance name (mywebserver-29May2025) and other select by default.   
In EC2 dashboard we can see this instance.   
Now go to LeftNav -> Elastic Block Store -> Volume    
We can see a volume   
<img width="1615" alt="image" src="https://github.com/user-attachments/assets/f49a3080-5196-4aaa-87b1-2bd3b3c0a560" />   
Note: Please ensure region is same for instance and EBS   

**While creating the EC2 instance, as we have selected all bydefault so if we terminate/delete the EC2 instance this volume in EBS will also gets deleted.**   

Case B:   
We will create one more EC2 instance but we will keep eceyrthing default other than **Configure Storage**    
<img width="823" alt="image" src="https://github.com/user-attachments/assets/758f8452-7ee6-4d33-a2ae-5cf654d4b5b3" />
Here will select : Delete on termination --> No   
In EC2 Dashboard , we can see the instance running. If we see the details in Storage section -> horizontal scroll -> we will see **Delete on termination** is **No**   
<img width="1521" alt="image" src="https://github.com/user-attachments/assets/8beaf345-9179-4cdb-8e93-a608292c506f" />

Now go to LeftNav -> Elastic Block Store -> Volume  
We can see a volume there    
However now even if we delete/terminate EC2 instance , this **volume will not get deleted.**      
We will delete/terminate it manually.     
<img width="1668" alt="image" src="https://github.com/user-attachments/assets/53a6733c-a275-467a-9d0e-ead3996e6867" />

Note: Since EC2 instance attached(the EC2 with which this volume created) is already deleted so detach option is not available.   
</details>

---
<details>
  <summary> 2. Create and Attach EBS to EC2 instance  </summary>
  
</details>























