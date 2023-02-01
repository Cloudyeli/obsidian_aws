## AWS Auto Scaling

AWS Auto Scaling is an Amazon service that lets you configure automatic scaling of AWS resources. It increases computing power or storage resources available for applications when loads increase, and reduces it when no longer needed. 

The AWS Auto Scaling Console provides a single user interface to use the auto scaling capabilities of various AWS services. AWS Auto Scaling can be used to scale Amazon Elastic Compute Cloud ([[EC2]]), EC2 [[Spot Fleet]] requests, Elastic Container Service ([[ECS]]), [[DynamoDB]], and Amazon [[Aurora]].

*   AWS Auto Scaling lets you configure and manage scalability using scaling strategies.
*   This lets you determine how to optimize resource usage by favoring availability, cost, or a balance between the two. 
*   It is also possible to create custom scaling strategies.
*   You can also leverage **scaling plans**. These are policies that adjust resources using dynamic or predictive scaling.

## Amazon [[EC2 Auto Scaling]]

![[Pasted image 20221116160642.png]]

-   Automates scaling of [[EC2]] instances
-   Launches and terminates EC2 instances based on demand (dynamically)
-   Helps to ensure that you have the correct number of EC2 instances available to handle the application load
-   Amazon EC2 Auto Scaling provides **elasticity** and **scalability**
-   You create collections of EC2 instances, called an Auto Scaling group ([[ASG]])

### Scaling policies include:  

*   **Target Tracking** – Attempts to keep the group at or close to the metric
-   **Simple Scaling** – Adjust group size based on a metric
-   **Step Scaling** – Adjust group size based on a metric – adjustments vary based on the size of the alarm breach
-   **Scheduled Scaling** – Adjust the group size at a specific time

#### Scaling is horizontal ([[scaling out]]), !NOT vertical ([[scaling up]])

## Auto Scaling Group ([[ASG]])

An Auto Scaling group (ASG) **contains a collection of [[EC2]] instances that are treated as a logical grouping for the purposes of automatic scaling and management**. 

An Auto Scaling group (ASG) also lets you use Amazon [[EC2 Auto Scaling]] features such as health check replacements and scaling policies.

*   Responds to [[EC2]] status checks and [[CloudWatch]] metrics
*   Can scale based **on demand** (performance) or on a **schedule**
*   Scaling policies define how to respond to changes in demand

