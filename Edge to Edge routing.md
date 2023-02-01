Like most IT terms, there is no formal definition. It means whatever the vendor wants it to mean.

But edge-to-edge routing in a cloud provider context means essentially using a "virtual cloud"** as a transit between another cloud and some other network (_i.e._, routing from one edge of the cloud to another).

For example, you have a corporate network connected to one Amazon VPC (A). That VPC is also connected to another VPC (B). Routing from your corporate network through VPC A to reach VPC B is an example of edge to edge routing (and it's not allowed).

[[VPC Peering]] [Basics](https://docs.aws.amazon.com/vpc/latest/peering/invalid-peering-configurations.html#edge-to-edge-vgw) 

** Cloud providers have different product names for this: Virtual Private Cloud or Virtual Network.

