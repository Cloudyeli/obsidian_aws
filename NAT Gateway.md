A NAT gateway is **a Network Address Translation ([[NAT]]) service**. You can use a NAT gateway so that EC2 instances in a private subnet can connect to services outside your [[VPC]] but external services cannot initiate a connection with those instances.

![[Pasted image 20221117180117.png]]

*   The NAT gateway is created in the public subnet
*   The NAT gateway ID must be specified in the private subnet route rable

## [[NAT Instance]]s and NAT Gateways  

Used both for accessing the internet from private subnets 

| NAT Instance | NAT Gateway |
|---------------- | ------------------ |
| Managed by you (e.g. software updates) | Managed by AWS 
| Scale up (instance type) manually and use enhanced networking | Elastic scalability up to 45 Gbps 
| No high availability – scripted/auto-scaled HA possible using multiple NATs in multiple subnets | Provides automatic high availability within an AZ  and can be placed in multiple AZs  
| Need to assign Security | Group No Security Groups
| Can use as a bastion host | Cannot access through SSH
| Use an Elastic IP address or a public IP address with a NAT instance |Choose the Elastic IP address to associate with a  NAT gateway at creation
| Can implement port forwarding through manual customisation | Does not support port forwarding  
| Managed by you | Managed by AWS
| Must disable source/destination checks | Deployed in public [[subnet]]s  
| Uses a special [[AMI]] with the string “**amzn-ami- vpc-nat**” in the name |   |
| The NAT instance ID must be specified in the private subnet [[route table]] | |


![[Pasted image 20230201185407.png]]

## [[NAT for public IP adresses]]

