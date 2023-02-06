## AWS Elastic Compute Cloud (EC2)

Amazon Elastic Compute Cloud (Amazon EC2) is a web service with which you can run virtual server “instances” in the cloud.

*   An EC2 instance is a virtual server
*   Each virtual server is known as an “instance”
-   EC2 hosts are managed by AWS.
-   Key pairs are used to securely connect to EC2 instances
-   EC2 is a [[region]]al service
-   Amazon EC2 instances can run the Windows, Linux, or MacOS operating systems ([[OS]]).
-   With EC2 you have full control at the operating system (OS) layer
-   Amazon Machine Image ([[AMI]]) is used to launch an EC2 instance – consists of[[ EBS snapshot]], permissions and configuration.
-   Data is stored on an [[EBS volume]] (virtual hard drive). 
-   Storage is either Amazon [[EBS]] (persistent) or Instance Store (non-persistent)
-   When you launch your instance, you have to choose an [[instance type]].
-   The [[instance type]] defines the hardware profile (and cost).
-   You can launched an EC2 instance in a private or public [[Subnet]] of your [[VPC]].
-   A [[Security Group]] controls inbound and outbound traffic

![[Pasted image 20230201094920.png]]
## Benefits of EC2 include:

-   **Elastic computing** – easily launch hundreds to thousands of EC2 instances within minutes.
-   **Completely controlled** – you control the EC2 instances with full [[root]]/administrative access.
-   **Flexible** – Choice of [[instance type]]s, operating systems, and software packages.
-   **Integrated** – EC2 is integrated with most AWS services such as [[S3]], [[RDS]], and [[VPC]] to provide a complete, secure solution.
-   **Reliable** – EC2 offers very high levels of availability and instances can be rapidly commissioned and replaced. [[SLA]]s of 99.99% for each region.
-   **Secure** – Fully integrated with Amazon VPC and security features ([[Security Group]]s, [[Network ACL]]s, and [[IPSec VPN]] features).
-   **Inexpensive** – Low cost, pay for what you use.

## Amazon EC2 [[Metadata]] and [[User Data]]

-  Instance [[metadata]] is data about your EC2 instance that you can use to configure or manage the running instance.
-  Instance metadata is available at: ==http://169.254.169.254/latest/meta-data
-   [[User data]] is data that is supplied by the [[IAM user]] at instance launch in the form of a [[script]].
- Instance user data is available at: ==http://169.254.169.254/latest/user-data
-   **User data and metadata are not encrypted.**
-   The Instance Metadata Query tool allows you to query the instance metadata without having to type out the full [[URI]] or category names.

## Amazone Machine Image ([[AMI]])

An Amazon Machine Image (AMI) is a special type of virtual appliance that is used to create a virtual machine within the Amazon Elastic Compute Cloud (EC2).

## Instance [[Status Check]]s

##### - [[System Status Check]]
*   Checks that the underlying hardware on which your [[EC2]] instance is running, is working operationally.
*   If there is a problem with a system status check, it means that AWS are going to need to be involved to actually fix that problem.
##### - [[Instance Status Check]]
*   AWS is checking the software networking configuration of your [[EC2]] instance itself.
*   Makes shure that the [[OS]] is configured correctly, so that your [[EC2]] instance is operational and it's communicating with the network
*   If there is a problem with the Instance status check, it means it would need your involvment as an AWS customer to fix that problem.

## [[Monitoring]]

Information/Data about the performance of your EC2 Instance is getting sent to [[CloudWatch]] monitoring service.
*   With monitoring you EC2 instance will send mertic data to [[CloudWatch]] every 5 minutes (free)
*   You can enable detailed monitoring, if you want that the instance send data every 1 minute (cost)

## EC2 [[Placement Group]]s

EC2 Placement Groups are a way to control how AWS deploys your EC2 instances and places them within your [[AZ]]s or across your [[AZ]]s.

##### - [[Cluster]]
*   packs instances **phisical** close together inside an [[AZ]] (in same rack or in adjacent racks)
*  Uses **enhanced networking**, low network latency and high throughput for inter- instance traffic.
*   This strategy enables workloads to achieve the **low-latency** network performance necessary for **tightly-coupled** node-to-node communication that is typical of **[[HPC]] applications**.
* 
##### - [[Partition]]
Spreads your instances across logical partitions such that groups of instances in one partition **do not share the underlying hardware** with groups of instances in different partitions.
*   This strategy is typically used by large **distributed and replicated workloads**, such as Hadoop, Cassandra, and Kafka
* Partitions can be in multiple [[AZ]]s (up to 7 per [[AZ]]).

##### - [[Spread]]
Strictly places a small group of EC2 instances across **distinct underlying hardware** to reduce correlated failures.
*   Each instance is located in a separate AWS rack
*   Can be within an [[AZ]] or across [[AZ]]s.


## [[IAM roles for EC2 instances]]

[[IAM role]]s can be used for granting applications running on EC2 instances permissions to AWS [[API]] requests using [[instance profile]]s.

## [[Instance Type]]s

Amazon [[EC2]] provides a wide selection of instance types optimized to fit different use cases.

Instance types comprise varying combinations of CPU, memory, storage, and networking capacity and give you the flexibility to choose the appropriate mix of resources for your applications.

Each instance type includes one or more instance sizes, allowing you to scale your resources to the requirements of your target workload.

## [[Network Interfaces]] ([[ENI]], [[ENA]]; [[EFA]])

##### - Elastic Network Interface ([[ENI]])
##### - Elastic Network Adapter ([[ENA]])
##### - Elastic Fabric Adapter ([[EFA]])

## Also intresting: Interaction of EC2, [[Network Interfaces]] and [[NAT for public IP adresses]]

## EC2 [[Instance Lifecycle]]

##### - Stopping EC2 instances
##### - Hibernating EC2 instances
##### - Rebooting EC2 instances
##### - Retiring EC2 instances
##### - Terminating EC2 instances
##### - Recovering EC2 instances 

## [[Nitro Enclave]]s and [[Nitro System]]s

## AWS [[EC2 Pricing]] ([[Pricing]])

##### - On-demand
##### - Reserved
##### - Spot
##### - Dedicated hosts
##### - Dedicated Instances
##### - Saving Plans

Once an EC2 instance is stopped, CPU usage and data transfer charges cease, but storage charges for any attached [[EBS volume]]s continue.



