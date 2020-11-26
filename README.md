### Cloud Computing
- on-demand delivery of computer power
- could be databases,storage,networking,software,analytics
- applications
- other IT resources
- pay-as-you-go pricing model

### AWS History
- started using the concept of decouples services
- services that didn't depend on other services
- creation of well documented API
- Unbunduling FSI Value changes

### Types of Cloud models
- Iaas
- Paas
- Saas

### Cloud Deployement model
- Cloud
- Hybrid
- On-premises(Private)

### AWS Value Proposition
- access wia API,SDK,CLI
- cost savings
- increased speed and agility
- security
- performance

### IAM
- AWS Identity and Access Management
- web service to access control to AWS resources.

*Features*
- Shared access to your AWS account
- Granular permissions
- Secure access to AWS resources for applications that run on amazon EC2
- MFA
- Identity Federation
- Identity information for assurance
- Free to use

### Accessing IAM
- via AWS Mgmt console,CLI tools,AWS SDK
- IAM HTTPS API

### How does IAM work?
- Resources
- Identities
- Entities
- Principles

AWS supports the use of federated identities to gain temporary access to our AWS account.

### IAM Roles
An IAM role is similar to a user.Its an identity with permission policies assigned to it.The permissions define what AWS service requests that the role has authorization to execute.

An IAM role permits us to delegate access,along with defined permissions,to trusted entities without having to share long-term access keys.

We create a role in nearly the same way that we create an ordinary user.We just name the role and then attach a policy to it.

user or identity to define a set of permission to make a set of aws requests.

IAM roles permits to deligate access and define permission to trusted entities on a temporary basis for eg to EC2 access and restricting access to other resources.

Name a role and attach policies to the role.

### AWS S3

AWS S3 is AWS storage. It has a simple web services interface that we can use to store and retrieve almost any amount of data.

A bucket is a container for objects stored in S3.

We can use Amazon S3 for backup and ariving,Static website hosting,Disaster recovery,content storage and many more applications.

- AWS Simple Storage Service
- Used for Media sharing,Software distribution,Backup,Online storage,Application storage
- Amazon S3 is a simple key value store.
- It is designed to store as many objects as we want
- A key is the name that we assign to an object.We use the object key to retrieve the object in our bucket.
- Within a bucket,a key and version ID uniquely identify an object.
- The version ID is a string that AMazon S3 generates when we add an object to our bucket.
- A value is the content that we are storing.An object value can be any sequence of bytes.Objects can range in size from 0 to 5TB.
- Metadata is a set of name-value pairs that we can use to store information about our object.
- we can assign metadata,(user-defined metadata),to our objects in Amazon S3.
- Amazon S3 also assigns system-metadata to our objects that it uses for management purposes.
- Amazon S3 supports Access Control Lists(ACL) and user-based access control.

S3 scalability,Durability,Avalability

built in error correction
version of data

### Amazon S3 Storage Classes

99.99999999999% durability

- S3 Standard
    - Big data analysis
    - Content distribution
    - static website hosting
- S3 Standard IA(Infrequent access)
    - Backup & archive
    - disaster recovery
    - file sync & share
    - Long retained data
- Amazon S3 Glacier
    - Long term archive
    - Digital preservation
    - Magnetic tape Replacement

### Data lifecycle management
- Transition standard to standard-IA
- Transition Standard-IA to Amazon Glacier
- Expiration lifecycle policy
- Versioning support

### AWS EC2

- Elastic Compute Cloud(EC2) provides us with scalable computing capacity in the AWS cloud.
- An EC2 instance will eliminate the requirement for us to spend money on hardware up front
- We would also be able to configure networking,security,and manage our storage needs.
- EC2 enables us to handle changes in requirements.
- Aids in forcasting requirements
- EC2 instances are virtual computing environments
- Amazon Machin Image(AMI) are preconfigured template for our instances.
- Secure login information for our instances using key pairs
- Create storage volumes for temporary data that's deleted when we stop or terminate our instance.These are called instance store volumes
- For persistent storage volumes for our data,we can use Amazon Elastic Block Store(Amazon EBS)
- Multiple physical locations for our instances and Amazon EBS volumes
- We can launch different types of instances from a single AMI.An instance type determines the hardware of the host computer used for our instance.
- Instance type falls into the following categories:
    - General Purpose - Amazon EC2 A1 instances
    - Compute Optimized - C5 instances are optimized for compute intensive workloads.
    - Memory Optimized - used for memory intensive applications such as high performance databases
    - Accelerated Computing - commonly used for machine learning
    - Storage Optimized - HDD-based local storage,delivers high disk throughput,and a balance of compute and memory
- There are 4 ways to pay for EC2 usage:
    - pay-as-you-go(On-Demand)
    - reserved instances
    - Amazon EC2 spot instances
    - A dedicated Host

### AWS VPC

An amazon Virtual Private Cloud enables us to launch AWS resources intoa virtual network we define.This virtual network resembles a traditional data center network

- As a part of the default VPC,AWS creates a /16 IPV4 CIDR block,/20 subnets,an internet gateway,security group,ACL and DHCP option set.
- Only subnet is permitted per availability zone.

https://cidr.xyz/
