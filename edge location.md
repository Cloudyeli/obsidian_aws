**Edge locations are AWS data centers designed to deliver services with the lowest latency possible.** Amazon has dozens of these data centers spread across the world. They’re closer to users than [[Region]]s or Availability Zones ([[AZ]]), often in major cities, so responses can be fast and snappy. A subset of services for which latency really matters use edge locations, including:

-   AWS [[CloudFront]], which uses edge locations to cache copies of the content that it serves, so the content is closer to users and can be delivered to them faster.
-   AWS [[Route 53]], which serves [[DNS]] responses from edge locations, so that DNS queries that originate nearby can resolve faster.
-   AWS [[WAF]] and AWS [[Shield]], which filter traffic in edge locations to stop unwanted traffic as soon as possible.