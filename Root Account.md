The “root account” is the account created when you setup the AWS account. It has complete Admin access and is the only account that has this access by default.

*  It is a best practice to avoid using the root account for anything other than billing.
* The account root user credentials are the email address used to create the account and a password.
* The root account has full administrative permissions, and these cannot be restricted.

#### Best practice for root accounts:
-   Don’t use the root user credentials.
-   Don’t share the root user credentials.
-   Create an [[IAM user]] and assign administrative permissions as required.
-   Enable [[MFA]].