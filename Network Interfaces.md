An _elastic network interface_ is a logical networking component in a [[VPC]] that represents a virtual network card. 

*  You can create and configure network interfaces and attach them to instances in the same Availability Zone ([[AZ]]). (`eth0`)
*   Additional [[ENI]]s can be attached from subnets within the same [[AZ]]. (`eth1`)
*   You cannot attach ENIs from subnets in different [[AZ]]s.
*   The primary network interface (`eth0`) has a private IP and optionally a public IP.
*   Your account might also have _requester-managed_ network interfaces, which are created and managed by AWS services to enable you to use other resources and services. 
*   You cannot manage these network interfaces yourself. For more information, see [Requester-managed network interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/requester-managed-eni.html).

## The different Network Interfaces

##### - Elastic Network Interface ([[ENI]])
##### - Elastic Network Adapter ([[ENA]])
##### - Elastic Fabric Adapter ([[EFA]])

![[Pasted image 20230201124222.png]]

## It can include the following attributes:

-   A primary private IPv4 address from the IPv4 address range of your [[VPC]]
-   One or more secondary private IPv4 addresses from the IPv4 address range of your [[VPC]]
-   One Elastic IP ([[EIP]]) address (IPv4) per private IPv4 address
-   One public IPv4 address
-   One or more IPv6 addresses
-   One or more security groups
-   A MAC address
-   A source/destination check flag
-   A description

![[Pasted image 20230201124200.png]]

## Network Interfaces and [[NAT for public IP adresses]]