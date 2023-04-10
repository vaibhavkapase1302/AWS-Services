# SQS
* AWS SQS (Amazon Simple Queue Service) is a fully managed message queuing service offered by Amazon Web Services.
*  It allows applications to send, store, and receive messages between software components or microservices, without the need for those components to be running at the same time.

It offers two types of queues: 
1)  Standard Queue: This type of queue provides a high throughput and ***flexible*** queuing system that supports message deduplication, at-least-once delivery, and is suitable for most use cases.
2) FIFO (First-In-First-Out) Queue: This type of queue provides ***strict message ordering*** and exactly-once processing of messages, making it suitable for applications that require deterministic ordering of messages, such as financial systems, or e-commerce applications.

AWS SQS also integrates with other AWS services such as AWS Lambda, AWS EC2, AWS SNS, and AWS S3, making it a versatile messaging platform that can be used in a wide range of use cases, including application decoupling, event-driven architecture, and asynchronous processing of workloads.

## Queue 
