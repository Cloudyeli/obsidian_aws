## AWS Nitro Enclaves

AWS Nitro Enclaves enables customers to create isolated compute environments to further protect and securely process highly sensitive data such as personally identifiable information ([[PII]]), healthcare, financial, and intellectual property data within their Amazon [[EC2]] instances. Nitro Enclaves uses the same Nitro Hypervisor technology that provides CPU and memory isolation for EC2 instances.

*   Enclaves are fully isolated virtual machines, hardened, and highly constrained. 
*   There are no additional charges for using AWS Nitro Enclaves other than the use of Amazon EC2 instances and any other AWS services that are used with Nitro Enclaves.

## Benefits

### Additional isolation and security

Enclaves are fully isolated virtual machines, hardened, and highly constrained. They have no persistent storage, no interactive access, and no external networking. Communication between your instance and your enclave is done using a secure local channel. Even a [[root]] user or an admin user on the instance will not be able to access or [[SSH]] into the enclave.

Nitro Enclaves uses the proven isolation of the Nitro Hypervisor to further isolate the CPU and memory of the enclave from users, applications, and libraries on the parent instance. These features help isolate the enclave and your software, and significantly reduce the attack surface area.  

### Cryptographic attestation

Attestation allows you to verify the enclave’s identity and that only authorized code is running in your enclave. The attestation process is accomplished through the Nitro Hypervisor, which produces a signed attestation document for the enclave to prove its identity to another party or service. Attestation documents contain key details of the enclave such as the enclave's public key, hashes of the enclave image and applications, and more. Nitro Enclaves includes AWS [[KMS]] integration, where KMS is able to read and verify these attestation documents that is sent from the enclave.  

### Flexible

Nitro Enclaves are flexible. You can create enclaves with varying combinations of CPU cores and memory. This ensures you have sufficient resources to run the same memory or compute intensive applications that you were already running on your existing [[EC2]] instances. Nitro Enclaves are processor agnostic, and can be used across instances powered by different CPU vendors. They are also compatible with any programming language or framework. Furthermore, because many components of Nitro Enclaves are open sourced, customer can even inspect the code and validate it themselves.