## [Benefits of AWS](https://aws.amazon.com/about-aws/global-infrastructure/)

1. Security
2. Availability
3. Performance
4. Scalability
5. Flexibility
6. Global Footprint

### An AWS Region is a physical location in the world where AWS have multiple AZs.

AZs consist of one or more discrete data centers, each with redundant power, networking, and connectivity, housed in separate facilities.

Each region is completely independent. Each Availability Zone is isolated, but the Availability Zones in a region are connected through low-latency links.

AWS are constantly expanding around the world and currently there are (May no longer be up to date):

![Text Description automatically generated with low confidence](https://digitalcloud.training/wp-content/uploads/2022/02/text-description-automatically-generated-with-low.png)An AWS Region is a physical location in the world where AWS have multiple AZs.

The AWS Global Infrastructure is made up of:

## AWS [[Region]]s  

* A region is a geographical area  
* Each region consists of 2 or more availability zones
* Isolated from other AWS Regions

## Availability Zones  ([[AZ]]s)

* Availability Zones are physically separate and isolated from each other  
* AZs span one or more data centers  
* Each AZ is designed as an independent failure zone

## [[Local Zone]]s  

* AWS Local Zones place compute, storage, database and other select AWS services closer to end-users
* Extension of an AWS Region where you can run your latency sensitive applications

![[Pasted image 20221114120153.png]]

## AWS [[Wavelength]] Zones

* AWS Wavelength enables developers to build applications that deliver single-digit millisecond latencies to mobile devices and end-users.
* AWS developers can deploy their applications to Wavelength Zones, AWS infrastructure deployments that embed AWS compute and storage services within the telecommunications providers’ datacenters at the edge of the 5G networks, and seamlessly access the breadth of AWS services in the region.
* AWS Wavelength brings AWS services to the edge of the 5G network, minimizing the latency to connect to an application from a mobile device.

## AWS [[Outposts]]

* AWS Outposts bring native AWS services, infrastructure, and operating models to virtually any data center, co-location space, or on-premises facility.
* You can use the same AWS APIs, tools, and infrastructure across on-premises and the AWS cloud to deliver a truly consistent hybrid experience.
* AWS Outposts is designed for connected environments and can be used to support workloads that need to remain on-premises due to low latency or local data processing needs.

## [[Edge Locations and Regional Edge Caches ]] 

* Edge locations are Content Delivery Network ([[CDN]]) [[endpoint]]s for CloudFront
- There are many more edge locations than regions
- Regional Edge Caches sit between your [[CloudFront]] Origin servers and the Edge Locations
- A Regional Edge Cache has a larger cache-width than each of the individual Edge Locations



