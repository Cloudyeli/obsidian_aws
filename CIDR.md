CIDR (Classless Inter-Domain Routing) -- also known as _supernetting_ -- is a method of assigning Internet Protocol (IP)  addresses that improves the efficiency of address distribution and replaces the previous system based on Class A, Class B and Class C networks. 

A CIDR address looks like a normal IP address, except that it ends with a slash followed by a number. The number after the slash represents the number of addresses in the range.

Here’s an example CIDR IP address in IPv4:

```
192.0.2.0/24
```

Because IPv4 has a 32-bit address space, the 24-bit prefix in the preceding example means that the address range is the 8 bits (256 addresses) after 192.0.2.0.

And here’s an example in IPv6:

```
2001:db8::/32
```

IPv6 has a 128-bit address range, so the 32-bit network prefix refers to 96 bits worth of addresses following 2001:db8::, about 76 octillion addresses.