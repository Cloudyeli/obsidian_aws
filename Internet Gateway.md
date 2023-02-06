An internet gateway is a horizontally scaled, redundant, and highly available [[VPC]] component that allows communication between your VPC and the internet.

*   It supports IPv4 and IPv6 traffic. 
*   It does not cause availability risks or bandwidth constraints on your network traffic.
*   An internet gateway enables resources in your public [[subnet]]s (such as [[EC2]] instances) to connect to the internet if the resource has a public IPv4 address or an IPv6 address.
*   An internet gateway provides a target in your VPC [[route table]]s for internet-routable traffic. 
*   For communication using IPv4, the internet gateway also performs network address translation ([[NAT]]).