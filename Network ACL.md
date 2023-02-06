A _network access control list (ACL)_ allows or denies specific inbound or outbound traffic at the subnet level. You can use the default network ACL for your VPC, or you can create a custom network ACL for your VPC with rules that are similar to the rules for your security groups in order to add an additional layer of security to your VPC.

*   Network ACLs apply at the [[subnet]] level
*   Network ACL apply only to traffic entering / existing the [[subnet]]
*   Rules are processed in order
*   Network ACL have an explicit deny

| [[Security Group]] | Network ACL |
| ---- | -------- |
| Operates at the instance level | Operates at the [[subnet]] level
| Supports allow rules only | Supports allow and deny rules
| Stateful | Stateless
| Evaluates all rules | Processes rules in order
| Applies to an instance only if associated with a group | Automatically applies to all instances in the subnets its associated with

![[Pasted image 20230205175448.png]]

The following diagram shows a VPC with two subnets. Each subnet has a network ACL. When traffic enters the VPC (for example, from a peered VPCs, VPN connection, or the internet), the router sends the traffic to its destination. Network ACL A determines which traffic destined for subnet 1 is allowed to enter subnet 1, and which traffic destined for a location outside subnet 1 is allowed to leave subnet 1. Similarly, network ACL B determines which traffic is allowed to enter and leave subnet 2.
![[Pasted image 20221114190848.png]]

![[Pasted image 20230205175431.png]]
![[Pasted image 20221117172143.png]]
