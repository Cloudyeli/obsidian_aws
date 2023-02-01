# Amazon SQS FIFO (First-In-First-Out) queues

[PDF](https://docs.aws.amazon.com/pdfs/AWSSimpleQueueService/latest/SQSDeveloperGuide/sqs-dg.pdf#FIFO-queues)[RSS](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/recent-updates.rss)

_FIFO (First-In-First-Out)_ queues have all the capabilities of the [standard queues](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/standard-queues.html), but are designed to enhance messaging between applications when the order of operations and events is critical, or where duplicates can't be tolerated.

Examples of situations where you might use FIFO queues include the following:

-   E-commerce order management system where order is critical
    
-   Integrating with a third-party systems where events need to be processed in order
    
-   Processing user-entered inputs in the order entered
    
-   Communications and networking – Sending and receiving data and information in the same order
    
-   Computer systems – Making sure that user-entered commands are run in the right order
    
-   Educational institutes – Preventing a student from enrolling in a course before registering for an account
    
-   Online ticketing system – Where tickets are distributed on a first come first serve basis