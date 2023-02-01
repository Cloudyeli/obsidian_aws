## AWS Elastic File System (EFS)

Amazon Elastic File System (EFS) is **a simple, serverless, set-and-forget, elastic file system**. There is no minimum fee or setup charge. You pay only for the storage you use, for read and write access to data stored in Infrequent Access storage classes, and for any provisioned throughput.

![[Pasted image 20221116140013.png]]

EFS is a fully managed service that makes it easy to set up and scale file storage in the Amazon Cloud.

Good for big data and analytics, media processing workflows, content management, web serving, home directories etc.

EFS uses the NFS protocol.

Pay for what you use (no pre-provisioning required).

Can scale up to petabytes.

EFS is elastic and grows and shrinks as you add and remove data.

Can concurrently connect 1 to 1000s of EC2 instances, from multiple AZs.

A file system can be accessed concurrently from all AZs in the region where it is located.

By default you can create up to 10 file systems per account.



Can choose General Purpose or Max I/O (both SSD).


The VPC of the connecting instance must have DNS hostnames enabled.
On-premises access can be enabled via Direct Connect or AWS VPN.

EFS provides a file system interface, file system access semantics (such as strong consistency and file locking).

Data is stored across multiple AZs within a region.

Read after write consistency.

Need to create mount targets and choose AZs to include (recommended to include all AZ’s).

Instances can be behind an ELB.

There are two performance modes:

-   “General Purpose” performance mode is appropriate for most file systems.
-   “Max I/O” performance mode is optimized for applications where tens, hundreds, or thousands of EC2 instances are accessing the file system.

Amazon EFS is designed to burst to allow high throughput levels for periods of time.

![amazon-efs-filesystems](https://digitalcloud.training/wp-content/uploads/2022/02/amazon-efs-filesystems.png)
*   File-based storage system 
*   Uses the [[NFS]] protocol  
*   Can connect many [[EC2]] instance concurrently  
*   EC2 instances can be connected from multiple [[AZ]]s
*   Only available for Linux instances
*   Can connect instances from other [[VPC]]s
*   The VPC of the connecting instance must have DNS hostnames enabled.
*   On-premises access can be enabled via [[Direct Connect]] or [[AWS VPN]].