Amazon EBS Multi-Attach enables you to attach a single Provisioned IOPS SSD (`io1` or `io2`) volume to multiple instances that are in the same Availability Zone. You can attach multiple Multi-Attach enabled volumes to an instance or set of instances. Each instance to which the volume is attached has full read and write permission to the shared volume. Multi-Attach makes it easier for you to achieve higher application availability in clustered Linux applications that manage concurrent write operations.

![[Pasted image 20221130044431.png]]

## Considerations and limitations

-   Multi-Attach enabled volumes can be attached to up to 16 Linux instances built on the [Nitro System](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html#ec2-nitro-instances) that are in the same Availability Zone. You can attach a volume that is Multi-Attach enabled to Windows instances, but the operating system does not recognize the data on the volume that is shared between the instances, which can result in data inconsistency.
    
-   Multi-Attach is supported exclusively on [Provisioned IOPS SSD (io1 and io2) volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/provisioned-iops.html#EBSVolumeTypes_piops).
    
-   Multi-Attach for `io1` volumes is available in the following Regions only: US East (N. Virginia), US West (N. California), US West (Oregon), and Asia Pacific (Seoul).
    
    Multi-Attach for `io2` and `io2` Block Express volumes is available in all Regions that support those volumes types.
    
-   You can't attach a Multi-Attach enabled `io2` volume to instance types that support Block Express and instance types that do not support Block Express at the same time. For more information, see [io2 Block Express volumes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/provisioned-iops.html#io2-block-express).
    
-   `io1` volumes with Multi-Attach enabled are not supported with instance types that support io2 Block Express. To use Multi-Attach with these instance types, you must use io2 volumes.
    
-   Standard file systems, such as XFS and EXT4, are not designed to be accessed simultaneously by multiple servers, such as EC2 instances. Using Multi-Attach with a standard file system can result in data corruption or loss, so this is not safe for production workloads. You can use a clustered file system to ensure data resiliency and reliability for production workloads.
    
-   Multi-Attach enabled volumes do not support[[ I/O fencing]]. I/O fencing protocols control write access in a shared storage environment to maintain data consistency. Your applications must provide write ordering for the attached instances to maintain data consistency.
    
-   Multi-Attach enabled volumes can't be created as boot volumes.
    
-   Multi-Attach enabled volumes can be attached to one block device mapping per instance.
    
-   Multi-Attach can't be enabled during instance launch using either the Amazon EC2 console or RunInstances API.
    
-   Multi-Attach enabled volumes that have an issue at the Amazon EBS infrastructure layer are unavailable to all attached instances. Issues at the Amazon EC2 or networking layer might impact only some attached instances.
    
-   The following table shows volume modification support for Multi-Attach enabled `io1` and `io2` volumes after creation.

| | `io2` volumes | `io1` volumes |
| --- | -------- | ---------- |
| Modify volume type |✗ | ✗
|  Modify volume size | ✓ | ✗ |
|  Modify provisioned IOPS | ✓ | ✗
| Enable Multi-Attach | ✓* | ✗
| Disable Multi-Attach | ✓* | ✗
-   * You can't enable or disable Multi-Attach while the volume is attached to an instance.