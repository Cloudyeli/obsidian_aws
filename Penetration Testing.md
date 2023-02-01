Penetration testing is the practice of testing one’s own application’s security for vulnerabilities by simulating an attack

-   AWS allows penetration testing without prior approval for 8 AWS services

## Permitted services

-   Amazon [[EC2]] instances
-   [[NAT Gateway]]s, and Elastic Load Balancers ([[ELB]])
-   Amazon [[RDS]]
-   Amazon [[CloudFront]]
-   Amazon [[Aurora]]
-   Amazon [[API Gateway]]s
-   AWS [[Lambda]] and Lambda Edge functions
-   Amazon [[Lightsail]] resources
-   Amazon Elastic [[Beanstalk]] environments

## Prohibited Activities

-   [[DNS]] zone walking via Amazon [[Route 53]] Hosted Zones
-   Denial of Service ([[DoS]]), Distributed Denial of Service ([[DDoS]]) Simulated DoS, Simulated DDoS Port flooding
-   Protocol flooding
-   Request flooding (login request flooding, [[API]] request flooding)