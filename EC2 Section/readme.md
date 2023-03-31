# EC2: Elastic Compute Cloud

* EC2 is one of the most popular of AWS’ offering, It is a core service.
* EC2 = Elastic Compute Cloud = Infrastructure as a Service.

* It mainly consists in the capability of :
1. Renting virtual machines (EC2)
2. Storing data on virtual drives (EBS)
3. Distributing load across machines (ELB)
4. Scaling the services using an auto-scaling group (ASG)

### EC2 Instance Connect:
* By using SSH:
* By using RDP Client:

### Apache Web Server:
* Apache is a free and open-source web server that delivers web content through the internet1. It helps in establishing a connection between a server and the browsers of website visitors (Firefox, Google Chrome, Safari, etc.) while delivering files back and forth between them (client-server structure)2.
* In AWS, User data is user data/commands that you can specify at the time of launching your instance. These data/command executes after your EC2 instance starts. You don’t need to SSH into your EC2 instance and run those command one by one3. You can use EC2 User Data Script to Install Apache Web Server3.


## User Data:

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
