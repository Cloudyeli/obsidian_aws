## AWS Batch

AWS Batch enables developers, scientists, and engineers to run hundreds of thousands of batch computing jobs ([[batch job]]s) easily and efficiently on AWS.

![[Pasted image 20221116122509.png]]


AWS Batch dynamically provisions the optimal quantity and type of compute resources (e.g., CPU or memory optimized instances) based on the volume and specific resource requirements of the batch jobs submitted.

With AWS Batch, you simply package the code for your batch jobs, specify their dependencies, and submit your batch job using the AWS Management Console, [[CLI]]s, or [[SDK]]s.

AWS Batch allows you to specify execution parameters and job dependencies, and facilitates integration with a broad range of popular batch computing workflow engines and languages (e.g., Pegasus WMS, Luigi, and AWS [[Step Functions]]).

AWS Batch efficiently and dynamically provisions and scales [[EC2]] and [[Spot Instance]]s based on the requirements of your jobs. AWS Batch provides default job queues and compute environment definitions that enable you to get started quickly.