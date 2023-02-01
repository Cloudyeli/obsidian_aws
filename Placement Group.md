EC2 Placement Groups are a way to control how AWS deploys your EC2 instances and places them within your [[AZ]]s or across your [[AZ]]s.

##### -[[Cluster]]
A Cluster Placement Group packs instances **phisical** close together inside an [[AZ]] (in same rack or in adjacent racks).
*  Uses enhanced networking, low network latency and high throughput for inter- instance traffic.
*   This strategy enables workloads to achieve the **low-latency** network performance necessary for **tightly-coupled** node-to-node communication that is typical of **[[HPC]] applications**.

##### - [[Partition]]
Spreads your instances across logical partitions such that groups of instances in one partition **do not share the underlying hardware** with groups of instances in different partitions.
*   This strategy is typically used by large **distributed and replicated workloads**, such as Hadoop, Cassandra, and Kafka
* Partitions can be in multiple AZs (up to 7 per AZ).

##### - [[Spread]]
Strictly places a small group of EC2 instances across **distinct underlying hardware** to reduce correlated failures.
*   Each instance is located in a separate AWS rack
*   Can be within an [[AZ]] or across [[AZ]]s.

![[Pasted image 20230201124004.png]]