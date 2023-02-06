Information/Data about the performance of your [[EC2]] Instance is getting sent to [[CloudWatch]] monitoring service.

*   With monitoring you [[EC2]] instance will send metric data to [[CloudWatch]] every 5 minutes (free)
*   You can enable **detailed monitoring**, if you want that the instance send data every 1 minute (cost)

## Auto Scaling - Monitoring

##### - Group metrics ([[ASG]])
*   Data points about the Auto Scaling group ([[ASG]])
*   1-minute granularity  
*   No charge  
*   Must be enabled

##### - Basic monitoring ([[EC2]] Instances)
*   5-minute granularity  
*   No Charge

##### - Detailed monitoring ([[EC2]] Instances)
*   1-minute granularity
*   Charges apply
*   [[CloudWatch]] detailed monitoring is **enabled by default** when creating launch configurations through the [[CLI]].