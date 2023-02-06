## AWS Managed VPN

AWS Managed VPN helps customers to securely connect their on-premises network to AWS, providing a highly available and scalable VPN solution.

*   Virtual private network ([[VPN]]) connection between on- premises sites and AWS
*   Uses the public Internet

### These are the primary [[VPN]] offerings provided by AWS Managed VPN. 

1.  **AWS [[Site-to-Site VPN]]**: A VPN solution that enables secure communication between an on-premises network and an Amazon Virtual Private Cloud (VPC) network over the Internet.
    
2.  **AWS [[Client VPN]]**: A fully managed VPN service that enables secure access to AWS resources and on-premises resources from remote locations.
    
3.  **AWS [[Transit Gateway VPN]]**: A service that enables customers to connect multiple VPCs and on-premises networks to a single AWS Transit Gateway, simplifying network management and reducing the need for complex network topologies.

| | Managed VPN |
| ----- | ---- |
| **What** | AWS Managed [[IPSec VPN]] Connection over your existing Internet
| **When** | Quick and usually simple way to establish a secure tunnelled connection to a [[VPC]]; redundant link for [[Direct Connect]] or other VPC VPN
| **Pros** | Supports static routes or [[BGP]] peering and routing
| **Cons**  | Dependent on your Internet connection
| **How** |  Create a Virtual Private Gateway ([[VGW]]) on AWS, and a Customer Gateway ([[CGW]]) on the on-premises side



![](https://docs.aws.amazon.com/images/whitepapers/latest/aws-vpc-connectivity-options/images/image2.png)

_Figure 1 - AWS Managed VPN_

Consider taking this approach when you want to take advantage of an AWS-managed VPN endpoint that includes automated redundancy and failover built into the AWS side of the VPN connection.

The virtual private gateway ([[VGW]]) also supports and encourages multiple user gateway connections so that you can implement redundancy and failover on your side of the [[VPN]] connection, as shown in the following figure.

![](https://docs.aws.amazon.com/images/whitepapers/latest/aws-vpc-connectivity-options/images/image3.png)

_Figure 2 - Redundant AWS Managed VPN Connections_