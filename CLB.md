Classic Load Balancer provides basic load balancing ([[ELB]]) across multiple Amazon [[EC2]] instances and operates at both the request level and connection/transport level of the ([[OSI]]) model. Classic Load Balancer is intended for applications that are built within the EC2-Classic network. We recommend Application Load Balancer ([[ALB]]) for Layer 7 traffic and Network Load Balancer ([[NLB]]) for Layer 4 traffic when using Virtual Private Cloud ([[VPC]]).

*   Old generation; not recommended for new applications
*   Performs routing at Layer 4 and Layer 7  
*   Use for existing applications running in EC2-Classic
*   TCP, SSL, HTTP, HTTPS

![[Pasted image 20230204121749.png]]