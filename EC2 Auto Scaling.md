## Amazon [[EC2 Auto Scaling]]

![[Pasted image 20221116160642.png]]

-   Automates scaling of [[EC2]] instances
-   Launches and terminates EC2 instances based on demand (dynamically)
-   Helps to ensure that you have the correct number of EC2 instances available to handle the application load
-   Amazon EC2 Auto Scaling provides **elasticity** and **scalability**
-   You create collections of EC2 instances, called an Auto Scaling group ([[ASG]])

#### Scaling is horizontal ([[scaling out]]), !NOT vertical ([[scaling up]])

### Scaling policies include:  

*   **Target Tracking** – Attempts to keep the group at or close to the metric
-   **Simple Scaling** – Adjust group size based on a metric
-   **Step Scaling** – Adjust group size based on a metric – adjustments vary based on the size of the alarm breach
-   **Scheduled Scaling** – Adjust the group size at a specific time