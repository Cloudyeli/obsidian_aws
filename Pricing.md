## Fundamentals of [[Pricing]]:  

• Compute – CPU/RAM and duration  
• Storage – quantity of data stored or allocated  
• Outbound data transfer – data leaving an AWS Region

![[Pasted image 20221119213607.png]]

### Pay-as-you-go

*   Easily adapt to changing business needs  
*   Improved responsiveness to change  
*   Adapt based on needs, not forecasts  
*   Reduce risk over overpositioning of missing capacity

### Reserved Instances (save when you reserve )

*   Invest in reserved capacity (e.g. [[RDS]] and [[EC2]])  
* Save up to 75% compared to on-demand (pay-as- you-go)  
* The more you pay **upfront** the greater the discount

### Pay less by using more

*   Pay less using volume-based discounts  
* Tiered pricing means the more you use the lower the unit pricing
*  Also applies to AWS [[Fargate]] and AWS [[Lambda]] usage.

![[Pasted image 20221120075302.png]]

### AWS [[EC2 Pricing]]

EC2 instance pricing various depending on many variables. 1) The type of buying option 2) Selected Ami 3) Selected instance type 4) Region 5) Data in/out 6) Storage capacity

* ##### On-Demand (Pay-as-you-go)
Standard rate - no discount; no commitments; dev/test, short-term, or unpredictable workloads

![[Pasted image 20221119220503.png]]

* ##### Spot Instances
Bid for unused capacity; up to 90% discount; can be terminated at any time; workloads with flexible start and end times

![[Pasted image 20221119220540.png]]

2-minute warning if AWS need to reclaim capacity – available via instance [[metadata]] and [[CloudWatch Events]]

-   **Spot Instance**: One or more EC2 instances
-   **Spot Fleet**: launches and maintains the number of Spot / On-Demand instances to meet specified target capacity
-   **EC2 Fleet**: launches and maintains specified number of Spot / On-Demand / Reserved instances in a single **[[API]] call**
	-   Can define separate OD/Spot capacity targets, bids, instance types, and AZs
-   **Spot Block**: Requirement: Uninterrupted for 1-6 hours

* ##### Dedicated Hosts
Physical server dedicated for your use; Socket/core visibility, host affinity; pay per host; workloads with server-bound software licenses

![[Pasted image 20221119220659.png]]

* ##### Dedicated Instances
Physical isolation at the host hardware level from instances belonging to other customers; pay per instance

![[Pasted image 20221119220728.png]]

* ##### Reserved Instances
1 or 3-year commitment;  up to 75% discount; steady-state, predictable workloads and reserved capacity

![[Pasted image 20221119220602.png]]

* ##### Savings Plans
Commitment to a consistent amount of usage ([[EC2]] + [[Fargate]] + [[Lambda]]); Pay by $/hour; 1 or 3-year commitment

### AWS [[S3]] Pricing

- ##### Storage class
e.g. Standard or IA

- ##### Storage quantity
data volume stored in your buckets on a per GB basis

- ##### Number of requests
the number and type of requests, e.g. GET, PUT, POST, LIST, COPY 

* ##### Lifecycle transitions requests
moving data between storage classes
    
- ##### Data transfer
data transferred out of an S3 [[region]] is charged

### AWS [[S3 Glacier]] Pricing

![[Pasted image 20221120065722.png]]

### AWS [[EBS]] Pricing

* ##### Volumes
volume storage for all [[EBS volume]]s type is charged by the amount of GB provisioned per month

* ##### Snapshots
based on the amount of space consumed by snapshots in [[S3]]. Copying snapshots is charged on the amount of data copied across [[region]]s

* ##### Data transfer
inbound data transfer is free, outbound data transfer charges are tiered

### AWS [[RDS]] Pricing

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

### AWS [[DynamoDB]] Pricing

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

### AWS [[CloudFront]] Pricing

* ##### Traffic distribution
data transfer and request pricing, varies across [[region]]s, and is based on the [[edge location]] from which the content is served

* ##### Requests
the number and type of requests ([[HTTP]] or [[HTTPS]]) and the geographic [[region]] in which they are made

* ##### Data transfer out
quantity of data transferred out of CloudFront edge locations;
There are additional chargeable items such as invalidation requests, field-level [[encryption]] requests, and custom [[SSL]] certificates

### AWS [[Lambda]] Pricing

*   Number of requests  
*   Duration of request – rounded up to the nearest millisecond
-   Price is dependent on the amount of memory allocated to the function
-   Free tier includes 1M free requests per month and 400,000 GB-seconds of compute time

### [[LightSail]] Database Pricing

Amazon LightSail databases are available in Standard and High Availability plans.

Amazon LightSail is very affordable.

* High Availability plans add redundancy and durability to your database, by automatically creating standby database in a separate Availability Zone.
* Amazon LightSail plans are billed on an on-demand hourly rate, so you pay only for what you use.

For every Amazon LightSail plan you use, AWS charges you the fixed hourly price, up to the maximum monthly plan cost.

### AWS [[API]] Pricing

*   Query the prices of AWS services  
*   **Price List Service API (AKA the Query API)** – query with JSON
*   **AWS Price List API (AKA the Bulk API)** – query with HTML
*   Alerts via Amazon SNS when prices change