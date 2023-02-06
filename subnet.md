A subnet, or subnetwork, is a range of IP addresses in your [[VPC]], like a network inside a network. 
Subnets make networks more efficient. Through subnetting, network traffic can travel a shorter distance without passing through unnecessary routers to reach its destination.
The only difference between private and public subnet is, that a public subnet has just a privat IP adress assigned, while a public subnet also has a public IP Adress assigned.


## public subnet

Public subnets are subnets that have:  
*   `Auto-assign public IPv4 address` set to `Yes` 
*   The subnet route table has an attached [[Internet Gateway]]

## private subnet

*   A private subnet is a subnet that is associated with a [[route table]] that **doesn’t** have a route to an [[internet gateway]]. 
*   [[EC2]] Instances in the private subnet are backend servers they don’t accept the traffic from the internet.
*   To access the internet from a private subnet, use a [[NAT Gateway]]

![[Pasted image 20230201183327.png]]

## [[SSH]] into [[EC2]] in Private Subnet

https://digitalcloud.training/ssh-into-ec2-in-private-subnet/

### Why Private Subnet

Resources like databases may require connection to internet for updates/patches but should not be accepting request from the internet. In such cases a private subnet is to be used.

It's not possible to use the private IP addresses assigned to instances in a private VPC subnet over the internet. Instead, you must use NAT to map the private IP addresses to a public address for requests. Then, you must map the public IP address back to the private IP addresses for responses.
A [[NAT gateway]] allows EC2 instances to establish outbound connections to resources on internet without allowing inbound connections to the EC2 instance.