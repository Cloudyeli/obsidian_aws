A Security group is a instance-level firewall.

*   Firewall for EC2 instances  
*   Operate at the instance level
*   Support allow rules only
*   [[stateful]] [[firewall]]
*   Separate rules for inbound and outbound traffic
*   A source can be an IP address or security group ID
*   Security Groups can be applied to instances in **any** [[subnet]]

| Security Group | [[Network ACL]] |
| ---- | -------- |
| Operates at the instance level | Operates at the [[subnet]] level
| Supports allow rules only | Supports allow and deny rules
| Stateful | Stateless
| Evaluates all rules | Processes rules in order
| Applies to an instance only if associated with a group | Automatically applies to all instances in the subnets its associated with

![[Pasted image 20221117172143.png]]

## Security Groups Best Practice

![[Pasted image 20230205175339.png]]