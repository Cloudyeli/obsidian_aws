## Amazon LightSail Instances

Amazon Lightsail is designed to be the easiest way to launch and manage a virtual private server with AWS. Lightsail plans include everything you need to jumpstart your project – a virtual machine, SSD-based storage, data transfer, [[DNS]] management, and a static IP address – for a low, predictable price.

Amazon LightSail is great for users who do not have deep AWS technical expertise as it makes it very easy to provision compute services.

![[Pasted image 20221116124525.png]]

Amazon LightSail provides developers compute, storage, and networking capacity and capabilities to deploy and manage websites, web applications, and databases in the cloud.

Amazon LightSail includes everything you need to launch your project quickly – a virtual machine ([[VM]]), SSD-based storage, data transfer, [[DNS]] management, and a static IP.

Amazon LightSail provides preconfigured virtual private servers ([[EC2]] instances) that include everything required to deploy an application or create a database.

* The underlying infrastructure and operating system is managed by Amazon LightSail.
* Best suited to projects that require a few dozen instances or fewer.
* Provides a simple management interface.
* Good for blogs, websites, web applications, e-commerce etc.
* Can deploy load balancers and attach [[block storage]].
* Public [[API]].
* Can connect to each other and other AWS resources through public Internet and private ([[VPC peering]]) networking.
* Application templates include WordPress, WordPress Multisite, Drupal, Joomla!, Magento, Redmine, LAMP, Nginx (LEMP), MEAN, Node.js, and more.

Amazon LightSail currently supports 6 Linux or Unix-like distributions: Amazon Linux, CentOS, Debian, FreeBSD, OpenSUSE, and Ubuntu, as well as 2 Windows Server versions: 2012 R2 and 2016.

### Limitations:

Limited to 20 Amazon LightSail instances, 5 static IPs, 3 [[DNS]] zones, 20 TB [[block storage]], 40 databases, and 5 load balancers ([[ELB]]) per account.

Up to 20 certificates per calendar year.

## Amazon LightSail Databases

Amazon LightSail databases are instances that are dedicated to running databases.

An Amazon LightSail database can contain multiple user-created databases, and you can access it by using the same tools and applications that you use with a stand-alone database.

* Amazon LightSail managed databases provide an easy, low maintenance way to store your data in the cloud.
* Amazon LightSail manages a range of maintenance activities and security for your database and its underlying infrastructure.
* Amazon LightSail automatically backs up your database and allows point in time restore from the past 7 days using the database restore tool.
* Amazon LightSail databases support the latest major versions of [[MySQL]]. Currently, these versions are 5.6, 5.7, and 8.0 for MySQL.

### LightSail Database [[Pricing]]

Amazon LightSail databases are available in Standard and High Availability plans.

Amazon LightSail is very affordable.

* High Availability plans add redundancy and durability to your database, by automatically creating standby database in a separate Availability Zone.
* Amazon LightSail plans are billed on an on-demand hourly rate, so you pay only for what you use.

For every Amazon LightSail plan you use, AWS charges you the fixed hourly price, up to the maximum monthly plan cost.
