# SQS
* AWS SQS (Amazon Simple Queue Service) is a fully managed message queuing service offered by Amazon Web Services.
*  It allows applications to send, store, and receive messages between software components or microservices, without the need for those components to be running at the same time.

[SQS AWS Documantation Link](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html)

It offers two types of queues: 
1)  Standard Queue: This type of queue provides a high throughput and ***flexible*** queuing system that supports message deduplication, at-least-once delivery, and is suitable for most use cases.
2) FIFO (First-In-First-Out) Queue: This type of queue provides ***strict message ordering*** and exactly-once processing of messages, making it suitable for applications that require deterministic ordering of messages, such as financial systems, or e-commerce applications.

AWS SQS also integrates with other AWS services such as AWS Lambda, AWS EC2, AWS SNS, and AWS S3, making it a versatile messaging platform that can be used in a wide range of use cases, including application decoupling, event-driven architecture, and asynchronous processing of workloads.

## Queue 
* In AWS SQS, a queue is a logical container for messages. 
*  It allows applications to send messages to, and receive messages from, the queue. 
*   Messages in a queue are stored until they are consumed by a consumer or deleted.

A queue can be thought of as a buffer or a waiting area for messages. When a producer sends a message to a queue, the message is stored in the queue until a consumer retrieves it. The messages in a queue are processed in a first-in, first-out (FIFO) order by default, although this behavior can be modified for certain use cases.

##  dead-letter queues
