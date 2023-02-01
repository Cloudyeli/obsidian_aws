An Amazon EBS volume is **a durable, block-level storage device that you can attach to your instances**. After you attach a volume to an instance, you can use it as you would use a physical hard drive. EBS volumes are flexible.

![[Pasted image 20221130041502.png]]

-   EBS volume data persists independently of the life of the instance
-   EBS volumes do not need to be attached to an instance
-   You can attach multiple EBS volumes to an instance
-   You can use multi-attach to attach a volume to multiple instances but with some constraints
-   EBS volumes must be in the same [[AZ]] as the [[EC2]] instances they are attached to
-   Root EBS volumes are deleted on termination by default
-   Extra non-boot volumes are not deleted on termination by default

![[Pasted image 20221130041548.png]]
### [[Instance Type]]
![[Pasted image 20221130045504.png]]

### Solide State Drive (SSD)
![[Pasted image 20221130041659.png]]

![[Pasted image 20221116130845.png]]

### Hard Disk Drive (HDD)

![[Pasted image 20221130041848.png]]

![[Pasted image 20221116130903.png]]

### Features

![[Pasted image 20221130042003.png]]

## EBS [[Pricing]]

Once an [[EC2]] instance is stopped, CPU usage and data transfer charges cease, but storage charges for any attached EBS volumes continue

### [[EBS Snapshot]]

![[Pasted image 20221130042221.png]]

### AWS [[EBS Multi-Attach]] and AWS Date Lifecycle Manager ([[DLM]])

![[Pasted image 20221130044414.png]]

### Benefits

![[Pasted image 20221130044314.png]]

![[Pasted image 20221130044830.png]]
![[Pasted image 20221130045125.png]]

![[Pasted image 20221130045045.png]]

