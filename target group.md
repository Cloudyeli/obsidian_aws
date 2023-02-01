# **What is a target group?**

A **target group** contains [[EC2]] instances to which a **load balancer** ([[ELB]]) distributes workload.

A load balancer paired with a target group does NOT yet have [[auto scaling]] capability.

### **What is an Auto Scaling Group ([[ASG]])?**

This is where auto scaling comes in. An **auto scaling group** ([[ASG]]) can be attached to a **load balancer ([[ELB]]).**

We can attach auto scaling rules ([[scaling policy]]) to an [[ASG]]. Then, when thresholds are met (e.g. CPU utilization), the number of instances will be adjusted programatically.

### How to attach an ASG to a load balancer?

For Application load balancer ([[ALB]]), link [[ASG]] with the **target group** (which itself is attached to the load balancer ([[ELB]]))