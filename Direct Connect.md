## AWS Direct Connect (DX)

AWS Direct Connect (DX) is **a network service that provides an alternative to using the Internet to utilize AWS cloud services**. AWS Direct Connect enables customers to have low latency, secure and private connections to AWS for workloads which require higher speed or lower latency than the internet.

*   DX is a physical fibre connection to AWS running at 1 Gbps or 10 Gbps
*   A DX port (1000-Base-LX or 10GBASE-LR) must be allocated in a DX location
*   A cross-connect between the AWS DX [[router]] and the customer/partner DX [[router]]
*   The customer [[router]] is connected to the DX router in the DX location
*   **Avoids the public Internet**
*   Private connectivity between AWS and your datacenter / office (**Private connection from on-premises to AWS**)
*   Consistent network experience – **increased speed/latency & bandwidth/throughput**  
*   Lower costs for organisations that transfer **large volumes of data**

| | Direct Connect (DX) | Direct Connect (DX) + [[VPN]] |
| --- | --- | --- | 
| **What** | Dedicated network connection over private lines straight into the AWS backbone | IPSec VPN connection over private lines (Direct Connect)
| **When** | Requires a large network link into AWS; lots of resources and services being provided on AWS to your corporate users | Need the added security of encrypted tunnels over Direct Connect
| **Pros** | Predictable network performance; potential bandwidth cost reduction; up to 10/100 Gbps provisioned connections; supports BGP peering and routing | More secure (in theory) than Direct Connect alone
| **Cons** | May require additional telecom and hosting provider relationships and/or network circuits; costly; takes time to provision | More complexity introduced by VPN layer
| **How** | Work with your existing data networking provider; create Virtual Interfaces (VIFs) to connect to VPCs (private VIFs) or other AWS services like S3 or Glacier (public VIFs) | Work with your existing data networking provider

![[Pasted image 20230205200633.png]]

![[Pasted image 20221118083525.png]]


### AWS [[Direct Connect Gateway]]

A Direct Connect gateway is a globally available resource to enable connections to multiple Amazon [[VPC]]s across different [[region]]s or AWS accounts. This feature also allows you to connect to any participating VPCs from one private [[VIF]], reducing AWS [[Direct Connect (DX)]] management, as shown in the following figure.

![[Pasted image 20221118092737.png]]