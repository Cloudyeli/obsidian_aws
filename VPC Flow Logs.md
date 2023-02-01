## AWS VPC Flow Logs

AWS Flow Logs capture information about the IP traffic going to and from network interfaces in a [[VPC]]

*   Flow log data is stored using Amazon [[CloudWatch Logs]]

## Flow logs can be created at the following levels:

*   VPC  
*   Subnet  
*   Network interface

## To create a flow log, you specify:

-   The resource for which to create the flow log
-   The type of traffic to capture (accepted traffic, rejected traffic, or all traffic)
-   The destinations to which you want to publish the flow log data

In the following example, you create a flow log that captures accepted traffic for the network interface for one of the EC2 instances in a private subnet and publishes the flow log records to an Amazon [[S3]] bucket.

![Flow logs for an instance](https://docs.aws.amazon.com/images/vpc/latest/userguide/images/flow-logs-diagram_s3_updated.png)

In the following example, a flow log captures all traffic for a subnet and publishes the flow log records to Amazon [[CloudWatch Logs]]. The flow log captures traffic for all network interfaces in the subnet.

![Flow logs for a subnet](https://docs.aws.amazon.com/images/vpc/latest/userguide/images/flow-logs-diagram_cw_updated.png)