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

## Stack:
In AWS CloudFormation, a stack is a collection of AWS resources that you can manage as a single unit.
* For example, suppose you want to create a web application that consists of an EC2 instance, an S3 bucket for storing static content, and an RDS database for storing dynamic data. You can use CloudFormation to create a stack that includes all of these resources, with their respective configurations. You can then manage the stack as a single unit, making it easier to create, update, and delete your web application as needed.

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

## Yaml code for S3
```yml
Resources:
  MyBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: my-bucket

  MyTopic:
    Type: AWS::SNS::Topic
    Properties:
      DisplayName: my-topic
```

#### 🏷️ Parameters: These are user-defined values that can be passed to the template at runtime to customize resource creation.
#### 🏷️ Resources: These are the AWS resources that are created and configured by the CloudFormation template, such as EC2 instances, S3 buckets, and DynamoDB tables.
* In a CloudFormation template, Resources: is a top-level section that defines the AWS resources that you want to create or manage. 
* This section is required in every CloudFormation template and is used to declare the resources that will be created, updated or deleted during stack creation or stack update.

Here's an example of a CloudFormation template that defines two resources, an Amazon S3 bucket and an Amazon SNS topic:

#### 🏷️ Outputs: These are values that are returned by the CloudFormation stack after it is created, such as the URL of a load balancer or the ID of a newly created EC2 instance.



## 
