## AWS Managed VPN

Amazon VPC provides the option of creating an [[IPsec VPN]] connection between your remote networks and Amazon [[VPC]] over the internet, as shown in the following figure.

*   Virtual private network ([[VPN]]) connection between on- premises sites and AWS
*   Uses the public Internet

![](https://docs.aws.amazon.com/images/whitepapers/latest/aws-vpc-connectivity-options/images/image2.png)

_Figure 1 - AWS Managed VPN_

Consider taking this approach when you want to take advantage of an AWS-managed VPN endpoint that includes automated redundancy and failover built into the AWS side of the VPN connection.

The virtual private gateway ([[VGW]]) also supports and encourages multiple user gateway connections so that you can implement redundancy and failover on your side of the [[VPN]] connection, as shown in the following figure.

![](https://docs.aws.amazon.com/images/whitepapers/latest/aws-vpc-connectivity-options/images/image3.png)

_Figure 2 - Redundant AWS Managed VPN Connections_