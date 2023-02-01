## AWS Config

AWS Config is a fully managed service that provides you with an AWS resource inventory, configuration history, and configuration change notifications to enable security and governance. With AWS Config you can discover existing AWS resources, export a complete inventory of your AWS resources with all configuration details, and determine how a resource was configured at any point in time. These capabilities enable compliance auditing, security analysis, resource change tracking, and troubleshooting.

Config is a service used for compliance relating the configuration of AWS resources.

*   AWS Config evaluates the configuration against desired configurations
*   Fully-managed service for compliance management
*   Helps with compliance auditing, security analysis, resource change tracking and troubleshooting

![[Pasted image 20221119160807.png]]

| Example Rule                             | Description                                                                                                                                                                  |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| s3-bucket-server-side-encryption-enabled | Checks that your Amazon [[S3]] bucket either has S3 default encryption enabled or that the S3 bucket policy explicitly denies put-object requests without server side [[encryption]] |
| restricted-ssh                           | Checks whether [[security group]]s that are in use disallow unrestricted incoming [[SSH]] traffic                                                                                    |
| rds-instance-public-access-check         | Checks whether the Amazon Relational Database Service ([[RDS]]) instances are not publicly accessible                                                                            |
| cloudtrail-enabled                       | Checks whether AWS [[CloudTrail]] is enabled in your AWS account                                                                                                                 |