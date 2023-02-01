## AWS Systems Manager

AWS Systems Manager is the operations hub for your AWS applications and resources and a secure end-to-end management solution for hybrid cloud environments that enables safe and secure operations at scale.

-   Manages many AWS resources including Amazon [[EC2]], Amazon [[S3]], Amazon [[RDS]] etc.

### AWS Systems Manager is the operations hub for your AWS applications and resources, and is broken into four core feature groups:

### Operations Management

##### AWS [[Explorer]]
##### AWS [[OpsCenter]] 
##### AWS [[Incident Manager]] 
##### AWS [[CloudWatch Dashboard]]

### Application Management

##### AWS [[Application Manager]]
##### AWS [[AppConfig]]
##### AWS [[Parameter Store]]
-   store secrets and configuration data securely and hyrarchical


### Change Management

##### AWS [[Automation]]
-   uses [[SSM]] documents to run automations
##### AWS [[Change Manager]]
##### AWS [[Maintenance Windows]]
##### AWS [[Change Calendar]]

### Node Management

##### AWS [[Fleet Manager]]
##### AWS [[Session Manager]]
*   Secure remote management of your instances at scale without logging into your servers
-   connect securely without [[bastion host]]s, [[SSH]], [[RDP]] or remote PowerShell 
##### AWS [[Patch Manager]]
-   manage patching schedules and installation
-   Deploy operating system and software patches automatically across large groups of Amazon [[EC2]] or on- premises instances
##### AWS [[State Manager]]
##### AWS [[Compliance]]
*   Scan managed instances for patch compliance and configuration inconsistencies
##### AWS [[Inventory]]
-   gather inventory information
##### AWS [[Run Command]]
-   run commands on EC2 instances
##### AWS [[Distributor]]

## AWS Systems Manager Agent ([[SSM]] Agent) 

AWS Systems Manager Agent (SSM Agent) is Amazon software that runs on Amazon Elastic Compute Cloud ([[EC2]]) instances, edge devices, and on-premises servers and virtual machines (VMs). SSM Agent makes it possible for [[Systems Manager]] to update, manage, and configure these resources.

## Systems Manager Document ([[SSM]] Document)

A Systems Manager document (SSM document) defines the actions that Systems Manager performs. SSM document types include _Command_ documents, which are used by [[State Manager]] and [[Run Command]], and [[Automation]] runbooks, which are used by Systems Manager [[Automation]]. Systems Manager includes dozens of pre-configured documents that you can use by specifying parameters at runtime. Documents can be expressed in [[JSON]] or [[YAML]], and include steps and parameters that you specify.

![[Pasted image 20221119154224.png]]

## How Systems Manager works

The following diagram describes how some Systems Manager capabilities perform actions on your resources. The diagram doesn't cover all capabilities. Each enumerated interaction is described after the diagram.

![[Pasted image 20221119153117.png]]
**Diagram 1: General example of Systems Manager process flow**

1.  **Access Systems Manager** – Use one of the available options for accessing Systems Manager.
    
2.  **Choose a Systems Manager capability** – Determine which capability can help you perform the action you want to perform on your resources. The diagram shows only a few of the capabilities that IT administrators and DevOps personnel use to manage their applications and resources.
    
3.  **Verification and processing** – Systems Manager verifies that your AWS Identity and Access Management (IAM) user, group, or role has permission to perform the action you specified. If the target of your action is a managed node, the Systems Manager Agent ([[SSM]] Agent) running on the node performs the action. For other types of resources, Systems Manager performs the specified action or communicates with other AWS services to perform the action on behalf of Systems Manager.
    
4.  **Reporting** – Systems Manager, [[SSM]] Agent, and other AWS services that performed an action on behalf of Systems Manager report status. Systems Manager can send status details to other AWS services, if configured.
    
5.  **Systems Manager operations management capabilities** – If enabled, Systems Manager operations management capabilities such as Explorer, OpsCenter, and Incident Manager aggregate operations data or create artifacts in response to events or errors with your resources. These artifacts include operational work items (OpsItems) and incidents. Systems Manager operations management capabilities provide operational insight into your applications and resources and automated remediation solutions to help troubleshoot problems.

