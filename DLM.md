Amazon Data Lifecycle Manager (Amazon DLM) is an automated procedure to back up the data stored on your Amazon EBS volumes. Use Amazon DLM to create lifecycle policies to automate snapshot management.

![[Pasted image 20221130044414.png]]

Data Lifecycle Manager ([[DLM]]) automates the creation, retention, and deletion of EBS snapshots and [[EBS-backed AMI]]s

-   Protects valuable data by enforcing a regular backup schedule
-   Create standardized AMIs that can be refreshed at regular intervals
-   Retain backups as required by auditors or internal compliance
-   Reduce storage costs by deleting outdated backups
-   Create disaster recovery backup policies that back up data to isolated accounts