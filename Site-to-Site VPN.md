## AWS Site-to-Site VPN

By default, instances that you launch into an Amazon VPC can't communicate with your own (remote) network. You can enable access to your remote network from your VPC by creating an AWS Site-to-Site VPN (Site-to-Site VPN) connection, and configuring routing to pass traffic through the connection.

![[Pasted image 20221118114218.png]]

Although the term _VPN connection_ is a general term, in this documentation, a VPN connection refers to the connection between your [[VPC]] and your own on-premises network. Site-to-Site VPN supports Internet Protocol security [[IPsec VPN]] connections.

Your Site-to-Site VPN connection is either an AWS Classic VPN or an AWS VPN. For more information, see [Site-to-Site VPN categories](https://docs.aws.amazon.com/vpn/latest/s2svpn/vpn-categories.html).

Your Site-to-Site VPN connection is either an AWS Classic VPN connection or an AWS VPN connection. Any new Site-to-Site VPN connection that you create is an AWS VPN connection. The following features are supported on AWS VPN connections only:

-   Internet Key Exchange version 2 (IKEv2)
-   NAT traversal
-   4-byte ASN in the range of 1 – 2147483647 for Virtual Private Gateway ([[VGW]]) configuration. 
-   2-byte ASN for Customer Gateway ([[CGW]]) in the range of 1 – 65535. 
-   [[CloudWatch]] metrics
-   Reusable [[IP address]]es for your [[CGW]]s
-   Additional [[encryption]] options; including AES 256-bit encryption, SHA-2 hashing, and additional Diffie-Hellman groups
-   Configurable tunnel options
-   Custom private [[ASN]] for the Amazon side of a [[BGP]] session
-   Private Certificate from a subordinate CA from AWS Private Certificate Authority
-   Support for IPv6 traffic for [[VPN]] connections on a [[transit gateway]]
- 
### The key concepts for Site-to-Site VPN:

- ##### VPN connection:
A secure connection between your on-premises equipment and your VPCs.
    
- ##### VPN tunnel:
An encrypted link where data can pass from the customer network to or from AWS.
Each VPN connection includes two VPN tunnels which you can simultaneously use for high availability.
    
- ##### Customer gateway ():
An AWS resource which provides information to AWS about your customer gateway device.
    
- ##### Customer gateway device: 
A physical device or software application on your side of the Site-to-Site VPN connection.
    
- ##### Target gateway:
A generic term for the VPN endpoint on the Amazon side of the Site-to-Site VPN connection.
    
- ##### Virtual private gateway ([[VGW]]): 
A virtual private gateway is the VPN endpoint on the Amazon side of your Site-to-Site VPN connection that can be attached to a single VPC.
    
- ##### [[Transit gateway]]: 
A transit hub that can be used to interconnect multiple [[VPC]]s and on-premises networks, and as a [[VPN]] endpoint for the Amazon side of the Site-to-Site VPN connection.