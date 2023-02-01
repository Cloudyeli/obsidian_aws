## Application Load Balancer (ALB)

Elastic Load Balancing ([[ELB]]) with the Application Load Balancer (ALB) is best suited for load balancing of HTTP and HTTPS traffic and provides advanced request routing targeted at the delivery of modern application architectures, including microservices and containers.

*   With ALB, it is a requirement that you enable at least two or more [[AZ]]s.
*   This is a [[TCP]] Load Balancer only that does some NAT magic at the VPC level. It uses [[EIP]]s, so it has a static endpoint unlike ALB and [[CLB]]s (by default). Each Target can be on different ports.

Operating at the individual request level (Layer 7), Application Load Balancer routes traffic to targets within Amazon Virtual Private Cloud ([[VPC]]) based on the content of the request.

*   Used for web applications.
*    Operates at the request level ([[HTTP]]/[[HTTPS]]) of the ([[OSI]]) model and routes based on the content of the request (layer 7) 
*    Supports advanced routing

## Elastically Scale the Application

*   A Launch Template specifies the EC2 instance configuration
* . The Application Load Balancer distributes connections between targets ([[EC2]] instances)
*   [[CloudWatch]] receives metrics from ALB and notifies [[Auto Scaling]] if thresholds are breached

![[Pasted image 20221117093518.png]]
