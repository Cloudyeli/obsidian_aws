## Cross-Zone Load Balancing ([[ELB]])

##### - When cross-zone load balancing is enabled:
*   Each load balancer node distributes traffic across the registered targets in all enabled [[AZ]]s
*   With Application Load Balancers ([[ALB]]), cross-zone load balancing is **always enabled**

![[Pasted image 20230204132724.png]]

##### - When cross-zone load balancing is disabled:
-   Each load balancer node distributes traffic only across the registered targets in its AZ
-   With Network Load Balancers ([[NLB]]) and Gateway Load Balancers ([[GLB]]), cross- zone load balancing is **disabled by default**

![[Pasted image 20230204132706.png]]