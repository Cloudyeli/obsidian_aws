
AWS Organizations allows you to consolidate multiple AWS accounts into an organisation that you create and centrally manage

### Available in two feature sets:

##### - Consolidated Billing
-   **Paying Account** – independent and cannot access resources of other accounts.
-   **Linked Accounts** – all linked accounts are independent.

-   Single payment method for all the AWS accounts in the Organization
-   Combined view of charges incurred by all your accounts
-   Pricing benefits from aggregated usage
-   Limit of 20 linked accounts for consolidated billing (default)
-   Can help with cost control through volume discounts
-   Unused reserved [[EC2]] instances are applied across the group
-   **Paying accounts** should be used for billing purposes only

##### - All features
*   Includes **root accounts** and **organisational units ([[OU]])**.
*   Use service control policies ([[SCP]])s to centrally control permissions for the accounts in your organisation.
*   Policies are applied to root accounts or [[OU]]s.
*   All features and gives you some additional capabilities, including Service Control Policies ([[SCP]]) and [[tag policy\|tag policies]].

## AWS Organizations - Migration

-   Accounts can be migrated between AWS Organizations
-   You must have root or [[IAM]] access to both the **member** and **management accounts**
-   Use the AWS Organizations console for just a few accounts
-   Use the AWS Organizations [[API]] or AWS [[CLI]] if there are many accounts to migrate

## Account Configurations

*   Use the AWS Management Console to create an Organization
*   Create a Service Control Policy ([[SCP]]) and attach to [[OU]]
*   Role can be assumed by any user with the `sts:AssumeRole` permissions
*   `OrganizationAccountAccessRole` Role has **full permissions** in the account

![[Pasted image 20230204141635.png]]

## AWS Organizations has four main benefits: 

1) Centrally manage access polices across multiple AWS accounts. 
2) Automate AWS account creation and management. 
3) Control access to AWS services with [[SCP]]
4) Enable consolidated billing across multiple AWS accounts 

Analysing cost is done through the [[Cost Explorer]] (or TCO calculator), which is not part of AWS Organizations.

![[Pasted image 20230204140546.png]]

