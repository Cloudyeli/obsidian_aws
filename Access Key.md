Access Keys are some secret information that is stored on the file system of the instance. The access keys are associated with an IAM account and the user account has a policy.

*   A combination of an **access key ID** and a **secret access key.**
*   AWS CLI configured with access keys
*   The access key will use permissions assigned to the IAM user
*   Access Keys are configured and saved on the on the file system of the server ==! Not very secure
*   better to use a [[instance profile]] if you want to grant an [[EC2]] instance access to other services ([[IAM roles for EC2 Instances]])
   
![[Pasted image 20221116122308.png]]

IAM roles for EC2 Instances
-   You can assign two active access keys to a user at a time.
-   These can be used to make programmatic calls to AWS when using the **[[API]]** in program code or at a command prompt when using the **AWS [[CLI]]** or the **[[AWS PowerShell tools]]**.
-   You can create, modify, view, or rotate access keys.
-   When created [[IAM]] returns the access key ID and secret access key.
-   The secret access is returned only at creation time and if lost a new key must be created.
-   Ensure access keys and secret access keys are stored securely.
-   Users can be given access to change their own keys through [[IAM policy]] (not from the console).
-   You can disable a user’s access key which prevents it from being used for API calls.