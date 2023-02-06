Building on the AWS [[managed VPN]] options described previously, you can securely communicate from one site to another using the AWS VPN CloudHub. The AWS VPN CloudHub operates on a simple hub-and-spoke model that you can use with or without a [[VPC]]. Use this approach if you have multiple branch offices and existing internet connections and would like to implement a convenient, potentially low-cost hub-and-spoke model for primary or backup connectivity between these remote offices.

*   A [[VGW]] is deployed on AWS site
*   Network traffic may go between a [[VPC]] and a remote office
*   Network traffic between offices can also be routed over the [[IPSec VPN]]
*   Remote offices connect to the [[VGW]] in a hub-and-spoke model
*   Each office must use a unique [[BGP]] ASN


![[Pasted image 20230205200242.png]]


The following figure shows the AWS VPN CloudHub architecture, with dashed lines indicating network traffic between remote sites being routed over their AWS [[VPN]] connections.

![](https://docs.aws.amazon.com/images/whitepapers/latest/aws-vpc-connectivity-options/images/image12.png)