A private subnet is a subnet that is associated with a [[route table]] that **doesn’t** have a route to an [[internet gateway]]. [[EC2]] Instances in the private subnet are backend servers they don’t accept the traffic from the internet.

### Why Private Subnet

Resources like databases may require connection to internet for updates/patches but should not be accepting request from the internet. In such cases a private subnet is to be used.

It's not possible to use the private IP addresses assigned to instances in a private VPC subnet over the internet. Instead, you must use NAT to map the private IP addresses to a public address for requests. Then, you must map the public IP address back to the private IP addresses for responses.
A [[NAT gateway]] allows EC2 instances to establish outbound connections to resources on internet without allowing inbound connections to the EC2 instance.
