## AWS Elastic Block Store (EBS)

Amazon Elastic Block Store (EBS) provides persistent block storage volumes for use with Amazon EC2 instances in the AWS Cloud. Each Amazon [[EBS volume]] is automatically replicated within its Availability Zone ([[AZ]]) to protect you from component failure, offering high availability and durability. Amazon EBS volumes offer the consistent and low-latency performance needed to run your workloads. With Amazon EBS, you can scale your usage up or down within minutes—all while paying a low price for only what you provision.

![[Pasted image 20221116130656.png]]

### EBS Volume

[[EBS volume]] data persists independently of the life of the instance
-   EBS volumes do not need to be attached to an instance
-   You can attach multiple EBS volumes to an instance
-   You can use multi-attach to attach a volume to multiple instances but with some constraints
-   EBS volumes must be in the same [[AZ]] as the instances they are attached to
-   Root EBS volumes are deleted on termination by default
-   Extra non-boot volumes are not deleted on termination by default
- 
### EBS snapshots

[[EBS Snapshot]]s are **a point-in-time copy of your data**, and can be used to enable disaster recovery, migrate data across [[region]]s and accounts, and improve backup compliance. You can create and manage your EBS Snapshots through the AWS Management Console, AWS Command Line Interface ([[CLI]]), or the [[AWS SDK]]s.

![[Pasted image 20221116132007.png]]

-   Snapshots capture a point-in-time state of an instance
-   Snapshots are stored on [[S3]]
-   If you make periodic snapshots of a volume, the snapshots are incremental
-   [[EBS volume]]s are [[AZ]] specific but snapshots are region specific