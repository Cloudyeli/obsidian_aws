## AWS DynamoDB

Amazon DynamoDB is a fully managed, [[serverless]], **key-value** [[NoSQL]] [[database]] designed **to run high-performance applications at any scale**. DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data import and export tools.

Point-in-time recovery (PITR) provides continuous backups of your DynamoDB table data. When enabled, DynamoDB maintains incremental backups of your table for the last 35 days until you explicitly turn it off. It is a customer responsibility to enable PITR on and AWS is responsible for actually performing the backups.

*   Fully managed [[NoSQL]] [[database]] service  
*   **Key/value** store and **document** store  
*   It is a non-relational, key-value type of database
*   Fully serverless service  
*   Push button scaling

![[Pasted image 20221119101132.png]]

### Key Features

* ##### [[Serverless]] 
Fully managed, fault tolerant, service

* ##### Highly available 
99.99% availability SLA – 99.999% for Global Tables!

* ##### [[NoSQL]] type of database with Name / Value structure
Flexible schema, good for when data is not well structured or unpredictable

* ##### Horizontal scaling 
Seamless scalability to any scale with push button scaling or [[Auto Scaling]]

* ##### DynamoDB Accelerator ([[DAX]])
Fully managed in-memory cache for DynamoDB that increases performance (microsecond latency)

* ##### Backup 
Point-in-time recovery down to the second in last 35 days; On-demand backup and restore

* ##### Global Tables 
Fully managed multi-region, multi-master solution

### AWS DynamoDB [[Pricing]]

*   Charged for reading, writing, and storing data
*   On-demand capacity mode
	*   Charged for reads and writes
	*   No need to specify how much capacity is required
	*   Good for unpredictable workloads

*   Provisioned capacity mode  
	*   Specify number of reads and writes per second
	*   Can use [[Auto Scaling]]  
	*   Good for predictable workloads  
	*   Consistent traffic or gradual changes