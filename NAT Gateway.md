A NAT gateway is **a Network Address Translation ([[NAT]]) service**. You can use a NAT gateway so that EC2 instances in a private subnet can connect to services outside your [[VPC]] but external services cannot initiate a connection with those instances.

![[Pasted image 20221117180117.png]]

*   The NAT gateway is created in the public subnet
*   The NAT gateway ID must be specified in the private subnet route rable

## [[NAT Instance]]s and NAT Gateways  

*   Used for accessing the internet from private subnets 
*   Deployed in [[public subnet]]s  
*   Must update the [[route table]] in private subnets  
*   [[NAT instance]]s are managed by you  
*   NAT gateways are managed by AWS