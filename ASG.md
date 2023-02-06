### Part of: [[Auto Scaling]]

An Auto Scaling group (ASG) **contains a collection of [[EC2]] instances that are treated as a logical grouping for the purposes of automatic scaling and management**. 

##### A Launch Template specifies the EC2 instance configuration:

*   Configure purchase options – On-demand vs. Spot
*   Configure [[VPC]] and [[Subnet]]s
*   Attach an Elastic Load Balancer ([[ELB]])
*   Configure [[health check]]s - [[EC2]] & [[ELB]]
*   Group size and scaling policies
*   Launch Configurations are replaced by [[launch template]]s and have fewer features
* 
![[Pasted image 20230204100528.png]]

## EC2 [[Auto Scaling]]

An Auto Scaling group (ASG) also lets you use Amazon EC2 [[Auto Scaling]] features such as health check replacements and [[scaling policies]].

*   Responds to [[EC2]] status checks and [[CloudWatch]] metrics
*   Can scale based **on demand** (performance) or on a **schedule**
*   [[Scaling policies]] define how to respond to changes in demand

![[Pasted image 20221117095351.png]]

### How to use a ASG?

1. Create [[launch template]] (more powerful) or launch config for your [[EC2]] Instances.
2. Create Autoscaling Group (ASG)
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