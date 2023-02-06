## EC2 [[Pricing]]

[[EC2]] instance pricing various depending on many variables:
1) The type of buying option 
2) Selected [[AMI]] 
3) Selected [[instance type]] 
4) Region 
5) Data in/out 
6) Storage capacity

*Each time you start a stopped instance, AWS charges a minimum of one minute für usage of per second billing instances. After one minute, AWS charges only für the seconds you use.

## On-demand:

-   Good for users that want the low cost and flexibility of EC2 without any up-front payment or long-term commitment.
-   Applications with short term, spiky, or unpredictable workloads that cannot be interrupted.
-   Applications being developed or tested on [[EC2]] for the first time.

![[Pasted image 20221119215303.png]]

## Reserved Instance ([[RI]]):

-   Applications with steady state or predictable usage.
-   Applications that require reserved capacity.
-   Users can make up-front payments to reduce their total computing costs even further 
-   Can pay All Upfront, Partial Upfront, No Upfront
-   When the attributes of a used instance match the attributes of an RI the discount is applied
-   Reserves capacity in specified [[AZ]]
-   Does not reserve capacity; discount applies to all [[AZ]]s ([[Region]])

![[Pasted image 20221119215347.png]]

**Standard Reserved Instance**:
-   provide up to 75% off on-demand price.
*   Change AZ, instance size (Linux), networking type
-   Use `ModifyReservedInstances` API

**Convertible Reserved Instance** 
*   provide up to 54% off on-demand price.
*   provides the capability to change the attributes of the RI, if the exchange results in the creation of RIs of equal or greater value.
*   Change AZ, instance size (Linux), networking type + Change family, OS, tenancy, payment option
*   Use `ExchangeReservedInstances` API

![[Pasted image 20230202063246.png]]

## [[Spot Instance]]:

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

## Dedicated hosts:

-   Physical servers dedicated just for your use.
-   You then have control over which instances are deployed on that host.
-   Available as On-Demand or with Dedicated Host Reservation.
-   Useful if you have server-bound software licenses that use metrics like per-core, per-socket, or per-VM.
-   Each dedicated host can only run one [[EC2]] instance size and type.
-   Good for regulatory compliance or licensing requirements.
-   Predictable performance.
-   Complete isolation.
-   Most expensive option.
-   Billing is per host.

## Dedicated instances:

-   Virtualized instances on hardware just for you.
-   Also uses physically dedicated [[EC2]] servers.
-   Does not provide the additional visibility and controls of dedicated hosts (e.g. how instances are placed on a server).
-   Billing is per instance.
-   May share hardware with other non-dedicated instances in the same account.
-   Available as On-Demand, Reserved Instances, and Spot Instances.
-   **Cost additional $2 per hour per region.

## Savings Plans:

-   Savings Plans is a flexible pricing model that provides savings of up to 72% on your AWS compute usage.
-   This pricing model offers lower prices on Amazon EC2 instances usage, regardless of instance family, size, OS, tenancy, or AWS Region.
-   1 or 3-year

**Compute Savings Plan**:
*   hourly commitment to usage of [[Fargate]], [[Lambda]], and [[EC2]]
*   Any [[Region]], [[instance type]] family, size, tenancy, and [[OS]]

**EC2 Savings Plan:**
*   hourly commitment to usage of [[EC2]] 
*   within a selected [[Region]] and [[instance type]] Family
*   Any size, tenancy and [[OS]]

![[Pasted image 20221119215514.png]]

## EBS Volume costs

Once an EC2 instance is stopped, CPU usage and data transfer charges cease, but storage charges for any attached [[EBS volume]]s continue.