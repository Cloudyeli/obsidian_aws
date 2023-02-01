## AWS Health Aware (AHA)

AWS Health Aware – AHA is an incident management & communication framework to ingest proactive and real-time alerts from AWS Health to a customer’s preferred communication channels. Customers using AWS Organizations can get aggregated active account level alerts from impacted accounts across their organization. Alerts can be configured to endpoint(s) such as Slack, Microsoft Teams, Amazon [[Chime]] and Email Alerts. AHA can also be integrated with a broad range of other endpoints during configuration. These alerts are targeted to give customers event visibility and guidance to help quickly diagnose and resolve issues that are impacting our customer’s applications or workloads.

## **Benefits of AHA**

AHA uses the [AWS Health API](https://docs.aws.amazon.com/health/latest/ug/health-api.html) which is only available to AWS customers who have Business or [Enterprise Support](https://aws.amazon.com/premiumsupport/plans/enterprise/) plan.

These customers can take advantage of the following features:

1.  Integration with communication platforms such as Slack, Amazon Chime, Microsoft Teams and Email for automated and real time alerts of the AWS incidents.
2.  Integration with Amazon EventBridge, with capability to ingest both Organizational and Non-organizational alerts to an event bus. This help customers integrate with more than 35 SaaS partners such as NewRelic/DataDog/PagerDuty etc.
3.  Aggregated [[PHD]] alerts with prescriptive guidance provided by AWS Health.
4.  Visibility into the AWS accounts and resources that are impacted for [[PHD]] alerts.
5.  Ability to filter out unwanted alerts by selecting specific [[region]](s).