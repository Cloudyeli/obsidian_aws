## AWS Relational Database Service (RDS) 

Amazon Relational Database Service (Amazon RDS) is **a collection of managed services that makes it simple to set up, operate, and scale databases in the cloud**.

-   RDS uses [[EC2]] instances, so you must choose an instance family/type

![[Pasted image 20221119094006.png]]

-   Relational [[database]]s are known as Structured Query Language ([[SQL]]) databases
-   RDS is an Online Transaction Processing ([[OLTP]]) type of database
-   Easy to setup, highly available, fault tolerant, and scalable
-   Common use cases include **online stores** and **banking systems**
-   Can encrypt your Amazon RDS instances and snapshots at rest
-   [[Encryption]] uses AWS Key Management Service ([[KMS]])

### Amazon RDS supports the following database engines:

-   SQL Server, Oracle, [[MySQL]] Server, PostgreSQL, [[Aurora]], MariaDB
-   **Scales up** by increasing [[EC2]] instance size (compute and storage)

![[Pasted image 20221119094207.png]]

### Disaster Recovery ([[DR]]) and Scaling Out (Horizontally)

Multi-[[AZ]] creates a passive standby. Primarly used for disaster Recovery. Application servers can read from the read replica and write to the master. Read Replicas are used for scaling database queries (reads)

-   Disaster recovery with Multi-[[AZ]] option
-   Read replicas option for read heavy workloads (scales out for reads/queries only)

![[Pasted image 20221119094257.png]]


# ___

Amazon Relational Database Service (Amazon RDS) is a managed service that makes it easy to set up, operate, and scale a relational database in the cloud.

Relational databases are known as Structured Query Language (SQL) databases.

Non-relational databases are known as NoSQL databases.

RDS is an Online Transaction Processing (OLTP) type of database.

RDS features and benefits:

-   SQL type of database.
-   Can be used to perform complex queries and joins.
-   Easy to setup, highly available, fault tolerant, and scalable.
-   Used when data is clearly defined.
-   Common use cases include online stores and banking systems.

Amazon RDS supports the following database engines:

-   SQL Server.
-   Oracle.
-   MySQL Server.
-   PostgreSQL.
-   Aurora.
-   MariaDB.

Aurora is Amazon’s proprietary database.

RDS is a fully managed service and you do not have access to the underlying EC2 instance (no root access).

The RDS service includes the following:

-   Security and patching of the DB instances.
-   Automated backup for the DB instances.
-   Software updates for the DB engine.
-   Easy scaling for storage and compute.
-   Multi-AZ option with synchronous replication.
-   Automatic failover for Multi-AZ option.
-   Read replicas option for read heavy workloads.

A DB instance is a database environment in the cloud with the compute and storage resources you specify.

Encryption:

-   You can encrypt your Amazon RDS instances and snapshots at rest by enabling the encryption option for your Amazon RDS DB instance.
-   Encryption at rest is supported for all DB types and uses AWS KMS.
-   You cannot encrypt an existing DB, you need to create a snapshot, copy it, encrypt the copy, then build an encrypted DB from the snapshot.

DB Subnet Groups:

-   A DB subnet group is a collection of subnets (typically private) that you create in a VPC and that you then designate for your DB instances.
-   Each DB subnet group should have subnets in at least two Availability Zones in each region.
-   It is recommended to configure a subnet group with subnets in each AZ (even for standalone instances).

AWS Charge for:

-   DB instance hours (partial hours are charged as full hours).
-   Storage GB/month.
-   I/O requests/month – for magnetic storage.
-   Provisioned IOPS/month – for RDS provisioned IOPS SSD.
-   Egress data transfer.
-   Backup storage (DB backups and manual snapshots).

Scalability:

-   You can only scale RDS up (compute and storage).
-   You cannot decrease the allocated storage for an RDS instance.
-   You can scale storage and change the storage type for all DB engines except MS SQL.

RDS provides multi-AZ for disaster recovery which provides fault tolerance across availability zones:

-   Multi-AZ RDS creates a replica in another AZ and synchronously replicates to it (DR only).
-   There is an option to choose multi-AZ during the launch wizard.
-   AWS recommends the use of provisioned IOPS storage for multi-AZ RDS DB instances.
-   Each AZ runs on its own physically distinct, independent infrastructure, and is engineered to be highly reliable.
-   You cannot choose which AZ in the region will be chosen to create the standby DB instance.

Read Replicas – provide improved performance for reads:

-   Read replicas are used for read heavy DBs and replication is asynchronous.
-   Read replicas are for workload sharing and offloading.
-   Read replicas provide read-only DR.
-   Read replicas are created from a snapshot of the master instance.
-   Must have automated backups enabled on the primary (retention period > 0).

![amazon-rds-scaling-dr](https://digitalcloud.training/wp-content/uploads/2022/02/amazon-rds-scaling-dr.png)

### AWS RDS [[Pricing]]

* ##### Clock hours of server uptime
amount of time the DB instance is running

* ##### Database characteristics
e.g. database engine, size and memory class

* ##### Database purchase type
e.g. On-Demand, Reserved;
Number of database instances

* ##### Provisioned storage
backup is included up to 100% of the size of the DB

* ##### Additional storage
the amount of storage in addition to the provisioned storage is charged per GB per month

* ##### Requests
the number of input and output requests to the DB

* ##### Deployment type
single [[AZ]] or multi-AZ

* ##### Reserved Instances ([[RI]])
RDS RIs can be purchased with No Upfront, Partial Upfront, or All Upfront terms. Available for [[Aurora]], [[MySQL]], MariaDB, Oracle and [[SQL]] Server