## AWS CloudHSM

AWS CloudHSM is a cryptographic service for creating and maintaining **hardware security modules** (HSMs) in your AWS environment. HSMs are computing devices that process cryptographic operations and provide secure storage for cryptographic keys.

*   AWS CloudHSM is a cloud-based hardware security module ([[HSM]])  
*   Generate and use your own encryption keys on the AWS Cloud  
*   Manage your own encryption keys using FIPS 140-2 Level 3 validated HSMs 
*   CloudHSM runs in your [[VPC]]

## AWS CloudHSM vs. AWS [[KMS]]

|  |AWS [[CloudHSM]] | AWS [[KMS]] |
| - | -------- | ---------- |
| **Tenancy** | Single-tenant | HSM Multi-tenant AWS service
| Availability | Customer-managed durability and availabile | Highly available and durable key storage available and management
| Root of Trust | Customer managed root of trust | AWS managed root of trust
| FIPS 140-2 | Level 3 | Level 2 / Level 3 in some areas
| 3rd Party Support | Broad 3rd Party Support | Broad AWS service support

