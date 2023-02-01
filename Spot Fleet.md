A Spot Fleet is a set of [[Spot Instance]]s and optionally On-Demand [[EC2]] Instances that is launched based on criteria that you specify. 
*   The Spot Fleet selects the Spot capacity pools that meet your needs and launches Spot Instances to meet the target capacity for the fleet. 
*   By default, Spot Fleets are set to _maintain_ target capacity by launching replacement instances after Spot Instances in the fleet are terminated. 
*   You can submit a Spot Fleet as a one-time _request_, which does not persist after the instances have been terminated. 
*   You can include On-Demand Instance requests in a Spot Fleet request.