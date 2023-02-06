## Application Load Balancer (ALB)

Elastic Load Balancing ([[ELB]]) with the Application Load Balancer (ALB) is best suited for load balancing of **HTTP** and **HTTPS** traffic and provides advanced request routing targeted at the delivery of modern application architectures, including **microservices** and **containers**.

*   With ALB, it is a requirement that you enable at least **two or more** [[AZ]]s.
*   Operates at the request level
*   Routes based on the content of the request (layer 7 [[OSI]] model), routing ([[HTTP]]/[[HTTPS]])  
*   Microservices architectures (e.g. Docker containers)
*   [[Lambda]] targets
*   Supports advanced [[routing]]
*   You need a [[security group]]
*   Source IP preservation: x-forwarded-for
*   SSL termination: [[ELB]]

![[Pasted image 20230204121522.png]]

### Supported targets: 

*   [[EC2]] instances
*   IP addresses
*   [[Lambda]] functions
*   Containers ([[ECS]])

## Supports advanced [[routing]]:

##### - path-based routing
*   path in URL can be used to determine where to send the connection
##### - host-based routing
*   checks the domain name to determine where to send the connection
##### - query string parameter-based routing 
*   checks the query strings in the URL to determine where to send the connection
listener rule query string: #url #querystring #routing
`http(s)://DNS?Argument=Variable`
##### - source IP address-based routing
*  routed based of source IP address

![[Pasted image 20230204123929.png]]

## Distribution

*   By default, the load balancer will select targets to distribute connections in a round robin fashion. So it's just going to connect to one instance, then the next one. And it will attempt to make the distribution even in that manner.
*   You can also choose least **outstanding requests**, and it will actually see how many requests are outstanding for a load balancer.
*   `ALBRequestCountPerTarget` Metric: The number of requests that are outstanding for an individual target. So that gives you an idea of how many connections are happening on each instance, and that helps you to spread the load that way. #cli #alb

## [[SSL]]/[[TLS]] Termination

![[Pasted image 20230204134149.png]]

## Elastically Scale the Application

*   A [[Launch Template]] specifies the EC2 instance configuration
* . The Application Load Balancer distributes connections between targets ([[EC2]] instances)
*   [[CloudWatch]] receives metrics from ALB and notifies [[Auto Scaling]] if thresholds are breached

![[Pasted image 20221117093518.png]]
