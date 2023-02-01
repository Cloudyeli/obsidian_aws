## AWS Elastic Container Service (ECS)

Amazon Elastic Container Service (ECS) is another product in the AWS Compute category. It provides a highly scalable, high performance container management service that supports [[Docker]] [[container]]s and allows you to easily run applications on a managed [[cluster]] of Amazon [[EC2 instances.

![[Pasted image 20221116125902.png]]

Amazon ECS eliminates the need for you to install, operate, and scale your own cluster management infrastructure.

Using [[API]] calls you can launch and stop container-enabled applications, query the complete state of clusters, and access many familiar features like [[security group]]s, Elastic Load Balancing ([[ELB]]), [[EBS]] volumes and [[IAM role]]s.

Amazon ECS can be used to schedule the placement of containers across clusters based on resource needs and availability requirements.

An Amazon ECS launch type determines the type of infrastructure on which your tasks and services are hosted.

There are two launch types, and the table below describes some of the differences between the two launch types:

| **Amazon [[EC2]]** | **Amazon [[Fargate]]** |
| ---------- | -------------- |
| You explicitly provision EC2 instances | The control plane asks for resources and Fargate automatically provisions |
| You’re responsible for upgrading, patching, care of EC2 pool | Fargate provisions compute as needed |
| You must handle cluster optimization  | Fargate handles cluster optimization|
| More granular control over infrastructure | Limited control, as infrastructure is automated|
![[Pasted image 20221116125954.png]]

### Elastic container registry ([[ECR]])

The Elastic container registry (ECR) is a managed AWS Docker registry service for storing, managing, and deploying Docker images.

There is no additional charge for Amazon ECS. You pay for AWS resources (e.g. [[EC2]] instances or [[EBS]] volumes) you create to store and run your application.

Amazon ECR is integrated with Amazon EC2 Container Service (ECS).

With Amazon ECR, there are no upfront fees or commitments. You pay only for the amount of data you store in your repositories and data transferred to the Internet.

==Summary:==
ECS is used for running Docker containers in the cloud
*   ECS containers are known as tasks
-   EC2 launch type:  
    *   You managed EC2 instances which are the hosts for running the tasks
-   Fargate launch type:
    *   AWS manage the underlying compute, cluster, and scaling
-   Amazon Elastic Container Registry (ECR) is a private
    container image registry


