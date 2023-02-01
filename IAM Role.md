Roles are created and then “assumed” by trusted entities and define a set of permissions for making AWS service requests.

-   Roles are created and then “assumed” by trusted entities
-   With IAM Roles you can delegate permissions to resources for [[IAM user]]s and services
-   [[IAM user]]s or AWS services can assume a role to obtain temporary security credentials
-   Temporary security credentials are issued by the AWS Security Token Service ([[STS]])

![[Pasted image 20221114160630.png]]

## There are two different [[policies]] that apply to the IAM Role:

##### - [[trust policy]]
*   Control who can assume the IAM Role, so who is allowed to assume this role and become this role and act as if they are the role? So the trustpolicy allows the principal to assume the role.
*   The [[STS]] Service gets involved and returns temporary security credentials to the principal, so that the principal can access the AWS service with this temporary credentials and take the allowed actions.
*   A trust policy is also an example of a [[resource-based policy]]

##### - [[Permissions policy]]
*   These define the permission that are allowed or denied to this specific entity.
*   A permission policy is an [[identity-based policy]].

### [[Role Delegation]]

Create an IAM role with two policies:

[[Permissions policy]] – grants the [[IAM user]] of the role the required permissions on a resource.
[[Trust policy]] – specifies the trusted accounts that are allowed to assume the role.

-   Wildcards (`*`) cannot be specified as a principal.
-   A [[Permissions policy]] must also be attached to the [[IAM user]] in the trusted account ([[trust policy]]).

![[Pasted image 20230201060749.png]]

## [[IAM roles for EC2 instances]]

-   [[IAM role]]s can be used for granting applications running on EC2 instances permissions to AWS [[API]] requests using [[instance profile]]s.
-   Only one role can be assigned to an [[EC2]] instance at a time.
-   A role can be assigned at the [[EC2]] instance creation time or at any time afterwards.
-   When using the AWS [[CLI]] or [[API]] [[instance profile]]s must be created manually (it’s automatic and transparent through the console).
-   Applications retrieve [[temporary security credentials]] from the instance [[metadata]].

## An IAM role is an identity that you can assume to gain temporary access to permissions.

![[Pasted image 20221114162018.png]]

*   With IAM Roles you can delegate permissions to resources for users and services without using permanent credentials (e.g. user name and password).
*   [[IAM user]]s can temporarily assume a role to take on permissions for a specific task.
*   [[IAM user]]s or AWS services can assume a role to obtain [[temporary security credentials]] that can be used to make AWS API calls.
*   Temporary security credentials are issued by the AWS Security Token Service ([[STS]])
*   You can delegate using roles.
*   There are no credentials associated with a role (password or [[access key]]s).
*   A role can be assigned to a federated user who signs in using an external identity provider ([[Identity federation]]).
* Temporary credentials are primarily used with IAM roles and automatically expire.
*   Roles can be assumed temporarily through the console or programmatically with the **AWS [[CLI]]**, **Tools for Windows PowerShell,** or the **[[API]].**