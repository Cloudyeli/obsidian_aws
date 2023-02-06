## Source Network Address Translation (SNAT)

Source Network Address Translation (SNAT) is a networking technique used to map one IP address space into another by modifying network address information in the IP header of packets while they are in transit across a traffic routing device. The technique was originally used for ease of rerouting traffic in IP networks without readdressing every host.

In Amazon Web Services (AWS), SNAT is used in a Virtual Private Cloud ([[VPC]]) environment to allow outbound traffic initiated from instances in a private subnet to access the Internet, while hiding the original private IP addresses of the instances behind a single, public IP address or a group of public IP addresses.