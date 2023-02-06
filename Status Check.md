## EC2 Status Check:

##### - [[System Status Check]]
*   Checks that the underlying hardware on which your [[EC2]] instance is running, is working operationally.
*   If there is a problem with a system status check, it means that AWS are going to need to be involved to actually fix that problem.
##### - [[Instance Status Check]]
*   AWS is checking the software networking configuration of your [[EC2]] instance itself.
*   Makes shure that the [[OS]] is configured correctly, so that your [[EC2]] instance is operational and it's communicating with the network
*   If there is a problem with the Instance status check, it means it would need your involvement as an AWS customer to fix that problem.
##### - [[Health Check]]
*   [[EC2]] = EC2 [[Instance status check]]s
*   [[ELB]] = Uses the ELB health checks in addition to EC2 [[Instance status check]]s
**Health check grace period:**
*   How long to wait before checking the health status of the [[EC2]] instance
*   [[Auto Scaling]] does not act on health checks until grace period expires
**[[Target Group]] [[Health check]] with [[NLB]]:**
*   NLB can't route based on [[HTTP]] information, but it can make a connection request to the [[EC2]] instance.