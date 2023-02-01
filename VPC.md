## Virtual Private Cloud (VPC)

A Amazon Virtual Private Cloud (VPC) is a logically isolated portion of the AWS cloud within a [[region]].

![[Pasted image 20221117160724.png]]

-   A VPC is a virtual network dedicated to your AWS account.
-   Analogous to having your own datacenter inside AWS.
-   It is logically isolated from other virtual networks in the AWS Cloud.
-   Provides complete control over the virtual networking environment.
-   You can launch your AWS resources, such as Amazon [[EC2]] instances, into your VPC.
-   An [[Internet Gateway]] is used to connect to the Internet.
-   The route table is used to configure the VPC router.

![[Pasted image 20221117162029.png]]

*   When you create a VPC, you must specify a range of IPv4 addresses for the VPC in the form of a Classless Inter-Domain Routing (CIDR) block; for example, 10.0.0.0/16 (CIDR block range from /16 till /28)
-   A VPC spans all the Availability Zones ([[AZ]]s) in the [[region]].
-   You have full control over who has access to the AWS
    resources inside your VPC.
-   By default you can create up to 5 VPCs per region.
-   A default VPC is created in each region with a [[subnet]] in each AZ

## VPC Components

* ##### Virtual Private Cloud (VPC)
A logically isolated virtual network in the AWS cloud

* ##### [[Subnet]]
A segment of a VPC’s IP address range where you can place groups of isolated resources

* ##### [[Internet Gateway]]/Egress-only Internet Gateway
The Amazon VPC side of a connection to the public Internet for IPv4/IPv6

* ##### [[Router]]
Routers interconnect subnets and direct traffic between [[Internet gateway]]s, virtual private gateways ([[VGW]]), [[NAT gateway]]s, and [[subnet]]s

* ##### Peering Connection ([[VPC Peering]])
Direct connection between two VPCs

* ##### [[VPC Endpoint]]s
Private connection to public AWS services

* ##### (OLD) [[NAT Instance]]
Enables Internet access for EC2 instances in private subnets managed by you

* ##### [[NAT Gateway]] 
Enables Internet access for [[EC2]] instances in [[private subnet]]s (managed by AWS)

* ##### Virtual Private Gateway ([[VGW]])
The Amazon VPC side of a Virtual Private Network ([[VPN]]) connection

* ##### Customer Gateway ([[CGW]]) 
Customer side of a [[VPN]] connection

* ##### AWS [[Direct Connect]] 
High speed, high bandwidth, private network connection from customer to aws

* ##### [[Security Group]] 
Instance-level [[firewall]]

* ##### Network Access Control List ([[NACL]]) 
Subnet-level [[firewall]]


## VPC Connections

* ###  AWS [[VPC Peering]]
Used to route between VPCs using private IP addresses

* ### AWS [[Managed VPN]]
Virtual private network (VPN) connection between on- premises sites and AWS

• Uses the public Internet  
AWS Direct Connect  
• Private connection from on-premises to AWS • Avoids the public Internet


