Depending on your use case, [[Storage Gateway]] provides three types of storage interfaces for your on-premises applications: file, volume, and tape.

The Volume Gateway provides block storage to your on-premises applications using iSCSI connectivity. Data on the volumes is stored in Amazon [[S3]] and you can take point-in-time copies of volumes that are stored in AWS as Amazon [[EBS snapshot]]s. You can also take copies of volumes and manage their retention using AWS [[Backup]]. You can restore EBS snapshots to a Volume Gateway volume or an [[EBS volume]].