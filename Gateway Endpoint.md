*   [[EC2]] instance connects to [[S3]] using a private IP
*   [[IAM]] [[policies]] can be applied to endpoints
*   [[Bucket policy\|Bucket policies]] can limit access to [[endpoint]] source
*   A [[route table]] entry is required with the prefix list for [[S3]] and the gateway ID
*   Available for [[S3]] and [[DynamoDB]]

| Destination | Target |
| ------- | -------- |
| pl-6ca54005 (com.amazonaws.ap-southeast-2.s3, 54.231.248.0/22, 54.231.252.0/24, 52.95.128.0/21) | vpce-ID

|  | [[Interface Endpoint]] | [[Gateway Endpoint]] |
| ---- | ----- | ----- |
| **What** | Elastic Network Interface with a Private IP | A gateway that is a target for a specific route
| **How** | Uses DNS entries to redirect traffic | Uses prefix lists in the route table to redirect traffic
| **Which services** | [[API Gateway]], [[CloudFormation]], [[CloudWatch]] etc. | Amazon [[S3]], [[DynamoDB]] 
| **Security** | [[Security Group]]s | VPC Endpoint [[Policies]]

![[Pasted image 20230205180939.png]]
