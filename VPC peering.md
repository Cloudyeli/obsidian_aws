A VPC peering connection is a networking connection between two [[VPC]]s that enables you to route traffic between them using private IPv4 addresses or IPv6 addresses. Instances in either VPC can communicate with each other as if they are within the same network.

*   Used to route between VPCs using private [[IP address]]es
*   You can create a VPC peering connection between your own VPCs, or with a VPC in another AWS account.
*   The VPCs can be in different [[Region]]s (also known as an inter-Region VPC peering connection).

![[Pasted image 20221117181016.png]]

![[Pasted image 20230205180058.png]]

When you establish peering relationships between VPCs across different AWS Regions, resources in the VPCs (for example, [[EC2]] instances and [[Lambda]] functions) in different AWS Regions can communicate with each other using private [[IP address]]es, without using a gateway, [[VPN]] connection, or network appliance.

*   The traffic remains in the private IP space. 
*   All inter-Region traffic is encrypted with no single point of failure, or bandwidth bottleneck. 
* Traffic always stays on the global AWS backbone, and never traverses the public internet, which reduces threats, such as common exploits, and [[DDoS]] attacks. 
*   Inter-Region VPC peering provides a simple and cost-effective way to share resources between regions or replicate data for geographic redundancy.

A VPC peering connection helps you to facilitate the transfer of data. For example, if you have more than one AWS account, you can peer the VPCs across those accounts to create a file sharing network. You can also use a VPC peering connection to allow other VPCs to access resources you have in one of your VPCs.

## VPC Peering [Basics](https://docs.aws.amazon.com/vpc/latest/peering/invalid-peering-configurations.html#edge-to-edge-vgw) 

