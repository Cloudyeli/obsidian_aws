An Amazon Machine Image (AMI) is a special type of virtual appliance that is used to create a virtual machine within the Amazon Elastic Compute Cloud (EC2).
![[Pasted image 20221129225006.png]]


An AMI includes the following:

-   One or more [[EBS snapshot]]s, or, for [[instance store-backed AMI]]s, a template for the root volume of the instance (for example, an operating system, an application server, and applications).
-   Launch permissions that control which AWS accounts can use the AMI to launch instances.
-   A block device mapping that specifies the volumes to attach to the instance when it’s launched.

AMIs come in three main categories:

-   **Community AMIs** – free to use, generally you just select the operating system you want.
-   **AWS Marketplace AMIs** – pay to use, generally come packaged with additional, licensed software.
-   **My AMIs** – AMIs that you create yourself.

![ec2-instance-launch](https://digitalcloud.training/wp-content/uploads/2022/02/ec2-instance-launch-1.png)

## [Storage for the root device](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ComponentsAMIs.html)

All AMIs are categorized as either _backed by Amazon EBS_ or _backed by instance store_.

-   Amazon EBS-backed AMI – The root device for an instance launched from the AMI is an Amazon Elastic Block Store (Amazon [[EBS]]) volume created from an Amazon [[EBS snapshot]].
    
-   Amazon [[instance store-backed AMI]] – The root device for an instance launched from the AMI is an instance store volume created from a template stored in Amazon [[S3]].