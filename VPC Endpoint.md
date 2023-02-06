A VPC endpoint is your private [[VPC]] connection to public AWS services.
You can create an interface VPC endpoint to connect to services powered by AWS [[PrivateLink]], including many AWS services.

For each [[subnet]] that you specify from your VPC, we create an endpoint network interface in the subnet and assign it a private [[IP address]] from the subnet address range. An endpoint network interface is a requester-managed network interface; you can view it in your AWS account, but you can't manage it yourself.

##### - VPC [[Interface Endpoint]]s
##### - VPC [[Gateway Endpoint]]s

|  | [[Interface Endpoint]] | [[Gateway Endpoint]] |
| ---- | ----- | ----- |
| **What** | Elastic Network Interface with a Private IP | A gateway that is a target for a specific route
| **How** | Uses DNS entries to redirect traffic | Uses prefix lists in the route table to redirect traffic
| **Which services** | [[API Gateway]], [[CloudFormation]], [[CloudWatch]] etc. | Amazon [[S3]], [[DynamoDB]] 
| **Security** | [[Security Group]]s | VPC Endpoint [[Policies]]

## Service provider Model

![[Pasted image 20230205183607.png]]

### What is the difference between gateway and endpoint?

*   An **Endpoint** indicates a specific location for accessing a service using a specific protocol and data format. 
*   A service **Gateway** provides a central access point for managing, monitoring, and securing access to your publicly exposed web services