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

