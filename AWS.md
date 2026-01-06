1. EC2 -> Elastic Compute Cloud.
   1. EC2 provides Web services API for managing and provisioning virtual machines inside Amazon Cloud or Amazon's data centers.
   2. Ease in scaling up (from 8GB to 16GB) or down (from 8Gb to 4GB).
   3. EC2 service is easily integrated with other services like S3, EFS, RDS, DynamoDB, and Lambda.
   4. Pricing
      1. On demand -> Pay per hour or seconds.
      2. Reserved -> Reserved capacity for 1 to 3 years for discounts.
      3. Spot -> Bid your price for unused EC2 capacity. The problem is that if someone outbids, then the instance is gone.
      4. Dedicated Hosts -> Physical server is dedicated.
  5. Components of EC2 instance or service:
     1. AMI (Amazon Machine Image) -> Ready-made virtual machine like vagrant. Huge list to choose from. Virtual server in the cloud.
     2. Instance type -> Determines the hardware of the host computer used for the instance.
     3. Amazon Elastic Block Storage (EBS) -> Flexible, cost-effective, and easy-to-use data storage options for the instances. EBS are the virtual hard disks on which you can store your operating system and also store your data.
     4. Tags -> Simple label consisting of a customer-defined key and an optional value that makes it easier to manage, search for, and filter resources.
     5. Security Group -> Acts as a virtual firewall that controls the traffic for one or more instances.
     6. Key-Pair -> To log in to EC2 instances.
     7. 
