*   An [[ENI]] is created in the [[subnet]]
*   Each interface endpoint can connect to one of many AWS services
*   [[EC2]] instance connects to public AWS service using a private IP
*   Or you can connect to an AWS [[PrivateLink]] powered service

|  | [[Interface Endpoint]] | [[Gateway Endpoint]] |
| ---- | ----- | ----- |
| **What** | Elastic Network Interface with a Private IP | A gateway that is a target for a specific route
| **How** | Uses DNS entries to redirect traffic | Uses prefix lists in the route table to redirect traffic
| **Which services** | [[API Gateway]], [[CloudFormation]], [[CloudWatch]] etc. | Amazon [[S3]], [[DynamoDB]] 
| **Security** | [[Security Group]]s | VPC Endpoint [[Policies]]

![[Pasted image 20230205180600.png]]


