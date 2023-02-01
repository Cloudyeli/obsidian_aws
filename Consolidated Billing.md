You can use the consolidated billing feature in [[AWS Organizations]] to consolidate billing and payment for multiple AWS accounts or multiple Amazon Internet Services Pvt. Ltd ([[AISPL]]) accounts. Every organization in AWS Organizations has a **management account** that pays the charges of all the **member accounts**.

Consolidated billing includes:

- ##### Management Account (Paying Account) 
Independent and cannot access resources of other accounts.

- ##### Member Accounts (Linked Accounts)
All linked accounts are independent.

### Consolidated billing has the following benefits:

-   **One bill** – You get one bill for multiple accounts.
    
-   **Easy tracking** – You can track the charges across multiple accounts and download the combined cost and usage data.
    
-   **Combined usage** – You can combine the usage across all accounts in the organization to share the volume pricing discounts, Reserved Instance ([[RI]]) discounts, and Saving Plans. This can result in a lower charge for your project, department, or company than with individual standalone accounts. 
    
-   **No extra fee** – Consolidated billing is offered at no additional cost.
    

### Note:

The member account bills are for informational purpose only. The management account might reallocate the additional volume discounts, Reserved Instance, or Savings Plans discounts that your account receives.

If you have access to the management account, you can see a combined view of the AWS charges that the member accounts incur. You also can get a cost report for each member account.

AWS and AISPL accounts can't be consolidated together. If your contact address is in India, you can use AWS Organizations to consolidate AISPL accounts within your organization.

### Important

When a member account leaves an organization, the member account can no longer access Cost Explorer data that was generated when the account was in the organization. The data isn't deleted, and the management account in the organization can still access the data. If the member account rejoins the organization, the member account can access the data again.