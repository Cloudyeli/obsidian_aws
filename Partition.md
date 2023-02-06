Spreads your instances across logical partitions such that groups of instances in one partition **do not share the underlying hardware** with groups of instances in different partitions for the case that if one of these partitions within an [[AZ]] or across [[AZ]]s fails, you still have a group of instances that are in another partition, which should be running.

*   This strategy is typically used by large **distributed and replicated workloads**, such as Hadoop, Cassandra, and Kafka
* Partitions can be in multiple [[AZ]]s (up to 7 per [[AZ]]).

![[Pasted image 20230201123246.png]]