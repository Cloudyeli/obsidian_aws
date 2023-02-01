Identity-based policies are attached to[[ IAM User]]s, [[IAM Group]]s or [[IAM Role]]s.

There are are a view ways that you can attach  an identidy based policie:

##### [[Inline-policy]]
*   have a one o one relationship with the user, role or group; 
*   you create a specic inline policie for the role, so you can't share them accross other roles. 
*   If you delete the user, you delete the policie along with it.
* 
##### [[Managed policy]]
*   Ether AWS managed or customer managed. 
*   AWS managed are created and managed by AWS. You can't modify thise policies, but you can use them in your account.
*   Customer managed are created and managed by you. 
*   Managed policies are standalone policies that can be attached to multiple users, groups, or roles

![[Pasted image 20230131141842.png]]