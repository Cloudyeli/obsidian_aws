## AWS Auto Scaling

AWS Auto Scaling is an Amazon service that lets you configure automatic scaling of AWS resources. It increases computing power or storage resources available for applications when loads increase, and reduces it when no longer needed. 
The AWS Auto Scaling Console provides a single user interface to use the auto scaling capabilities of various AWS services. 

*   AWS Auto Scaling lets you configure and manage scalability using scaling strategies.
*   This lets you determine how to optimise resource usage by favouring availability, cost, or a balance between the two. 
*   It is also possible to create custom scaling strategies.
*   You can also leverage **scaling plans**. These are [[scaling policies]] that adjust resources using dynamic or predictive scaling.

##### AWS Auto Scaling can be used to scale:

*   Amazon Elastic Compute Cloud ([[EC2]])
*   EC2 [[Spot Fleet]] requests
*   Elastic Container Service ([[ECS]])
*   [[DynamoDB]]
*   Amazon [[Aurora]]

## Amazon [[EC2]] Auto Scaling

-   [[EC2]] Auto Scaling launches and terminates instances dynamically
-   Scaling is horizontal ([[scaling out]])
-   Provides elasticity and scalability
-   Responds to [[EC2]] [[Instance status check]]s and [[CloudWatch metrics]]
-   Can scale based on demand (performance) or on a schedule
-   [[Scaling policies]] define how to respond to changes in demand
-   Auto Scaling groups ([[ASG]]) define collections of [[EC2]] instances that are scaled and managed together

![[Pasted image 20221116160642.png]]

## Auto Scaling Group ([[ASG]])

An Auto Scaling group (ASG) **contains a collection of [[EC2]] instances that are treated as a logical grouping for the purposes of automatic scaling and management**. 

##### A Launch Template specifies the EC2 instance configuration:

*   Configure purchase options – On-demand vs. Spot
*   Configure [[VPC]] and [[Subnet]]s
*   Attach an Elastic Load Balancer ([[ELB]])
*   Configure [[health check]]s - [[EC2]] & [[ELB]]
*   Group size and [[scaling policies]]
*   Launch Configurations are replaced by [[launch template]]s and have fewer features

![[Pasted image 20230204100528.png]]

## EC2 [[Auto Scaling]]

An Auto Scaling group (ASG) also lets you use Amazon EC2 [[Auto Scaling]] features such as health check replacements and [[scaling policies]].

*   Responds to [[EC2]] status checks and [[CloudWatch metrics]]
*   Can scale based **on demand** (performance) or on a **schedule**
*   [[Scaling policies]] define how to respond to changes in demand

![[Pasted image 20221117095351.png]]

### How to use a [[ASG]]?

1. Create [[launch template]] (more powerful) or launch config for your [[EC2]] Instances.
2. Create Autoscaling Group ([[ASG]])
3. Select launch template
4. Add a Load Balancer ([[ELB]]) (optional)
5. Select [[target group]] if you add a [[ELB]]
6. Enable Group metrics (get ASG metrics with 1 min granularity for **free**)
7. choose min and max capacity
8. choose a scaling policy (optional)

**[[warm pool]]:** - pre-initialised instances that are sort of ready to go into action when they are needed.
**Start instance refresh:** - replace instances
**[[fault tolerance]]** is where we have the ability to recover in the case of something like a component failure.

==You cant do ASGs across regions, but what you can do is create an ASG in a second region with a capacity set to 0. That means there's not going to be any Instances running, so you are not waisting money.==

## [[Health check]]s

*   [[EC2]] = EC2 [[Instance status check]]s
*   [[ELB]] = Uses the ELB health checks in addition to EC2 [[Instance status check]]s
**Health check grace period:**
*   How long to wait before checking the health status of the [[EC2]] instance
*   [[Auto Scaling]] does not act on health checks until grace period expires

#### Scaling is horizontal ([[scaling out]]), !NOT vertical ([[scaling up]])

## Auto Scaling - [[Monitoring]]

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

## [[Scaling policies]] include:  

##### - [[Target Tracking]]
*   Attempts to keep the group at or close to the metric
##### - [[Simple Scaling]]
*   Adjust group size based on a metric
##### - [[Step Scaling]]
*   Adjust group size based on a metric – adjustments vary based on the size of the alarm breach
##### - [[Scheduled Scaling]]
*   Adjust the group size at a specific time

##### Additional Scaling Settings:

##### - [[Cooldown]]s
*   Used with [[simple scaling]] policy to prevent Auto Scaling from launching or terminating before effects of previous activities are visible. 
*   Default value is 300 seconds (5 minutes)
##### - [[Termination Policy]]
*   Controls which instances to terminate first when a scale-in event occurs
##### - [[Termination Protection]]
*   Prevents Auto Scaling from terminating protected instances
##### - [[Standby State]]
*   Used to put an instance in the `InService` state into the `Standby` state, to update or troubleshoot the instance
##### - [[Lifecycle Hook]]s
*   Used to perform custom actions by pausing instances as the ASG launches or terminates them.
Use case:
*   Run a script to download and install software after launching
*   Pause an instance to process data before a scale-in (termination)




