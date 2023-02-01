## Multi-factor authentication (MFA)

![[Pasted image 20230131141238.png]]

With [[IAM]] you can assign [[IAM User]]s individual security credentials such as access keys, passwords, and multi-factor authentication devices.

Multi-factor authentication (MFA) can be enabled/enforced for the AWS account and for individual users under the account.

MFA uses an authentication device that continually generates random, six-digit, single-use authentication codes.

![[Pasted image 20230131141338.png]]
![[Pasted image 20230131141409.png]]


You can authenticate using an MFA device in the following two ways:

-   Through the **AWS Management Console** – the user is prompted for a user name, password, and authentication code.
-   Using the **AWS API** – restrictions are added to IAM policies and developers can request temporary security credentials and pass MFA parameters in their AWS [[STS]] API requests.
-   Using the **AWS CLI** by obtaining temporary security credentials from AWS [[STS]] (aws sts get-session-token).

It is a best practice to always setup multi-factor authentication on the root account.