Create an [[IAM role]] with two policies:

[[Permissions policy]] – grants the [[IAM user]] of the role the required permissions on a resource.
[[Trust policy]] – specifies the trusted accounts that are allowed to assume the role.

-   Wildcards (`*`) cannot be specified as a principal.
-   A [[Permissions policy]] must also be attached to the [[IAM user]] in the trusted account ([[trust policy]]).