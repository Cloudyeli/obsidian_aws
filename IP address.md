## public IP:

*   Public IP is dynamic and lost when instance is stopped
*   Public IPs cannot be moved between [[EC2]] instances

## private IP:

*   Private IPs are attached to all [[EC2]] instances  
*   Private IPs are retained when the instance is stopped
*   [[RFC 1918]]


## Elastic IP ([[EIP]]):

*   Elastic IPs are static public addresses  
*   Elastic IPs are retained when the instance is stopped  
*   Elastic IPs can be moved between instances  
*   Elastic IPs are chargeable if not used

![[Pasted image 20221117173119.png]]



![[Pasted image 20230201180822.png]]

![[Pasted image 20230201180912.png]]

if CIDR block 10.100.100.0/24, then reserved IP addresses are: • 10.100.100.0 – Network Address • 10.100.100.1 – reserved by AWS for the VPC router • 10.100.100.2 – reserved by AWS for mapping to Amazon-provided DNS • 10.100.100.3 – reserved by AWS for future use • 10.100.100.255 – Network Broadcast Address. AWS does not support broadcast in a VPC,