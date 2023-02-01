Amazon Route 53 is a highly available and scalable Domain Name System ([[DNS]]) web service. Route 53 connects user requests to internet applications running on AWS or on-premises.

![[Pasted image 20221116154210.png]]

*   Route 53 is the AWS Domain Name Service

### Route 53 performs three main functions:

- ##### Domain registration
Route 53 allows you to register domain names

- ##### Domain Name Service ([[DNS]])
Route 53 translates name to IP addresses using a global network of authoritative DNS servers

- ##### Health checking
Route 53 sends automated requests to your application to verify that it’s reachable, available and functional

The name for the AWS Service Route 53 comes from the fact that **[[DNS]] servers respond to queries on [[port]] 53 and provide answers that route end users to your applications on the Internet**.

### Amazon Route 53 Routing Policies

*   **Simple** – IP address associated with name
*   **Failover** – if primary is down, route to secondary
*   **Geolocation** – route based on geographic location of request
*   **Geoproximity** – route to closes [[Region]] withing geo area 
*   **Latency** – use lowest latency route to resources  
*   **Multivalue answer** – returns several IP addresses  
*   **Weighted** – relative weights (e.g. 80%/20%)

![[Pasted image 20221116154925.png]]

A hosted zone represents a set of records belonging to a domain

![[Pasted image 20221116155356.png]]