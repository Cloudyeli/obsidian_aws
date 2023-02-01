EBS Snapshots are **a point-in-time copy of your data**, and can be used to enable disaster recovery, migrate data across [[region]]s and accounts, and improve backup compliance. You can create and manage your EBS Snapshots through the AWS Management Console, AWS Command Line Interface ([[CLI]]), or the [[AWS SDK]]s.

![[Pasted image 20221116132007.png]]

![[Pasted image 20221130042240.png]]

-   Snapshots capture a point-in-time state of an instance
-   Snapshots are stored on [[S3]]
-   If you make periodic snapshots of a volume, the snapshots are incremental
-   [[EBS volume]]s are [[AZ]] specific but snapshots are region specific

## Data Lifecycle Manager ([[DLM]])

Data Lifecycle Manager ([[DLM]]) automates the creation, retention, and deletion of EBS snapshots and [[EBS-backed AMI]]s

-   Protects valuable data by enforcing a regular backup schedule
-   Create standardized AMIs that can be refreshed at regular intervals
-   Retain backups as required by auditors or internal compliance
-   Reduce storage costs by deleting outdated backups
-   Create disaster recovery backup policies that back up data to isolated accounts
