[[IAM role]]s can be used for granting applications running on EC2 instances permissions to AWS [[API]] requests using [[instance profile]]s.

-   Only one [[IAM role]] can be assigned to an [[EC2]] instance at a time.
-   The [[IAM role]] is assumed by the [[EC2]] instance.
-   The [[EC2]] instance will gain acces to whatever permission the [[IAM role]] provides.
-   So no credentials are stored on the [[EC2]] instance.
-   A role can be assigned at the [[EC2]] instance creation time or at any time afterwards.
-   When using the AWS [[CLI]] or [[API]] [[instance profile]]s must be created manually (it’s automatic and transparent through the console).
-   Applications retrieve [[temporary security credentials]] from the instance [[metadata]].

![[Pasted image 20221116122425.png]]