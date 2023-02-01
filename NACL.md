## Network Access Controll List (NACL)

An Network ACL (NACL) is an optional layer of security that acts as a [[firewall]] for controlling traffic in and out of a subnet. You can associate multiple [[subnet]]s with a single network ACL, but a subnet can be associated with only one network ACL at a time.

• Firewall at the subnet level  
• Support allow and deny rules  
• [[Stateless firewall]]
• Process rules in order

NACLs have an explicit deny

![[Pasted image 20221117172728.png]]

NACLs apply only to traffic entering / exiting the subnet

![[Pasted image 20221117172143.png]]
 