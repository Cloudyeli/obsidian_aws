## Availability Zone (AZ)
## Part of: [[AWS Global Infrastructure]]

*   Availability Zones are physically separate and isolated from each other  
*   AZs span one or more data centers and have direct, low-latency, high throughput, and redundant network connections between each other.
*   Each AZ is designed as an independent failure zone
An Availability Zone is represented by a region code followed by a letter identifier; for example, **us-east-1a.**

To ensure that resources are distributed across the Availability Zones for a region, AWS independently map Availability Zones to names for each AWS account. For example, the Availability Zone **_us-east-1a_** for your AWS account might not be the same location as **us-east-1a** for another AWS account.

*   To coordinate Availability Zones across accounts, you must use the _AZ ID_, which is a unique and consistent identifier for an Availability Zone.
*   AZs are physically separated within a typical metropolitan region and are in lower risk flood plains.
*   AZs use discrete UPS and onsite backup generation facilities and are fed via different grids from independent facilities.
*   AZs are all redundantly connected to multiple tier-1 transit providers.

The following graphic shows three AWS Regions each of which has three Availability Zones:

![aws-regions-availability-zones](https://digitalcloud.training/wp-content/uploads/2022/02/aws-regions-availability-zones.png)