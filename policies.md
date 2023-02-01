IAM Policies are documents that define permissions and can be applied to [[IAM user]]s, [[IAM Group]]s, and [[IAM role]]s.

-   [[Policy document]]s are written in [[JSON]] (key value pair that consists of an attribute and a value)
-   All permissions are implicitly denied by default
-   The most restrictive policy is applied
-   *   The [IAM policy simulator](https://policysim.aws.amazon.com/home/index.jsp?#) is a tool to help you understand, test, and validate the effects of access control policies.
*   The Condition element can be used to apply further conditional logic.

![[Pasted image 20221114160722.png]]

## Types of policies

##### - [[Identity-based policy]]
*   attached to users, groups, or roles 
##### - [[Resource-based policy]]
*   attached to a resource
*   define permissions for a principal accessing the resource
##### - IAM [[permissions boundary]]
*  set the maximum permissions an [[identity-based policy]] can grant an **IAM entity
##### AWS Organizations service control policies ([[SCP]])
*   specify the maximum permissions for [[AWS organizations]] or [[OU]]s
##### - [[Session policy]]
*  used with AssumeRole* API actions

![[Pasted image 20230131164902.png]]

## Determination Rules

1.  By default,all requests are implicitly denied (though the root user has full access)
2.  An explicit allow in an[[ identity-based policy]] or [[resource-based policy]] overrides this default
3.  If a [[permissions boundary]], Organizations [[SCP]], or [[session policy]] is present, it might override the allow with an implicit deny
4.  An explicit deny in any policy overrides any allows

![[Pasted image 20230131142638.png]]

## IAM Policy Structure

![[Pasted image 20230201082343.png]]
![[Pasted image 20230131165346.png]]
`*` is a wildcard
![[Pasted image 20230201082535.png]]
![[Pasted image 20230201082555.png]]
![[Pasted image 20230201082610.png]]
![[Pasted image 20230201082628.png]]
