A Database is a structured set of data held in a computer, especially one that is accessible in various ways.

![[Pasted image 20221121190635.png]]

| Database    | Use cases                                                                                                       | AWS services                                                                                                                                                                                                                                                                                                                                                                                            |
| ----------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Relational  | Traditional applications, enterprise resource planning ([[ERP]]), customer relationship management (CRM), ecommerce | Amazon [[Aurora]] — Designed for unparalleled high performance and availability at global scale with full [[MySQL]] and PostgreSQL compatibility<br><br>Amazon [[RDS]] — Set up, operate, and scale a relational database in the cloud with just a few clicks<br><br>Amazon [[Redshift]] — Accelerate your time to insights with fast, easy, and secure cloud data warehousing at scale |
| Key-value   | High-traffic web applications, ecommerce systems, gaming applications                                           | Amazon [[DynamoDB]] — Fast, flexible [[NoSQL]] database service for single-digit millisecond performance at any scale                                                                                                                                                                                                                                                                           |
| In-memory   | Caching, session management, gaming leaderboards, geospatial applications                                       | Amazon [[ElastiCache]] — Unlock microsecond latency and scale with in-memory caching<br><br>Amazon [[MemoryDB]] for Redis — Redis-compatible, durable, in-memory database service for ultra-fast performance                                                                                                                                                                                      |
| Document    | Content management, catalogs, user profiles                                                                     | Amazon [[DocumentDB]] (with MongoDB compatibility) — Scale [[JSON]] workloads with ease using a fully managed document database service                                                                                                                                                                                                                                                                 |
| Wide column | High-scale industrial apps for equipment maintenance, fleet management, and route optimization                  | Amazon [[Keyspaces]] — A scalable, highly available, and managed Apache Cassandra–compatible database service                                                                                                                                                                                                                                                                                       |
| Graph       | Fraud detection, social networking, recommendation engines                                                      | Amazon [[Neptune]] — Build and run graph applications with highly connected datasets                                                                                                                                                                                                                                                                                                                |
| Time series | Internet of Things ([[IoT]]) applications, DevOps, industrial telemetry                                             | Amazon [[Timestream]] — Fast, scalable, serverless time series database                                                                                                                                                                                                                                                                                                                             |
| Ledger      | Systems of record, supply chain, registrations, banking transactions                                            | Amazon Ledger Database Service ([[QLDB]]) — Maintain an immutable, cryptographically verifiable log of data changes                                                                                                                                                                                                                                                                                 |


## AWS Databases

##### Database on [[EC2]]  
*   Need full control over instance and database
*   Third-party database engine (not available in RDS)

##### Amazon [[RDS]]
*   Need traditional relational database  
*   e.g. Oracle, PostgreSQL, Microsoft SQL, MariaDB, MySQL
*   Data is well-formed and structured

##### Amazon [[Aurora]]
*   Is an AWS database offering in the [[RDS]] family
*   MySQL and PostgreSQL-compatible relational database built for the cloud
*    Five times faster than standard [[MySQL]] databases and three times faster than standard PostgreSQL databases

##### Amazon [[DynamoDB]]
*   NoSQL database  
*   In-memory performance
*   High I/O needs
*   Dynamic scaling

##### Amazon [[RedShift]]
*   Data warehouse for large volumes of aggregated data

##### Amazon [[ElastiCache]]
*   Fast temporary storage for small amounts of data
*   In-memory database

##### Amazon [[EMR]]
*   Analytics workloads using the Hadoop framework

##### Amazon Neptune


## Relational Databases

![[Pasted image 20221119085332.png]]

## Types of Non-Relational DB (NoSQL)

*   Key-value – e.g. Amazon [[DynamoDB]]
*   Graph – e.g. Amazon [[Neptune]]
*   Document – e.g. MongoDB

![[Pasted image 20221119085353.png]]

## Relational vs. Non-Relational Database

Key differences are how data are managed and how data are stored

| Relational | Non-Relational |
| ----------| --------------- |
| Organized by tables, rows and columns | Varied data storage models
| Rigid schema ([[SQL]]) | Flexible schema ([[NoSQL]]) – data stored in key-value pairs, columns, documents or graphs
| Rules enforced within database | Rules can be defined in application code (outside database)
| Typically scaled vertically | Scales horizontally
| Supports complex queries and joins | Unstructured, simple language that supports any kind of schema
| Amazon [[RDS]], Oracle, [[MySQL]], IBM DB2, PostgreSQL | Amazon [[DynamoDB]], MongoDB, Redis, Neo4j

## Operational vs. Analytical Databases

Key differences are use cases and how the database is optimized

*   Operational DBs receive data from applications (Amazon [[RDS]])
*   Data Warehouse performs analytics (Amazon [[Redshift]])

![[Pasted image 20221119091128.png]]

| Operational / transactional | Analytical |
| -------------- | ------------- |
| Online Transaction Processing ([[OLTP]]) | Online Analytics Processing ([[OLAP]]) – the source data comes from OLTP DBs
| Production DBs that process transactions. E.g. adding customer records, checking stock availability (INSERT, UPDATE, DELETE) | Data warehouse. Typically, separated from the customer facing DBs. Data is extracted for decision making 
| Short transactions and simple queries | Long transactions and complex queries
| Relational examples: Amazon [[RDS]], Oracle, IBM DB2, [[MySQL]] | Relational examples: Amazon [[RedShift]], Teradata, HP Vertica 
| Non-relational examples: MongoDB, Cassandra, Neo4j, HBase | Non-relational examples: Amazon [[EMR]], MapReduce 

![[Pasted image 20221119090942.png]]
