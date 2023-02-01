IAM users can be created to represent applications, and these are known as “service accounts”.

* You can have up to 5000 users per AWS account.
* Each user account has a friendly name and an [[ARN]] which uniquely identifies the user across AWS.
* A unique ID is also created which is returned only when you create the user using the [[API]], Tools for Windows PowerShell, or the AWS [[CLI]].
* You should create individual [[IAM]] accounts for users (best practice not to share accounts).
* The [[Access Key]] ID and Secret Access Key are not the same as a password and cannot be used to login to the AWS console.
* The [[Access Key]] ID and Secret Access Key can only be used once and must be regenerated if lost.
* A [[password policy]] can be defined for enforcing password length, complexity etc. (applies to all users).
* You can allow or disallow the ability to change passwords using an [[IAM policy]].
