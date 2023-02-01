A virtual tape library (VTL) is a hardware component that can emulate a tape library while using a disk as the underlying storage hardware.

Using a VTL, you can create variable numbers of drives and volumes because they are only logical entities within the VTL. The ability to create more drives and volumes increases the capability for parallelism, giving you more simultaneous mounts and tape I/O.

VTLs use SCSI and Fibre Channel interfaces to interact with applications. Because VTLs emulate tape drives, libraries, and volumes, an application such as Tivoli® Storage Manager cannot distinguish a VTL from real tape hardware unless the library is identified as a VTL.