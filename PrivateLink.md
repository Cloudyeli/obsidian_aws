## AWS PrivateLink

AWS PrivateLink provides private connectivity between virtual private clouds ([[VPC]]s), supported AWS services, and your on-premises networks without exposing your traffic to the public internet. Interface VPC endpoints, powered by PrivateLink, connect you to services hosted by AWS Partners and supported solutions available in AWS Marketplace.
With PrivateLink you dont need anymore an internet gateway or a public IP address. 
AWS Private Link also works with AWS [[Direct Connect]]. 

![AWS PrivateLink provides private connectivity between virtual private clouds (VPCs), supported AWS services, and your on-premises networks without exposing your traffic to the public internet. Interface VPC endpoints, powered by AWS PrivateLink, connect you to services hosted by AWS Partners and supported solutions available in the AWS Marketplace.](https://d1.awsstatic.com/products/privatelink/product-page-diagram_AWS-PrivateLink.fc899b8ebd46fa0b3537d9be5b2e82de328c63b8.png)

Unlike [[Direct Connect]], PrivateLink is used as a networking construct _inside_ AWS to privately expose a service/application residing in one VPC (that of a service provider) to other consumer VPCs within an AWS Region.

### **Benefits of AWS PrivateLink**  
  

True to its name, PrivateLink can be considered the most private AWS connectivity method. Thanks to this feature, it boasts a number of benefits:

-   **Secure traffic:**
Network traffic using PrivateLink never traverses the public internet to reduce exposure to a range of cybersecurity threats. The ability to use private IP connectivity also ensures your services function as though they were hosted directly on your private network. Plus, you can associate [[security group]]s and attach an [[endpoint policy]] to interface endpoints to give you precise control over who can access specified services.

-   **Simplified network management:** 
You can connect services across different accounts and Amazon [[VPC]]s with no need for [[firewall]] rules, path definitions, [[route table]]s, or configuration of an [[internet gateway]], [[VPC peering]] connection, or VPC [[CIDR]] management.

-   **Accelerated cloud migration:** 
With your data protected from the internet, you can more easily migrate traditional on-prem applications to [[SaaS]] offerings hosted in the cloud with PrivateLink, with the confidence that your traffic will remain secure.

-   **Automation capability:** 
By using a [[Terraform]] Provider supporting [[SaaS]], such as the one from [Databricks](https://docs.databricks.com/dev-tools/terraform/index.html), you can automate your infrastructure and configuration management to deploy an even more easy-to-manage, intuitive PrivateLink workspace.  

![[Pasted image 20221118083253.png]]