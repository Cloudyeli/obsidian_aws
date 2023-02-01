## AWS ElastiCache

Amazon ElastiCache is a fully managed, in-memory caching service supporting flexible, real-time use cases. You can use ElastiCache for [caching](https://aws.amazon.com/caching/), which accelerates application and [[database]] performance, or as a primary data store for use cases that don't require durability like session stores, gaming leaderboards, streaming, and analytics. ElastiCache is compatible with [[Redis]] and [[Memcached]].

-   Fully managed implementations [[Redis]] and [[Memcached]]
-   ElastiCache is a **key/value** store
-   In-memory database offering high performance and low latency
-   Can be put in front of [[database]]s such as [[RDS]] and [[DynamoDB]]
-   ElastiCache nodes run on Amazon [[EC2]] instances, so you must choose an instance family/type

![[Pasted image 20221119110242.png]]

### Use Cases and Benefits

* ##### Web session store 
In cases with load-balanced ([[ELB]]) web servers, store web session information in Redis so if a server is lost, the session info is not lost, and another web server can pick it up

* ##### Database caching 
Use [[Memcached]] in front of AWS [[RDS]] to cache popular queries to offload work from RDS and return results faster to users

* ##### Leaderboards 
Use [[Redis]] to provide a live leaderboard for millions of users of your mobile app

* ##### Streaming data dashboards 
Provide a landing spot for streaming sensor data on the factory floor, providing live real-time dashboard displays


![[Pasted image 20230120121905.png]]
