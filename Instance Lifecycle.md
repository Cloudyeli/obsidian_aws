##### - Stopping [[EC2]] instances:
-   EBS backed instances only
-   No charge for stopped instances
-   [[EBS volume]]s remain attached (chargeable)
-   Data in RAM is lost
-   Instance is migrated to a different host
-   Private IPv4 addresses and IPv6 addresses retained; public IPv4 addresses released
-   Associated Elastic IPs retained

##### - Hibernating EC2 instances
*   EBS backed instances only
*   Applies to on-demand or reserved Linux instances
*   Contents of RAM saved to [[EBS volume]]  
*   Must be enabled for hibernation when launched  
*   Specific prerequisites apply

When started (after hibernation):
*   The [[EBS]] root volume is restored to its previous state
-   The RAM contents are reloaded
-   The processes that were previously running on the instance are resumed
-   Previously attached data volumes are reattached and the instance retains its instance ID

##### - Rebooting EC2 instances
*   Equivalent to an OS reboot  
*   DNS name and all IPv4 and IPv6 addresses retained
*   Does not affect billing

##### - Retiring EC2 instances
-   Instances may be retired if AWS detects irreparable failure of the underlying hardware that hosts the instance
-   When an instance reaches its **scheduled retirement date**, it is stopped or terminated by AWS

##### - Terminating EC2 instances
*   Means deleting the EC2 instance  
*   Cannot recover a terminated instance  
*   By default root [[EBS volume]]s are deleted

##### - Recovering EC2 instances
-   [[CloudWatch]] can be used to monitor [[system status check]]s and recover instance if needed
-   ==Remember: Thats when AWS needs to do somethink to help revover the instance ([[system status check]])
-   Applies if the instance becomes impaired due to underlying hardware / platform issues
-   Recovered instance is identical to original instance

![[Pasted image 20230201191505.png]]