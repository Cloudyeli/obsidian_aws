AWS Step Functions is a [[serverless]] orchestration service that lets you integrate with [[Lambda]] functions and other AWS services to build business-critical applications.

![[Pasted image 20221117154428.png]]

AWS Step Functions makes it easy to coordinate the components of distributed applications as a series of steps in a visual workflow

*   Step Functions is based on state machines and tasks. 
*   A state machine is a workflow. 
*   A task is a state in a workflow that represents a single unit of work that another AWS service performs. 
*   Each step in a workflow is a state.

You can quickly build and run state machines to execute the steps of your application in a reliable and scalable fashion

Through Step Functions' graphical console, you see your application’s workflow as a series of [[event-driven]] steps.

![Diagram shows the workflow for a store checkout process using AWS Step Functions. AWS Lambda functions are invoked for each step of the process.](https://d1.awsstatic.com/video-thumbs/Step-Functions/AWS_Step_Functions_HIW.bc3d2930f00dd0401269367b8e8617a7dba5915c.png)

With Step Functions' built-in controls, you examine the state of each step in your workflow to make sure that your application runs in order and as expected. 

*   Depending on your use case, you can have Step Functions call AWS services, such as [[Lambda]], to perform tasks. 
*   You can create workflows that process and publish machine learning ([[ML]]) models. 
*   You can have Step Functions control AWS services, such as AWS [[Glue]] to create extract, transform, and load ([[ETL]]) workflows. 
*   You also can create long-running, automated workflows for applications that require human interaction.