AWS Transit Gateway is an AWS managed high availability and scalability regional network transit hub used to interconnect [[VPC]]s and customer networks. 

*   Transit Gateway is a network transit hub that interconnects [[VPC]]s and on-premises networks
*   Transit Gateways can be attached to [[VPN]]s, [[Direct Connect]] Gateways, 3rd party appliances and Transit Gateways in other [[Region]]s/accounts
*   Connects [[VPC]]s and on-premises networks through a central hub
*   Simplifies network configuration

![[Pasted image 20221118114711.png]]

### AWS Transit Gateway + VPN

AWS Transit Gateway + [[VPN]], using the [[Transit Gateway VPN attachment]], provides the option of creating an [[IPsec VPN]] connection between your remote network and the Transit Gateway over the internet, as shown in the following figure.

*   Connects VPCs and on-premises networks through a central hub
*   Simplifies network configuration

![](https://docs.aws.amazon.com/images/whitepapers/latest/aws-vpc-connectivity-options/images/image4.png)

_Figure 3 - AWS Transit Gateway and VPN_

Consider using this approach when you want to take advantage of an AWS [[managed VPN]] endpoint for connecting to multiple VPCs in the same region without the additional cost and management of multiple IPSec VPN connections to multiple Amazon VPCs.

AWS Transit Gateway also supports and encourages multiple user gateway connections so that you can implement redundancy and failover on your side of the VPN connection as shown in the following figure.

![](https://docs.aws.amazon.com/images/whitepapers/latest/aws-vpc-connectivity-options/images/image5.png)