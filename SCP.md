## Service Control Policies (SCP)s are a feature of [[AWS Organizations]].

An SCP control the maximum available permissions within an AWS account, so it's a security control that you can apply to your member accounts, as well as your root account to a certain extent within your organisation.

-   SCPs do not grant permissions
-   Manage the maximum available permissions
-   Must have **all features** enabled in [[AWS Organizations]]
-   Can be applied to accounts or [[OU]]s
-   Policies can be assigned at different points in the hierarchy
-   SCPs affect only [[IAM user]]s and [[IAM role]]s – not [[resource-based policy\|resources-based policies]]
-   SCPs affect the **root account** in **member accounts**
-   Users in the **management account** are not restricted - so SCPs do not affect any action performed by the **management account**

==**NOTE: SCPs do not grant ANY permissions, they control the AVAILABLE permissions**==

##### - Deny list strategy:

-   Uses the `FullAWSAccess` SCP
-   Attached to every **[[OU]]** and **account**
-   Overrides the **implicit deny**
-   Explicitly allows all permissions to flow down from the root
-   Create additional SCPs to explicitly deny permissions

##### - Allow list strategy:

-   `FullAWSAccess` SCP is **removed**
-   No [[API]]s are permitted anywhere unless you explicitly allow them
-   Create SCPs to allow permissions
-   SCPs must be **attached** to target account and every [[OU]] above it **including root**

#### SCPs can be applied to:

*   An individual member account
or
*   An organizational unit ([[OU]])
* 
![[Pasted image 20230204141923.png]]

## Preventive [[Guardrails]]

-  [[Control Tower]] creates a series of **preventive [[guardrails]]**. These are essentially service control policies (SCP), that will disallow certain [[API]] actions. Now you can think of this as similar to [[managed policy\|managed policies]] with [[IAM]]. Essentially [[Control Tower]] is creating a series of managed SCPs for you, that are preconfigured a certain way for a certain purpose. 