<img src="https://github.com/vaibhavkapase1302/AWS-Services/blob/main/EC2%20Section/EC2%20Logo.png" width="200" height="200" alt="AWS EC2 Logo">
# EC2: Elastic Compute Cloud

* EC2 is one of the most popular of AWS’ offerings, It is a core service.
* EC2 = Elastic Compute Cloud = Infrastructure as a Service.
 
* It mainly consists of the capability of :
1. Renting virtual machines (EC2)
2. Storing data on virtual drives (EBS)
3. Distributing load across machines (ELB)
4. Scaling the services using an auto-scaling group (ASG)

### Key Pair
AWS uses public-key cryptography to secure the login information for your instance.
- RSA 
- ED25519 [ Not Supported by Windows ]

Private key file format
- .pem [ For use with OpenSSH ]
- .ppk [ For use with PuTTY ]
 
### Security Groups
Security groups act as a firewall for associated instances, controlling both inbound and outbound traffic at the instance level.
- Inbound rules [ Incomming Traffic ]
- Outbound rules [ Outgoing Traffic ]

### Amazon Machine Images (AMIs)
Preconfigured templates for your instances that package the components you need for your server (including the operating system and additional software).

following requirements:
- The Region – AMI IDs are unique to each AWS Region.
- The operating system
- The architecture: 32-bit (i386), 64-bit (x86_64), or 64-bit ARM (arm64)
- The root device type: Amazon EBS or instance store
- The provider (for example, Amazon Web Services)
- Additional software (for example, SQL Server)

### Instance types
Various configurations of CPU, memory, storage, networking capacity, and graphics hardware for your instances.
- General purpose instances
- Compute optimized instances
- Memory optimized instances
- Storage optimized instances
- Accelerated computing
- High-performance computing

e.g. t2.micro

Instance purchasing options:
- On-Demand Instances
- Savings Plans
- Reserved Instances
- Spot Instances
- Dedicated Hosts
- Dedicated Instances

### Amazon EBS volumes
Persistent storage volumes for your data using Amazon Elastic Block Store (Amazon EBS).

### EC2 Instance Connect:
* By using SSH:
* By using RDP Client:
* By session manager
* ec2 serial console

### Ec2 connect through CLI SSH
* Open Windows CLI 
* wite in terminal ```ssh -i "key-pair name" ec2-user@ip-address```



### Apache Web Server:
* Apache is a free and open-source web server that delivers web content through the internet1. It helps in establishing a connection between a server and the browsers of website visitors (Firefox, Google Chrome, Safari, etc.) while delivering files back and forth between them (client-server structure)2.
* In AWS, User data is user data/commands that you can specify at the time of launching your instance. These data/command executes after your EC2 instance starts. You don’t need to SSH into your EC2 instance and run those commands one by one3. You can use EC2 User Data Script to Install Apache Web Server3.


## User Data:
Bootstrap script (configure at first launch)

* When you create an EC2 instance in AWS, you can install the Apache web server on it and use it to serve your web content. User data in AWS refers to the information that you can provide to an EC2 instance when you launch it, such as scripts or commands that you want to run when the instance starts up. 
* This user data can be used to automate the configuration and setup of the EC2 instance, including the installation and configuration of Apache and any other software that you need to run your web applications.

```js
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```

## For the windows Instace

We can  connect the Windows Instance throgh **RDP Client**

When we get this error:

<img src= "https://github.com/vaibhavkapase1302/AWS-Services/blob/main/EC2%20Section/Screenshot%20(488).png" alt="AWS EC2 Logo">

There are mulltiple reasons: How to Resolve Remote Desktop connection Error to connect on network ?  

https://youtu.be/KClNOjHkqL0?si=87gcR4WPO0w_EqpF

https://youtu.be/LznVlHNZWmk?si=_Ml8-zDQhObi7vyI

- To connect windows through RDP we need to **Enable Public IP** whilw creating the instance.
- We have to use the **Public Subnet** to create the Windows Instance. Those who are in the VPC.
- While connecting with the Remote Desktop **Local set-up** should be completed like FRemote Desktop option enable and RDP Port no. for Local machine should be **3389** etc

For specific version type: Windows10, Windows11

AWS doesn't provide a direct Windows 10 AMI in its public catalog, we will proceed with the assumption that you either have a custom Windows 10 AMI or will use a Windows Server AMI.
