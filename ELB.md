## Amazon Elastic Load Balancing (ELB)

Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets, such as Amazon **[[EC2]] instances**, **containers**, and **IP addresses**.

*   ELB can handle the varying load of your application traffic in a single [[AZ]] or across multiple Availability Zones.
*   ELB features **high availability**, **[[auto scaling]]**, and **robust security** necessary to make your applications fault tolerant.

You configure your load balancer to accept incoming traffic by specifying one or more _[[listener]]s_. A listener is a process that checks for connection requests. It is configured with a protocol and port number for connections from clients to the load balancer. Likewise, it is configured with a protocol and port number for connections from the load balancer to the targets.

There are four types of Elastic Load Balancer (ELB) on AWS (Just [[ALB]] & [[NLB]] important):

![[Pasted image 20221116171632.png]]

- ##### Application Load Balancer ([[ALB]])
Layer 7 load balancer that routes connections based on the content of the request ([[HTTP]]/[[HTTPS]]).

- ##### Network Load Balancer ([[NLB]])
Layer 4 load balancer that routes connections based on IP protocol data ([[TLS]]/[[TCP]]/UDP).

- ##### (OLD) Classic Load Balancer ([[CLB]])
This is the oldest of the three and provides basic load balancing at both layer 4 and layer 7 (not on the exam anymore).

- ##### Gateway Load Balancer ([[GLB]])
Layer 3 load balancer that routes connections by deciding the physical path on the network level of the  ([[OSI]]) model.
Used in front of virtual appliances such as [[firewall]]s, [[IDS]]/[[IPS]], and [[DPI]] and scales them up or down.

![[Pasted image 20221117081403.png]]
![[Pasted image 20221117062740.png]]

There is a key difference in how the load balancer types are configured. With Application Load Balancers, Network Load Balancers, and Gateway Load Balancers, you register targets in [[target group]]s, and route traffic to the target groups. With Classic Load Balancers, you register instances with the load balancer.

![[Pasted image 20221116171413.png]]


![elastic-load-balancing-ec2-auto-scaling](https://digitalcloud.training/wp-content/uploads/2022/02/elastic-load-balancing-ec2-auto-scaling.png)