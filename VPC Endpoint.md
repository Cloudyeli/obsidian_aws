A VPC endpint is your private [[VPC]] connection to public AWS services.
You can create an interface VPC endpoint to connect to services powered by AWS [[PrivateLink]], including many AWS services.

For each [[subnet]] that you specify from your VPC, we create an endpoint network interface in the subnet and assign it a private [[IP address]] from the subnet address range. An endpoint network interface is a requester-managed network interface; you can view it in your AWS account, but you can't manage it yourself.

### What is the [[difference between gateway and endpoint]]?

An endpoint indicates a specific location for accessing a service using a specific protocol and data format. GateWay: **An service Gateway provides a central access point for managing, monitoring, and securing access to your publicly exposed web services**.