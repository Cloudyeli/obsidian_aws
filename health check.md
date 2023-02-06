*   [[EC2]] = EC2 [[Instance status check]]s
*   [[ELB]] = Uses the ELB health checks in addition to EC2 [[Instance status check]]s

**Health check grace period:**
*   How long to wait before checking the health status of the [[EC2]] instance
*   [[Auto Scaling]] does not act on health checks until grace period expires

**[[Target Group]] Health check with [[NLB]]:**
*   NLB can't route based on [[HTTP]] information, but it can make a connection request to the [[EC2]] instance.