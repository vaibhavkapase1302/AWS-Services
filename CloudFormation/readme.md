# AWS CloudFormation
* AWS CloudFormation is a service provided by Amazon Web Services (AWS) that allows you to define and manage infrastructure as code. 
* You create a template that describes all the AWS resources that you want and CloudFormation takes care of provisioning and configuring those resources for you.
* It enables you to create and manage AWS resources such as EC2 instances, VPCs, S3 buckets, and more in a predictable and repeatable manner.
* With AWS CloudFormation, you can describe your infrastructure in a template file using JSON or YAML syntax. 
* The template file contains the configuration and properties for the AWS resources you want to create. 
* Once you have defined your template, you can use CloudFormation to create, update, or delete your resources.
* Overall, AWS CloudFormation helps you manage your infrastructure more efficiently and with greater consistency by treating it as code.

[AWS CloudFormation Documantation Link](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-template-resource-type-ref.html)

## Templates in CloudFormation
* Templates in CloudFormation provide a way to create and manage AWS resources in a repeatable and automated way, allowing for easy deployment and management of complex systems. 
* CloudFormation uses these templates as blueprints for building your AWS resources.


### How CloudFormation Works?
<!-- ![T](https://github.com/vaibhavkapase1302/AWS-Services/blob/main/CloudFormation/How%20CloudFormation%20Works.png) -->
<img src="https://github.com/vaibhavkapase1302/AWS-Services/blob/main/CloudFormation/How%20CloudFormation%20Works.png" alt="GitHub Logo" width="800" height="500">

### Components of Template:
* Format Version 
* Description
* Metadata
* Parameters
* Rules
* Mappings
* Conditions
* Transform
* Resources

#### 🏷️ Parameters: These are user-defined values that can be passed to the template at runtime to customize resource creation.
#### 🏷️ Resources: These are the AWS resources that are created and configured by the CloudFormation template, such as EC2 instances, S3 buckets, and DynamoDB tables.
#### 🏷️ Outputs: These are values that are returned by the CloudFormation stack after it is created, such as the URL of a load balancer or the ID of a newly created EC2 instance.

## Yaml code for S3
```js
jj
```

## 
