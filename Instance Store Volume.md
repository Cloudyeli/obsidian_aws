  ![[Pasted image 20221116134559.png]]
  
Instance store volumes **accesses storage from disks that are physically attached to the host computer**. When an Instance stored [[EC2]] instance is launched, the image that is used to boot the instance is copied to the root volume (typically sda1). Instance store provides temporary block-level storage for instances.

-   Instance store volumes are high performance local disks that are physically attached to the host computer on which an EC2 instance runs
-   Instance stores are ephemeral which means the data is lost when powered off (non-persistent)
-   Instances stores are ideal for temporary storage of information that changes frequently, such as buffers, caches, or scratch data