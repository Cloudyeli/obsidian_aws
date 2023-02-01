AWS Identity and Access Management (IAM) allows you to manage access to AWS services and resources.

-   IAM is used to securely control individual and group access to AWS resources
-   IAM makes it easy to provide multiple users secure access to AWS resources

![[Pasted image 20230131120518.png]]

You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.

## IAM can be used to manage:

-   [[IAM User]]s.
-   [[IAM Group]]s.
-   Access [[policies]].
-   [[IAM Role]]s.
-   User credentials.
-   User [[password policy\|password policies]].
-   Multi-factor authentication ([[MFA]]).
-   API keys for programmatic access ([[CLI]]).

![[Pasted image 20230131120702.png]]

## IAM provides the following features:

-   Shared access to your AWS account.
-   Granular permissions.
-   Secure access to AWS resources for application that run on Amazon [[EC2]].
-   Multi-Factor authentication ([[MFA]]).
-   [[Identity federation]].
-   Identity information for assurance.
-   [[PCI DSS]] compliance.
-   Integrated with many AWS services.
-   [[Eventually consistent]].
-   Free to use.

### You can work with AWS Identity and Access Management in any of the following ways:

-   AWS Management Console.
-   AWS Command Line ([[CLI]]) Tools.
-   [[AWS SDK]]s.
-   [IAM HTTPS API](https://docs.aws.amazon.com/IAM/latest/UserGuide/programming.html).

### By default new users are created with NO access to any AWS services – they can only login to the AWS console.

*   Permission must be explicitly granted to allow a user to access an AWS service.
*   [[IAM user]]s are individuals who have been granted access to an AWS account
*   You can apply granular permissions with IAM.
*   IAM is not used for application-level authentication.
*   IAM is universal (global) and does not apply to regions.
*   IAM replicates data across multiple data centers around the world.

#### [[Root account]]
When you first create an AWS account, you begin with a single sign-on ([[SSO]]) identity that has complete access to all AWS services and resources in the account.
*  This identity is called the AWS account _[[root]]_ _user_ and is accessed by signing in with the email address and password that you used to create the account.
*  The “root account” is the account created when you setup the AWS account. It has complete Admin access and is the only account that has this access by default.
*   It is a best practice to avoid using the root account for anything other than billing.

#### [[Power user access]]
*   Power user access allows all permissions except the management of groups and users in IAM.

#### [[Temporary security credentials]]
*  Temporary security credentials consist of the AWS access key ID, secret access key, and security token.
*   IAM can assign temporary security credentials to provide users with temporary access to services/resources.

#### Sign-in
*  To sign-in you must provide your account ID or account alias in addition to a user name and password.

#### Authentication Methods
*   [[Console password]] - use to login to AWS Management Console
*   [[Access Key]]s & Secret Access Keys - used for programmatic access
*   [[Server certificates]] - uses SSL/TLS certficates

![iam-authentication-methods](https://digitalcloud.training/wp-content/uploads/2022/02/iam-authentication-methods.png)

## [[IAM Security Tools]]

##### - IAM [[Credential Report]] (account-level)  
*   a report that lists all your account's users and the status of their various credentials
##### - IAM [[Access Advisor]] (user-level)  
*   shows the service permissions granted to a [[IAM user]] and when those services were last accessed.  
*   You can use this information to revise your [[policies]].

## [[IAM Best Practice]]s

*   Lock away your AWS account root user access keys
*   Create individual IAM users  
*   Use [[IAM group]]s to assign permissions to [[IAM user]]s  
*   Grant least privilege
*   Get started using permissions with AWS [[managed policy\|managed policies]]
*   Use customer managed policies instead of [[inline-policy\|inline-polices]]
*   Use access levels to review IAM permissions  
*   Configure a strong password policy for your users
*   Enable MFA
-   Use roles for applications that run on Amazon EC2 instances
-   Use [[IAM role]]s to [[Role Delegation\|delegate permissions]]
-   Do not share access keys
-   Rotate credentials regularly
-   Remove unnecessary credentials
-   Use policy conditions for extra security
-   Monitor activity in your AWS account

## IAM Section – Summary

*   [[IAM User]]s: mapped to a physical user, has a password for AWS Console  
*   [[IAM Group]]s: contains users only  
*   IAM [[Policies]]: JSON document that outlines permissions for users or groups
*   [[IAM Role]]s: for EC2 instances or AWS services  
*   Security: [[MFA]] + [[Password Policy]]  
*   [[Access Key]]s: access AWS using the [[CLI]] or [[SDK]]  
*   [[IAM security tools\|Audit]]: IAM [[Credential Report]]s & IAM [[Access Advisor]]