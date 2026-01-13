## EC2 Instance

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
2. Right approach to create EC2 instances:
   1. Requirements gathering.
   2. Key pairs.
   3. Security group (firewall).
   4. Launch instance.
  
## AWS CLI (Command Line Interface)
1. Install on Mac: brew install awscli
2. Create an access key for the user through IAM.
3. The Key Pair will be downloaded.
4. In the command line:
   1. aws configure -> provide all the details.
   2. cat ~/.aws/config -> to check configuration.
   3. cat ~/.aws/credentials -> to check the key pair.
   4. aws sts get-caller-identity -> if the output returned is correct, proceed; else aws configure again.
   5. aws ec2 describe-instances -> to describe instances within the region.
  
## Elastic Block Store (EBS)
1. Block based storage.
2. Runs ec2 OS (root volume data), stores data from db, file data, etc.
3. While creating volume the availability zone (AZ) should be mentioned. The EC2 instance should be in the same AZ as the EBS volume.
4. Automatically replicated within the AZ to protect from failure.
5. A snapshot is backup of a volume.
6. EBS Types:
   1. General purpose (SSD): Most work loads.
   2. Provisioned IOPS: Larger volume than SSD and high input output per second. Used for large databases.
   3. Throughput Optimized HD: Big data and Data Warehouses.
   4. Cold HDD: For file servers. Low cost.
   5. Magnetic: Used for backups and archives. Very cheap.


## AWS Elastic Load Balancers (ELB)
1. A load balancer takes the request from the user on a specific port number, like 80 or 443, and forwards the request to the web server, distributing this traffic.
2. Acts as a single endpoint on which the user can access.
3. It will have an endpoint on which the user will access a frontend port. And when it receives this request, it is going to route to a backend port, which will be the port number of the server.
4. AWS provides Elastic Load Balancers.
5. Different types of load balancers in AWS are: Application load balancer, network load balancer, gateway load balancer, and classic load balancers.
6. Classic: Takes requests on the frontend port and routes to the backend server port. Ideal for a simple solution. Works on OSI layer 4 (Meaning it doesn't understand the URL, it understands the IP address and the port number (frontend and backend)).
7. Application: For http and https traffic. Works on OSI layer 7 (meaning it understands URL and routes based on URL). Used the most on AWS for HTTP and https traffic. It is intelligent routing.
8. Network: Provides a static IP address. Can handle millions of requests per second. Very expensive. Works on OSI layer 4. Sometimes, put in front of the application load balancer.
9. Gateway: Works on the OSI layer 3. Used to run and manage firewalls and intrusion detection systems.


## CloudWatch
1. Primary function is to monitor the performance of the AWS environment.
2. It automatically provides standard metrics for monitoring each service. Custom metrics of choice can also be set up (like alarms, notifications).
3. Captures events that provide real time stream of events happening.
4. Provides logs. EC2 does not have direct logs, and hence an agent can be set up that streams logs to the CloudWatch service.
5. Alarms monitor CloudWatch metrics for instances. In case of threshold spikes, Amazon SNS (Simple Notification Service) sends these warnings as messages to subscribing endpoints or clients.
6. SNS: is a web service that coordinates and manages the delivery of messages.


## Elastic File System (EFS)
1. It is a shared file system hosted on the cloud.
2. Access Points -> Connect EFS to the file system.

## Autoscaling Group
1. A service that automatically monitors and adjusts compute resources to maintain performance for applications hosted in AWS.
2. Alarm monitors CloudWatch metrics for Instances.
3. A launch configuration/Template is an instance configuration template that an Auto Scaling group uses to launch EC2 instances.
4. Scaling policy is used to add or remove instances dynamically according to the maximum and minimum limits provided, adding to maintain performance and removing to maintain cost.

## Simple Storage Service
1. S3:
   1. Storage service for the internet.
   2. Used to store and retrieve any amount of data at any time, from anywhere on the web.
   3. It is an object-based storage.
   4. When data is uploaded to the S3 bucket, it is replicated across multiple facilities.
   5. Unlimited storage.
   6. Stores data as objects within buckets.
   7. Bucket name has to be unique.
   8. A bucket is a logical unit of storage in AWS.
   9. Object storage is a computer data storage architecture that manages data as objects.
   10. Storage Types:
       1. S3 standard: General-purpose storage of frequently accessed data. Fast access and object replication in multi-Availability Zones (AZ). Charged accordingly.
       2. S3 IA- Infrequent Access: Long-lived, less frequently accessed data. Slow access, object replication in multi-AZ. Less expensive and auto-replication to protect against data loss.
       3. S3 One Zone-IA: For data that is accessed less frequently but requires rapid access when needed. Slow access, no object replication.
       4. S3 Intelligent Tiering: Automatically moves data to the most cost-effective tier.
       5. S3 Glacier: Low-cost storage class for data archiving.
       6. S3 Glacier Deep Archive: Lowest cost storage, retrieval time of 12 hours.
      
   11. Lifecycle Policies: When uploading object, you can decide what storage type, or you can also set a lifecycle policy that can move your object from one storage type to another based on its age.
   12. S3 charges are based on storage, requests, tiers, data transfer, and region replication.

## Relational Database (RDS)
1. It is a distributed relational database service.
2. High availability through Multi-AZ deployments.
3. Easy to scale.
4. Read replicas for performance.
