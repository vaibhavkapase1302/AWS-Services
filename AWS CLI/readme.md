# AWS CLI:
* AWS CLI stands for Amazon Web Services Command Line Interface. 
* It is a tool provided by Amazon Web Services (AWS) that allows users to interact with their AWS resources from the command line.
* It provides a powerful set of commands that enable users to automate and script their AWS management tasks, making it an essential tool for developers, administrators, and DevOps professionals who work with AWS.

### Install or update the AWS CLI

1. Download and run the AWS CLI MSI installer for Windows (64-bit)

[link for Download](https://awscli.amazonaws.com/AWSCLIV2.msi)


2. To confirm the installation, open the Start menu, search for cmd to open a command prompt window, and at the command prompt use the aws --version command.

```js
aws --version
```

### AWS Using CLI
```js
aws configure
```

```js
e.g.
AWS Access Key ID [None]: AKIATLRFSHVP5CUSK6KZ
AWS Secrete Access Key [None]: Fg3tJYOBuSCARII16wmTBbIhvtuFfclv3jJFPN+X
```

## AWS CloudShell
* Cloud Shell is a web-based command-line interface (CLI) that provides a secure and managed environment for interacting with your AWS resources. 
* It runs on AWS infrastructure, so you don't have to worry about configuring any local software or managing any servers.
* Overall, Cloud Shell is a convenient and powerful tool for managing your AWS resources, especially if you prefer working with the CLI or need to automate tasks in your environment.



# S3 Section:

Available Commands
[Documantation link](https://docs.aws.amazon.com/cli/latest/reference/s3/)

* [cp](https://docs.aws.amazon.com/cli/latest/reference/s3/cp.html) ```Copies a local file or S3 object to another location locally or in S3```
```js 
aws s3 cp test.txt s3://mybucket/test2.txt
```

* [ls](https://docs.aws.amazon.com/cli/latest/reference/s3/ls.html) ```List S3 objects``` 
```js
aws s3 ls
```

* [mb](https://docs.aws.amazon.com/cli/latest/reference/s3/mb.html) ```Make Bucket: Creates an S3 bucket```
```js
aws s3 mb s3://mybucket
```

* [mv](https://docs.aws.amazon.com/cli/latest/reference/s3/mv.html) ```Moves a local file or S3 object to another location locally or in S3```
```js 
aws s3 mv test.txt s3://mybucket/test2.txt
```

* [presign](https://docs.aws.amazon.com/cli/latest/reference/s3/presign.html) 
```js
aws s3 presign s3://DOC-EXAMPLE-BUCKET/test2.txt
```

* [rb](https://docs.aws.amazon.com/cli/latest/reference/s3/rb.html) ```Deletes an empty S3 bucket```
```js 
aws s3 rb s3://mybucket
```

* [rm](https://docs.aws.amazon.com/cli/latest/reference/s3/rm.html) ```Deletes an S3 object```
```js 
aws s3 rm s3://mybucket/ --recursive --exclude "another/*"
```

* [sync](https://docs.aws.amazon.com/cli/latest/reference/s3/sync.html) 
```js 
aws s3 sync s3://mybucket s3://mybucket2
```

* [website](https://docs.aws.amazon.com/cli/latest/reference/s3/website.html) ```Set the website configuration for a bucket```
```js
aws s3 website s3://my-bucket/ --index-document index.html --error-document error.html
```

