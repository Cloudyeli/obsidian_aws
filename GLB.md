## Gateway Load Balancer (GLB)

Elastic Load Balancing ([[ELB]]) with the Gateway Load Balancer (GLB) helps you easily deploy, scale, and manage your third-party virtual appliances. It gives you one gateway for distributing traffic across multiple virtual appliances while scaling them up or down, based on demand. This decreases potential points of failure in your network and increases availability.  

*   Operates at Layer 3 – listens for all packets on all ports
*   Forwards traffic to the [[target group]] specified in the [[listener]] rules
*   Gateway Load Balancers enable you to deploy, scale, and manage virtual appliances, such as **[[firewall]]s**, **intrusion detection system ([[IDS]])**  **intrusion prevention systems ([[IPS]])**, and **deep packet inspection systems ([[DPI]])**. 
*   It combines a transparent network gateway (that is, a single entry and exit point for all traffic) and distributes traffic while scaling your virtual appliances with the demand.
*   It listens for all IP packets across all ports and forwards traffic to the [[target group]] that's specified in the [[listener]] rule. 
*   It maintains [[stickiness]] of flows to a specific target appliance using 5-tuple (for [[TCP]]/[[UDP]] flows) or 3-tuple (for non-TCP/UDP flows). 
*   GLB and virtual appliances exchange application traffic using the [[GENEVE]] protocol on port 6081
*   Integrate with Auto Scaling groups ([[ASG]]) for elasticity  
*   Apply network [[monitoring]] and logging for analytics

### Use with virtual appliances such as:

*   Firewalls
*   Intrusion detection systems ([[IDS]])  
*   Intrusion prevention systems ([[IPS]])  
*   Deep packet inspection systems ([[DPI]])
*   Next generation firewalls ([[NGFW]])
*   Web application firewalls ([[WAF]])
*   Distributed denial of service protection systems ([[DDoS]])

![[Pasted image 20230204123139.png]]