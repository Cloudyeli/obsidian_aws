## Wavelength Zones

* AWS Wavelength enables developers to build applications that deliver single-digit millisecond latencies to mobile devices and end-users.
* AWS developers can deploy their applications to Wavelength Zones, AWS infrastructure deployments that embed AWS compute and storage services within the telecommunications providers’ datacenters at the edge of the 5G networks, and seamlessly access the breadth of AWS services in the region.
* AWS Wavelength brings AWS services to the edge of the 5G network, minimizing the latency to connect to an application from a mobile device.

Use cases:

-   Single-digit ms latency to **mobile devices/users**
-   Live video, [[ML]], [[AR]]/[[VR]]

![[Pasted image 20230205154338.png]]
_----

AWS Wavelength_ allows developers to build applications that deliver ultra-low latencies to mobile devices and end users. Wavelength deploys standard AWS compute and storage services to the edge of telecommunication carriers' 5G networks. Developers can extend a Amazon Virtual Private Cloud to one or more Wavelength Zones, and then use AWS resources like Amazon EC2 instances to run applications that require ultra-low latency and a connection to AWS services in the Region.

A Wavelength Zone is an isolated zone in the carrier location where the Wavelength infrastructure is deployed. Wavelength Zones are tied to a Region. A Wavelength Zone is a logical extension of a Region, and is managed by the control plane in the Region.

A Wavelength Zone is represented by a Region code followed by an identifier that indicates the Wavelength Zone, for example, `us-east-1-wl1-bos-wlz-1`.

To use a Wavelength Zone, you must opt-in to the zone. Once you have opted in, you must create a Amazon VPC and subnet in the Wavelength Zone. Then you will be ready to launch your Amazon EC2 instances in them to use for your Amazon ECS clusters and tasks. For more information, see [Get started with AWS Wavelength](https://docs.aws.amazon.com/wavelength/latest/developerguide/get-started-wavelength.html) in the _AWS Wavelength Developer Guide_.

Wavelength Zones are not available in every Region. For information about the Regions that support Wavelength Zones, see [Available Wavelength Zones](https://docs.aws.amazon.com/wavelength/latest/developerguide/wavelength-quotas.html) in the _AWS Wavelength Developer Guide_.

![[Pasted image 20221114120408.png]]