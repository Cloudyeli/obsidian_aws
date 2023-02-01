An IAM group is a collection of [[IAM user]]s and have policies attached to them.

-   A group is not an identity and cannot be identified as a principal in an [[IAM policy]]
-   Use groups to assign permissions to users
-   A group can contain many users, and a user can belong to multiple groups.
*   There’s a limit to the number of groups you can have, and a limit to how many groups a user can be in.
-   Use the principal of least privilege when assigning permissions
-   You cannot nest groups (groups within groups)
-   Members inherit the policies assigned to the group.

**Best practice: Attach IAM policies to IAM groups, rather than to individual IAM users.**

![[Pasted image 20221114160446.png]]

An **IAM group** is a collection of IAM users. Groups let you specify permissions for multiple users, which can make it easier to manage the permissions for those users. For example, you could have a group called _Admins_ and give that group the types of permissions that administrators typically need. Any user in that group automatically has the permissions that are assigned to the group.

![](https://media.tutorialsdojo.com/iam-groups.png)

