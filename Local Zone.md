## AWS Local Zones
## Part of: [[AWS Global Infrastructure]]

AWS Local Zones place compute, storage, database and other select AWS services closer to end-users

*   Extension of an AWS [[Region]] where you can run your latency sensitive applications
*   AWS Local Zones place compute, storage, database, and other select AWS services closer to end-users.
*   Each AWS Local Zone location is an extension of an AWS [[Region]] where you can run your latency sensitive applications using AWS services such as Amazon Elastic Compute Cloud ([[EC2]]), Amazon Virtual Private Cloud ([[VPC]]), Amazon Elastic Block Store ([[EBS]]), Amazon File Storage ([[EFS]]), and Amazon Elastic Load Balancing ([[ELB]]) in geographic proximity to end-users.
*   

Use cases:

-   Single-digit ms latency to end users / apps
-   Live video, [[ML]], [[AR]]/[[VR]]

![[Pasted image 20230205154338.png]]

----- 

A Local Zone is an extension of an AWS Region that is geographically close to your users. You can extend any virtual private cloud (VPC) from the parent AWS Region into Local Zones by creating a new subnet and assigning it to the AWS Local Zone. When you create a subnet in a Local Zone, your VPC is extended to that Local Zone. The subnet in the Local Zone operates the same as other subnets in your VPC. AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end users, giving them low latency access to their local applications. AWS Local Zones are also connected to the parent region by using Amazon’s redundant and high-bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.

AWS Local Zones place compute, storage, database, and other select AWS services closer to end-users.

With AWS Local Zones, you can easily run highly demanding applications that require single-digit millisecond latencies to your end-users.



AWS Local Zones provide a high-bandwidth, secure connection between local workloads and those running in the AWS Region, allowing you to seamlessly connect to the full range of in-region services through the same APIs and tool sets.