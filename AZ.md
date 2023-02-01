## Availability Zone (AZ)

Availability Zones (AZs) are physically separate and isolated from each other.

AZs span one or more data centers and have direct, low-latency, high throughput, and redundant network connections between each other.

Each AZ is designed as an independent failure zone.

When you launch an instance, you can select an Availability Zone or let AWS choose one for you.

If you distribute your EC2 instances across multiple Availability Zones and one instance fails, you can design your application so that an instance in another Availability Zone can handle requests.

You can also use Elastic IP ([[EIP]]) addresses to mask the failure of an instance in one Availability Zone by rapidly remapping the address to an instance in another Availability Zone.

An Availability Zone is represented by a region code followed by a letter identifier; for example, **_us-east-1a._**

To ensure that resources are distributed across the Availability Zones for a region, AWS independently map Availability Zones to names for each AWS account.

For example, the Availability Zone **_us-east-1a_** for your AWS account might not be the same location as us-east-1a for another AWS account.

To coordinate Availability Zones across accounts, you must use the _AZ ID_, which is a unique and consistent identifier for an Availability Zone.

AZs are physically separated within a typical metropolitan region and are in lower risk flood plains.

AZs use discrete UPS and onsite backup generation facilities and are fed via different grids from independent facilities.

AZs are all redundantly connected to multiple tier-1 transit providers.

The following graphic shows three AWS Regions each of which has three Availability Zones:

![aws-regions-availability-zones](https://digitalcloud.training/wp-content/uploads/2022/02/aws-regions-availability-zones.png)