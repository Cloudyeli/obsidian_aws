## Network Load Balancer (NLB)

Elastic Load Balancing ([[ELB]]) with the Network Load Balancer (NLB) is best suited for load balancing of [[SSL]]/[[TLS]], [[TCP]], [[UDP]]  traffic where extreme performance is required.

Operating at the connection level (Layer 4), Network Load Balancer routes traffic to targets within Amazon Virtual Private Cloud ([[VPC]]) and is capable of handling millions of requests per second while maintaining ultra-low latencies.

*   With NLB, Elastic Load Balancing ([[ELB]]) creates a network interface for each [[AZ]] that you enable.
*   Network Load Balancer is also optimized to handle sudden and volatile traffic patterns.

Layer 4 load balancer that routes connections based on IP protocol data.

*   Operates at the connection/transport level ([[TCP]]/[[UDP]]) of the ([[OSI]]) model and routes connections based on IP protocol data (layer 4) 
*   Offers ultra high performance, low latency and TLS offloading at scale