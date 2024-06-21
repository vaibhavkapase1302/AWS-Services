MemoryDB for Redis is a durable, in-memory database service that delivers ultra-fast performance. It is purpose-built for modern applications with microservices architectures.

Docs: https://aws.amazon.com/memorydb/

MemoryDB is compatible with Redis, a popular open source data store, enabling you to quickly build applications using the same flexible and friendly Redis data structures, APIs, and commands that they already use today. With MemoryDB, all of your data is stored in memory, which enables you to achieve microsecond read and single-digit millisecond write latency and high throughput. MemoryDB also stores data durably across multiple Availability Zones (AZs) using a Multi-AZ transactional log to enable fast failover, database recovery, and node restarts.

Delivering both in-memory performance and Multi-AZ durability, MemoryDB can be used as a high-performance primary database for your microservices applications, eliminating the need to separately manage both a cache and durable database.

**MemoryDB core components**
- Clusters
- Nodes
- Shards
- Parameter groups
- Subnet Groups
- Access Control Lists
- Users

**Clusters**

A cluster is a collection of one or more nodes serving a single dataset. A MemoryDB dataset is partitioned into shards, and each shard has a primary node and up to 5 optional replica nodes. A primary node serves read and write requests, while a replica only serves read requests. A primary node can failover to a replica node, promoting that replica to the new primary node for that shard.

**Nodes**

A node is the smallest building block of a MemoryDB deployment and runs using an Amazon EC2 instance. Each node runs the Redis version that was chosen when you created your cluster. A node belongs to a shard which belongs to a cluster.

**shard**

A shard is a hierarchical arrangement of nodes, each wrapped in a cluster. Shards support replication. Within a shard, one node functions as the read/write primary node. All the other nodes in a shard function as read-only replicas of the primary node. MemoryDB supports multiple shards within a cluster. This support enables partitioning of your data in a MemoryDB cluster.

**To access your MemoryDB for Redis cluster from an EC2 instance**

Steps to Access the Cluster
- **Verify VPC and Subnet Configuration:** Ensure that the MemoryDB cluster and the EC2 instance are in the same VPC or have VPC peering if they are in different VPCs. Verify that the subnet associated with the EC2 instance is part of the subnet group associated with the MemoryDB cluster.
- **Security Group Configuration:** 
1. MemoryDB Security Group: Inbound Rule: Allow traffic on port 6379 from the EC2 instance's security group.

Ensure that the security group **associated with your MemoryDB cluster** allows inbound traffic on the Redis port (default is 6379) from the security group associated with your EC2 instance.

e.g.
```sh
Type: Custom TCP
Protocol: TCP
Port range: 6379
Source: sg-ec2-instance (Security Group ID of your EC2 instance)
```
2. EC2 Security Group: Outbound Rule: Allow traffic on port 6379.

Ensure that the security group **associated with your EC2 instance** allows outbound traffic on the Redis port (default is 6379).

e.g. 
```sh
Type: Custom TCP
Protocol: TCP
Port range: 6379
Destination: sg-memorydb (Security Group ID of your MemoryDB cluster)
```

- **Install Redis CLI on EC2 Instance:** https://www.tecmint.com/install-redis-in-rhel-8/
- **Connect to the MemoryDB Cluster:** https://docs.aws.amazon.com/memorydb/latest/devguide/getting-startedclusters.connecttonode.html

To connect to a cluster with encryption and authentication enabled, enter this command:

```sh
redis-cli -h Primary or Configuration Endpoint --tls -a 'your-password' -p 6379
```

e.g. 

```sh
redis-cli -h clustercfg.demo-cluster.vkynzv.memorydb.ap-south-1.amazonaws.com --tls -a 'mySecurePassword' -p 6379
```

-h: Specifies the host of the MemoryDB cluster, which is the primary or configuration endpoint.

--tls: Enables TLS encryption for the connection.

-a: Provides the password for authentication.

-p: Specifies the port number (6379 for Redis).
