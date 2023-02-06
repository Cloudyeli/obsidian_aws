##### - [[Target Tracking]]
*   Attempts to keep the group at or close to the metric
##### - [[Simple Scaling]]
*   Adjust group size based on a metric
##### - [[Step Scaling]]
*   Adjust group size based on a metric – adjustments vary based on the size of the alarm breach
##### - [[Scheduled Scaling]]
*   Adjust the group size at a specific time

## Additional Scaling Settings:

##### - [[Cooldown]]s
*   Used with [[simple scaling]] policy to prevent Auto Scaling from launching or terminating before effects of previous activities are visible. 
*   Default value is 300 seconds (5 minutes)
##### - [[Termination Policy]]
*   Controls which instances to terminate first when a scale-in event occurs
##### - [[Termination Protection]]
*   Prevents Auto Scaling from terminating protected instances
##### - [[Standby State]]
*   Used to put an instance in the `InService` state into the `Standby` state, to update or troubleshoot the instance
##### - [[Lifecycle Hook]]s
*   Used to perform custom actions by pausing instances as the ASG launches or terminates them.
Use case:
*   Run a script to download and install software after launching
*   Pause an instance to process data before a scale-in (termination)