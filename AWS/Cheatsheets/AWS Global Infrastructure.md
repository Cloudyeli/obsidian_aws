## [Benefits of AWS](https://aws.amazon.com/about-aws/global-infrastructure/)

1. Security
2. Availability
3. Performance
4. Scalability
5. Flexibility
6. Global Footprint

## An AWS [[Region]] is a physical location in the world where AWS have multiple [[AZ]]s.

*  An AWS [[Region]] is a physical location in the world where AWS have multiple [[AZ]]s.
*   [[AZ]]s consist of one or more discrete data centers, each with redundant power, networking, and connectivity, housed in separate facilities.
*   Each [[region]] is completely independent. Each Availability Zone ([[AZ]]) is isolated, but the [[AZ]]s in a [[region]] are connected through low-latency links.

AWS are constantly expanding around the world and currently there are (May no longer be up to date):

![Text Description automatically generated with low confidence](https://digitalcloud.training/wp-content/uploads/2022/02/text-description-automatically-generated-with-low.png)


# The AWS Global Infrastructure is made up of:

## - [[Region]]s  

## - Availability Zones  ([[AZ]]s)

## - [[Local Zone]]s  

## - AWS [[Wavelength]] Zones

## - AWS [[Outposts]]

## - [[CloudFront]]

## Edge Locations and Regional Edge Caches

[[Edge location]]s are Content Delivery Network ([[CDN]]) endpoints for [[CloudFront]].

*   There are many more edge locations than regions.
*   Edge Locations are distributed around the world
*   Content is published from the CloudFront Origin and cached.
*   Currently there are over 200 [[edge location]]s.
*   Regional Edge Caches sit between your CloudFront Origin servers and the [[Edge Location]]s.
*   A [[Regional Edge Cache]] has a larger cache-width than each of the individual [[Edge Location]]s.

The following diagram shows [[CloudFront]] Edge locations:

![aws-cloudfront-edge-cache](https://digitalcloud.training/wp-content/uploads/2022/02/aws-cloudfront-edge-cache.png)


