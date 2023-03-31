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

