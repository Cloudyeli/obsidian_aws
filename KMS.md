## Key Management Service (KMS)

AWS Key Management Service (AWS KMS) lets you create, manage, and control cryptographic keys across your applications and more than 100 AWS services.
Use AWS KMS to encrypt data across your AWS workloads, digitally sign data, encrypt within your  applications using AWS [[Encryption SDK]], and generate and verify message authentication codes ([[MAC]]s).

*   Used for creating and managing encryption keys
-   Gives you centralized control over the encryption keys used to protect your data
-   KMS is integrated with most other AWS services
-   Easy to encrypt the data you store in these services with encryption keys you control
-   Create and managed symmetric and asymmetric encryption keys
-   The customer master keys ([[CMK]]s) are protected by hardware security modules ([[HSM]]s)

![[Pasted image 20221119175053.png]]

## AWS [[CloudHSM]] vs. AWS KMS

|  |AWS [[CloudHSM]] | AWS [[KMS]] |
| - | -------- | ---------- |
| **Tenancy** | Single-tenant | HSM Multi-tenant AWS service
| Availability | Customer-managed durability and availabile | Highly available and durable key storage available and management
| Root of Trust | Customer managed root of trust | AWS managed root of trust
| FIPS 140-2 | Level 3 | Level 2 / Level 3 in some areas
| 3rd Party Support | Broad 3rd Party Support | Broad AWS service support

