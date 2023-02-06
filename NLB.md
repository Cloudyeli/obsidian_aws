## Network Load Balancer (NLB)

Elastic Load Balancing ([[ELB]]) with the Network Load Balancer (NLB) is best suited for load balancing of [[SSL]]/[[TLS]], [[TCP]], [[UDP]]  traffic where extreme performance is required.

-   Operates at the connection level
-   Routes connections based on IP protocol data (layer 4 [[OSI]] model)
-   Offers **ultra high performance**, **low latency** and **[[TLS offloading]] at scale**
-   Can have a static IP ([[EIP]])
-   Supports [[TCP]]/[[UDP]] and static IP ([[EPI]]) addresses as targets
-   Ultra-low latency  
-   [[VPC endpoint]] services
-   Creates a network interface for each [[AZ]] that you enable.
-   Is also optimised to handle sudden and volatile traffic patterns.
-   Supports [[PrivateLink]]
-   Source IP preservation: Native
-   SSL termination: [[ELB]] or target

![[Pasted image 20230204121546.png]]
![[Pasted image 20230204124008.png]]
## [[SSL]]/[[TLS]] Termination

![[Pasted image 20230204134311.png]]



* This is a [[TCP]] Load Balancer only that does some NAT magic at the VPC level. It uses [[EIP]]s, so it has a static endpoint unlike ALB and [[CLB]]s (by default). Each Target can be on different ports.

