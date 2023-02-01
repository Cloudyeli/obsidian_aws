## AWS service quotas

[PDF](https://docs.aws.amazon.com/pdfs/general/latest/gr/aws-general.pdf#aws_service_limits)

Your AWS account has default quotas, formerly referred to as limits, for each AWS service. Unless otherwise noted, each quota is Region-specific. You can request increases for some quotas, and other quotas cannot be increased.

Service Quotas is an AWS service that helps you manage your quotas for many AWS services, from one location. Along with looking up the quota values, you can also request a quota increase from the Service Quotas console.

AWS Support might approve, deny, or partially approve your requests.

**To view service quotas**

You can view service quotas using the following options:

-   Open the [Service endpoints and quotas](https://docs.aws.amazon.com/general/latest/gr/aws-service-information.html) page in the documentation, search for the service name, and click the link to go to the page for that service. To view the service quotas for all AWS services in the documentation without switching pages, view the information in the [Service Endpoints and Quotas](https://docs.aws.amazon.com/general/latest/gr/aws-general.pdf#aws-service-information) page in the PDF instead.
    
-   Open the [Service Quotas console](https://console.aws.amazon.com/servicequotas/home). In the navigation pane, choose **AWS services** and select a service.
    
-   Use the [list-service-quotas](https://docs.aws.amazon.com/cli/latest/reference/service-quotas/list-service-quotas.html) and [list-aws-default-service-quotas](https://docs.aws.amazon.com/cli/latest/reference/service-quotas/list-aws-default-service-quotas.html) AWS CLI commands.
    

**To request a quota increase**

You can request a quota increase using Service Quotas and AWS Support Center. If a service is not yet available in Service Quotas, use AWS Support Center instead. Increases are not granted immediately. It might take a couple of days for your increase to become effective.

-   (Recommended) Open the [Service Quotas console](https://console.aws.amazon.com/servicequotas/home). In the navigation pane, choose **AWS services**. Select a service, select a quota, and follow the directions to request a quota increase. For more information, see [Requesting a Quota Increase](https://docs.aws.amazon.com/servicequotas/latest/userguide/request-quota-increase.html) in the _Service Quotas User Guide_.
    
-   Use the [request-service-quota-increase](https://docs.aws.amazon.com/cli/latest/reference/service-quotas/request-service-quota-increase.html) AWS CLI command.
    
-   Open the [AWS Support Center](https://console.aws.amazon.com/support/home#/) page, sign in if necessary, and choose **Create case**. Choose **Service limit increase**. Complete and submit the form.