AWS Guarduty:

Amazon GuardDuty is a threat detection service that continuously monitors, analyzes, and processes specific AWS data sources and logs in your AWS environment. GuardDuty uses threat intelligence feeds, such as lists of malicious IP addresses and domains, and machine learning (ML) models to identify unexpected, and potentially unauthorized activity in your AWS environment. 

This includes the following issues:

- Escalation of privileges, use of exposed credentials, or communication with malicious IP addresses and domains.

- Presence of malware on your Amazon EC2 instances and container workloads, and newly uploaded files in your Amazon S3 buckets.

- Discovery of unusual patterns of login events on your database.

https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_finding-types-active.html

**Finding types**

DefenseEvasion:EC2/UnusualDoTActivity:

This finding informs you that the listed EC2 instance in your AWS environment is behaving in a way that deviates from the established baseline. This EC2 instance doesn't have any recent history of DNS over TLS (DoT) communications with this public DoT server. The Unusual field in the finding details panel can provide information about the queried DoT server.
