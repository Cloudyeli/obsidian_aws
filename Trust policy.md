Specifies the trusted accounts that are allowed to assume the [[IAM role]].

*   Control who can assume the IAM Role, so who is allowed to assume this role and become this role and act as if they are the role? So the trustpolicy allows the principal to assume the role.
*   The [[STS]] Service gets involved and returns temporary security credentials to the principal, so that the principal can access the AWS service with this temporary credentials and take the allowed actions.

![[Pasted image 20230201060137.png]]