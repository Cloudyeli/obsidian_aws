Ordinarily, in most servers, if you have a public IP address, it will be configured and you would be able to see it if you query it like with `ip addr show eth0`. 
But on an EC2 instance you only see the private IP Adress, because the public IP doesn't exist anywhere on the EC2 instance. The reason is, that the Public IP address is actually associated to the [[network interfaces\|network interface]]. Your Instance doesn't know about that. That actually takes place externally to the instance and it's performed by the [[internet gateway]].
The internet Gateway performance network address translation (one to one [[NAT]]).
That means, that when packet goes out from your instance, it has a source address of the private IP destination of whatever the addresses on the internet.
The [[NAT gateway]] will then change the source address to be the public or elastic IP ([[EIP]]).
And then when the return traffic comes back, it's destined to the public address and the [[internet gateway]] will translate that to the private address.

![[Pasted image 20230201181031.png]]
