## AWS Security Token Service (STS)

The **AWS Security Token Service (AWS STS)** is a web service that enables you to request temporary, limited-privilege credentials for [[IAM user]]s or for users that you authenticate (federated users). It is also been used by the [[IAM Role]], with the AssumeRole [[trust policy]].

![[Pasted image 20230131141528.png]]

[[Temporary security credentials]] work almost identically to long-term access key credentials that [[IAM user]]s can use, with the following differences:

-   Temporary security credentials are short-term.
-   They can be configured to last anywhere from a few minutes to several hours.
-   After the credentials expire, AWS no longer recognizes them or allows any kind of access to [[API]] requests made with them.
-   [[Temporary security credentials]] are not stored with the [[IAM user]] but are generated dynamically and provided to the user when requested.
-   When (or even before) the temporary security credentials expire, the user can request new credentials, if the user requesting them still has permission to do so.

### Advantages of STS are:

-   You do not have to distribute or embed long-term AWS security credentials with an application.
-   You can provide access to your AWS resources to users without having to define an AWS identity for them ([[temporary security credentials]]are the basis for [[IAM Role]]s and [[Identity Federation]]).
-   The temporary security credentials have a limited lifetime, so you do not have to rotate them or explicitly revoke them when they’re no longer needed.
-   After temporary security credentials expire, they cannot be reused (you can specify how long the credentials are valid for, up to a maximum limit)

### Users can come from three sources:

##### [[Identity Federation]] (typically [[AD]]):
-   Uses SAML 2.0.
-   Grants temporary access based on the users [[AD]] credentials.
-   Does not need to be a [[IAM user]].
-   Single sign-on ([[SSO]]) allows users to login to the AWS console without assigning IAM credentials.

### Federation with Mobile Apps:
-   Use Facebook/Amazon/Google or other OpenID providers to login.

### Cross Account Access:
-   Allows users from one AWS account access resources in another.
-   To make a request in a different account the resource in that account must have an attached resource-based policy with the permissions you need.
-   Or you must assume a [[IAM role]] ([[identity-based policy]]) within that account with the permissions you need.