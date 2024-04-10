IAM Roles

Assume Role in AWS :

```json
{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "Statement1",
			"Effect": "Allow",
			"Action": "sts:AssumeRole",
			"Resource": "arn:aws:iam::494855333795:role/OrganizationAccountAccessRole"
		}
	]
}
```

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::494855333795:user/tester"
            },
            "Action": "sts:AssumeRole"
        }
    ]
}
```
This JSON represents an IAM policy that allows the IAM user tester in the AWS account 494855333795 to assume a role.
