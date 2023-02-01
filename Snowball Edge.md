## AWS Snowball Edge
#(AWS [[Snow Family]])

AWS Snowball Edge is a type of Snowball device with on-board storage and compute power for select AWS capabilities. Snowball Edge can do local processing and edge-computing workloads in addition to transferring data between your local environment and the AWS Cloud.

*   Snowball Edge devices have three options for device configurations—_Storage Optimized_, _Compute Optimized_, and _Compute Optimized with GPU_.
*   Snowball Edge Storage Optimized  
	*    Provides block storage and Amazon S3-compatible object storage
	*    Use for local storage and large-scale data transfer (max 80 TB)
* Snowball Edge Compute Optimized
	*    Provides block and object storage and optional GPU
	*    Use for data collection, machine learning ([[ML]]) and processing, and storage in environments with intermittent connectivity (edge use cases) (max 28/40 TB)
        
## Snowball Edge Device Options

-   **Snowball Edge Storage Optimized (for data transfer)** – This Snowball Edge device option has a 100 TB (80 TB usable) storage capacity.
    
-   **Snowball Edge Storage Optimized (with [[EC2]] compute functionality)** – This Snowball Edge device option has up to 80 TB of usable storage space, 24 vCPUs, and 80 GB of memory for compute functionality. It also comes with 1 TB of additional SSD storage space for block volumes attached to Amazon EC2 [[AMI]]s.
    
-   **Snowball Edge Compute Optimized** – This Snowball Edge device option has the most compute functionality, with 104 vCPUs, 416 GB of memory, and 28 TB of dedicated NVMe SSD for compute instances. This device configuration is available only in these [[region]]s: US East (Ohio) Region, US East (N. Virginia) Region, US West (N. California) Region, US West (Oregon) Region and AWS GovCloud (US).
    
    In other regions, Snowball Edge Compute Optimized has 52 vCPUs, 208 GB of memory, 42 TB (39.5 TB usable) storage space, and 7.68 of dedicated NVMe SSD for compute instances.
    
-   **Snowball Edge Compute Optimized with GPU** – This Snowball Edge device option is identical to the Compute Optimized option, except for an installed GPU, equivalent to the one available in the P3 Amazon [[EC2]] instance type. It has a storage capacity of 28 TB of dedicated NVMe SSD for compute instances.