## Virtual Private Cloud (VPC)

A Amazon Virtual Private Cloud (VPC) is a logically isolated portion of the AWS cloud within a [[region]].

*   Analogous to having your own DC inside AWS
-   Provides complete control over the virtual networking environment
-  It is logically isolated from other virtual networks in the AWS Cloud.
-   A VPC is logically isolated from other VPCs on AWS
-   VPCs are region wide
-   Provides complete control over the virtual networking environment including selection of I**P ranges**, **creation of [[subnet]]s**, and **configuration of [[route table]]s** and **gateways**
-   You can launch your AWS resources, such as Amazon [[EC2]] instances, into your VPC
- -   A VPC spans all the Availability Zones ([[AZ]]s) in the [[region]].
-   You have full control over who has access to the AWS resources inside your VPC.
-   A default VPC is created in each region with a [[subnet]] in each [[AZ]]
-   By default, you can create up to 5 VPCs per region
-   [[AZ]]s names are mapped to different zones for different users – use AZ ID to identify physical zones
-   The VPC [[router]] takes care of routing within the VPC and outside of the VPC
-   The [[route table]] is used to configure the VPC router.
-   An [[Internet Gateway]] is attached to a VPC and used to connect to the Internet

![[Pasted image 20230205165121.png]]

### Rules and Guidelines (IP [[CIDR]])

-   [[CIDR]] block size can be between /16 and /28
-   The [[CIDR]] block must not overlap with any existing [[CIDR]] block that's associated with the VPC
-   You cannot increase or decrease the size of an existing [[CIDR]] block
-   The first four and last IP address are not available for use
-   AWS recommend you use [[CIDR]] blocks from the [[RFC 1918]] ranges

### Additional Considerations

*   Ensure you have enough networks and hosts
*   Bigger [[CIDR]] blocks are typically better (more flexibility)
*   Smaller [[subnet]]s are OK for most use cases
*   Consider deploying application tiers per [[subnet]]
*   Split your [[HA]] resources across subnets in different [[AZ]]s
*   [[VPC Peering]] requires non-overlapping [[CIDR]] blocks
*   This is across all VPCs in all [[Regions]] / accounts you want to connect  
*   **==Avoid overlapping [[CIDR]] blocks as much as possible!==**

![[Pasted image 20221117162029.png]]

## VPC Components

##### - [[Subnet]]
*   A segment of a VPC’s IP address range where you can place groups of isolated resources (maps to a single [[AZ]])

##### - [[Internet Gateway]]
*   The Amazon VPC side of a connection to the public Internet for IPv4/IPv6

##### - [[Egress-only Internet Gateway]]
A stateful gateway to provide egress only access for IPv6 traffic from the VPC to the Internet

##### - [[NAT Gateway]]
*   A highly available, managed Network Address Translation ([[NAT]]) service for your resources in a private subnet to access the Internet

* ##### (OLD) [[NAT Instance]]
Enables Internet access for EC2 instances in private subnets managed by you

##### - [[Router]]
*   Routers interconnect [[subnet]]s and direct traffic between [[Internet gateway]]s, virtual private gateways ([[VGW]]), [[NAT gateway]]s, and [[subnet]]s
    
##### - Peering Connection
*  A peering connection enables you to route traffic via private IP addresses between two peered VPCs ([[VPC Peering]], [[Transit Gateway]])
    
##### - [[VPC Endpoint]]s
Enables private connectivity to services hosted in AWS  {[[Interface Endpoint]], [[Gateway Endpoint]])

##### - Hardware [[VPN]] Connection
*   A hardware-based [[VPN]] connection between your Amazon VPC and your datacenter, home network, or co-location facility

##### - Virtual Private Gateway ([[VGW]])
*   The Amazon VPC side of a Virtual Private Network ([[VPN]]) connection

##### - Customer Gateway ([[CGW]]) 
*   Customer side of a [[VPN]] connection

##### - AWS [[Direct Connect]] 
*   High speed, high bandwidth, private network connection from customer to AWS

##### - [[Security Group]]s
*   Instance-level [[firewall]]

##### - [[Network ACL]]
*  Subnet-level [[firewall]]

## VPC Connections

* ###  AWS [[VPC Peering]]
Used to route between VPCs using private IP addresses

* ### AWS [[Managed VPN]]
Virtual private network (VPN) connection between on- premises sites and AWS
