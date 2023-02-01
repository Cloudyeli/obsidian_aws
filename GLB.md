Elastic Load Balancing ([[ELB]]) with the Gateway Load Balancer (GLB) helps you easily deploy, scale, and manage your third-party virtual appliances. It gives you one gateway for distributing traffic across multiple virtual appliances while scaling them up or down, based on demand. This decreases potential points of failure in your network and increases availability.  
  
*   You can find, test, and buy virtual appliances from third-party vendors directly in AWS Marketplace.
*   Gateway Load Balancers enable you to deploy, scale, and manage virtual appliances, such as **[[firewall]]s**, **intrusion detection system ([[IDS]])**  **intrusion prevention systems ([[IPS]])**, and **deep packet inspection systems ([[DPI]])**. 
*   It combines a transparent network gateway (that is, a single entry and exit point for all traffic) and distributes traffic while scaling your virtual appliances with the demand.

A Gateway Load Balancer operates at thethe network layer of the  ([[OSI]]) model (3 layer). 

*   It listens for all IP packets across all ports and forwards traffic to the [[target group]] that's specified in the [[listener]] rule. 
*   It maintains [[stickiness]] of flows to a specific target appliance using 5-tuple (for [[TCP]]/UDP flows) or 3-tuple (for non-TCP/UDP flows). 
*   The Gateway Load Balancer and its registered virtual appliance instances exchange application traffic using the [GENEVE](https://datatracker.ietf.org/doc/html/rfc8926) protocol on port 6081.