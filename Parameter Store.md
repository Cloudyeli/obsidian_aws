## AWS Parameter Store
#(AWS [[Systems Manager]])

AWS [[Systems Manager]] provides a centralized store to manage your configuration data, whether plain-text data such as database strings or secrets such as passwords. This allows you to separate your secrets and configuration data from your code. Parameters can be tagged and organized into hierarchies, helping you manage parameters more easily. For example, you can use the same parameter name, "db-string", with a different hierarchical path, "dev/db-string” or “prod/db-string", to store different values. [[Systems Manager]] is integrated with AWS Key Management Service ([[KMS]]), allowing you to automatically encrypt the data you store. You can also control user and resource access to parameters using AWS Identity and Access Management ([[IAM]]). Parameters can be referenced through other AWS services, such as Amazon [[ECS]], AWS [[Lambda]] and AWS [[CloudFormation]].

-   Provides secure, hierarchical storage for configuration data management and secrets management
-   It is highly scalable, available, and durable
-   You can store data such as passwords, database strings, and license codes as parameter values
-   You can store values as plaintext (unencrypted data) or
    ciphertext (encrypted data)
-   You can then reference values by using the unique name that you specified when you created the parameter

![[Pasted image 20221119180540.png]]