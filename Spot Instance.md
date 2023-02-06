## Spot instance [[Pricing]]: 

Use cases: 
-   Applications that have flexible start and end times.
-   Applications that are only feasible at very low compute prices.
-   Users with an urgent need for a large amount of additional compute capacity.
-   If Amazon terminate your instances you do not pay, if you terminate you pay for the hour.
-   Bid for unused capacity at up to 90% discount

**2-minute warning if AWS need to reclaim capacity – available via instance [[metadata]] and [[CloudWatch Events]]**

##### - Spot Instance 
*   One or more EC2 instances
##### - Spot Fleet
*   launches and maintains the number of Spot / On-Demand instances to meet specified target capacity
##### - EC2 Fleet: 
*   launches and maintains specified number of Spot / On-Demand / Reserved instances in a **single [[API]] call**
*   Can define separate OD/Spot capacity targets, bids, [[instance type]]s, and [[AZ]]s
##### - Spot Block
*   Requirement: Uninterrupted for 1-6 hours
*   Pricing is 30% - 45% less than On-Demand

![[Pasted image 20230202070930.png]]
