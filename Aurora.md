Amazon Aurora is **a relational database management system ([[RDBMS]]) built for the cloud with full [[MySQL]] and PostgreSQL compatibility**. Aurora gives you the performance and availability of commercial-grade [[database]]s at one-tenth the cost.

-   Amazon Aurora is an AWS database offering in the [[RDS]] family
-   Amazon Aurora is a [[MySQL]] and PostgreSQL- compatible relational database built for the cloud
-   Amazon Aurora is up to five times faster than standard MySQL databases and three times faster than standard PostgreSQL databases
-   Amazon Aurora features a distributed, fault-tolerant, self- healing storage system that auto-scales up to 128TB per database instance

![[Pasted image 20221119100009.png]]

### Aurora Fault Tolerance  

*   Fault tolerance across 3 AZs  
*   Single logical volume  
*   Aurora Replicas scale-out read requests  
*   Can promote Aurora Replica to be a new primary or create new primary  
*   Can use [[Auto Scaling]] to add replicas

### Key Features

* ##### High performance and scalability
Offers high performance, self-healing storage that scales up to 128TB, point-in-time recovery and continuous backup to S3

* ##### DB compatibility 
Compatible with existing [[MySQL]] and PostgreSQL open source databases

* ##### Aurora Replicas
In-region read scaling and failover target – up to 15 (can use [[Auto Scaling]]) 

* ##### MySQL Read Replicas
Cross-region cluster with read scaling and failover target – up to 5 (each can have up to 15 Aurora Replicas)

* ##### Global Database
Cross-region cluster with read scaling (fast replication / low latency reads). Can remove secondary and promote

* ##### Multi-Master Cluster
Scales out writes within a region. Share a Storage Volume
![[Pasted image 20221201073212.png]]

* ##### Serverless
On-demand, autoscaling configuration for Amazon Aurora - does not support read replicas or public IPs (can only access through [[VPC]] or [[Direct Connect]] - not [[VPN]])