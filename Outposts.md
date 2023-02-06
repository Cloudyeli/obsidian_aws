With Outposts, you can run some AWS services on dedicated hardware within your own data center, and that means that you have really low latency access and you can develop and build your applications within your own on-premise data center.

*   AWS Outposts bring native AWS services, infrastructure, and operating models to virtually any data center, co-location space, or on-premises facility.
*   You can use the same AWS [[API]]s, tools, and infrastructure across on-premises and the AWS cloud to deliver a truly consistent hybrid experience.
*   AWS Outposts is designed for connected environments and can be used to support workloads that need to remain on-premises due to low latency or local data processing needs.

AWS Outposts is a fully managed service that extends AWS infrastructure, services, [[API]]s, and tools to customer on-premises. By providing local access to AWS managed infrastructure, AWS Outposts enables customers to build and run applications on premises using the same programming interfaces as in AWS [[Region]]s, while using local compute and storage resources for lower latency and local data processing needs.

*   Deploy AWS infrastructure on-premises and connect AWS services
*   Can extend a [[VPC]] into the on-premises environment
*   Supports several AWS services

### Use cases:

-   Use AWS services on-premises
-   Use AWS [[API]]s on-premises

### Services you can run on AWS Outposts include: 

*   AWS [[EC2]] 
*   AWS [[EBS]]  
*   AWS [[S3]]
*   Amazon [[VPC]]  
*   Amazon [[ECS]]/[[EKS]]
*   Amazon [[RDS]]  
*   Amazon [[EMR]]

An Outpost is a pool of AWS compute and storage capacity deployed at a customer site. AWS operates, monitors, and manages this capacity as part of an AWS Region. You can create [[subnet]]s on your Outpost and specify them when you create AWS resources such as [[EC2]] instances, [[EBS]] volumes, [[ECS]] clusters, and [[RDS]] instances. Instances in Outpost subnets communicate with other instances in the AWS [[Region]] using private [[IP address]]es, all within the same [[VPC]].

![[Pasted image 20221118115319.png]]
