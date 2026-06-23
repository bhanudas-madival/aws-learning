# AWS SAA-C03 - Day 1

## Topics Covered

### AWS Fundamentals
- AWS = Amazon Web Services
- Cloud computing provides on-demand resources and easy scalability
- AWS services are used by organizations worldwide

### AWS Global Infrastructure
- Region = Geographic area containing multiple Availability Zones
- Availability Zone (AZ) = One or more isolated data centers within a Region
- AZs are connected using high-bandwidth, low-latency networking
- Region selection factors:
  - Compliance
  - Latency
  - Service Availability
  - Pricing

### Global vs Regional Services
- IAM = Global service
- EC2 = Regional service
- Resource visibility depends on selected Region for regional services

### IAM (Identity and Access Management)
- IAM is used to manage authentication and authorization
- Root User is created when the AWS account is created
- Best practice: use IAM Users for daily work
- IAM Groups help manage permissions for multiple users
- Users can belong to multiple groups
- Groups cannot contain other groups
- Permissions are defined using IAM Policies
- Follow the Principle of Least Privilege

### Hands-On Lab Completed
- Created AWS account
- Created IAM user: Bhanu
- Created Admin group
- Attached AdministratorAccess policy
- Added user to Admin group
- Created account alias: mbhanudas
- Logged in using IAM user
- Verified IAM user inherited permissions from Admin group

### Key Takeaways
- IAM is Global
- EC2 is Regional
- Root account should be used sparingly
- Groups simplify permission management
- AdministratorAccess provides full administrative permissions

📅 Day Commit – AWS IAM & CLI Fundamentals

Today I completed and practiced core AWS Identity and Access Management (IAM) concepts:

✅ IAM Users, Groups, and Policies
✅ Created and managed IAM users and groups
✅ Attached and tested IAM policies
✅ Understood AWS Console simultaneous sign-in behavior
✅ Learned IAM MFA concepts and configured MFA hands-on
✅ Learned AWS Access Keys and their use with CLI/SDK
✅ Installed and configured AWS CLI on Linux
✅ Practiced AWS CLI commands using configured credentials
✅ Explored AWS CloudShell and its regional availability

Key Takeaways:

* IAM controls authentication and authorization in AWS.
* Users inherit permissions through groups and attached policies.
* MFA adds an important security layer for AWS accounts.
* Access Keys enable programmatic access through AWS CLI and SDKs.
* AWS CLI allows managing AWS resources directly from the terminal.
* CloudShell provides a browser-based shell with AWS CLI preconfigured.

Hands-on Skills Gained:

* IAM user creation and permission management
* MFA configuration
* AWS CLI setup and credential configuration
* Basic AWS CLI operations
* CloudShell usage

# AWS SAA-C03 - IAM Reinforcement

## IAM Concepts

* Clarified AWS Account vs Root User vs IAM User
* Understood AWS Account contains:

  * Root User
  * IAM Users
  * Groups
  * Policies
  * Roles
  * AWS Resources

## Account Alias

* Confirmed Account Alias belongs to the AWS Account
* Verified Account Alias is not tied to a specific IAM User
* Understood IAM Users use the Account Alias login URL

## IAM Permissions

* Reviewed permission inheritance through IAM Groups
* Revisited AdministratorAccess policy behavior

## IAM Policy Structure

* Studied policy components:

  * Statement
  * Effect
  * Action
  * Resource
  * Condition
* Understood how IAM policies define permissions

## IAM & AWS CLI Revision

* Reviewed key IAM concepts from completed section
* Created concept and practical Anki cards for retention
* Identified high-value concepts for SAA-C03 preparation

# AWS SAA-C03 - EC2 Fundamentals

## AWS Budget Setup
- Learned AWS Budget for cost monitoring and alerts
- Understood importance of tracking AWS spending

## EC2 Basics
- EC2 (Elastic Compute Cloud) provides virtual servers in AWS
- EC2 instances can be launched on demand
- Learned basic EC2 launch workflow

## EC2 Instance Hands-On
- Launched an EC2 instance
- Selected AMI
- Selected Instance Type
- Configured Key Pair
- Configured Security Group
- Used User Data during instance launch

## EC2 User Data
- User Data runs automatically during instance startup
- Used User Data to automate website deployment
- Understood basic instance bootstrapping

## EC2 Instance Types
- Learned purpose of different instance families
- General Purpose
- Compute Optimized
- Memory Optimized
- Storage Optimized

## Security Groups
- Learned Security Groups act as instance-level firewalls
- Understood Inbound and Outbound Rules
- Security Groups contain Allow rules
- Learned common ports:
  - SSH (22)
  - HTTP (80)
  - HTTPS (443)
  - FTP (21)
  - RDP (3389)
## IAM & Region Review

### AWS Regions
- Latency
- Compliance / Data Residency
- Service Availability
- Cost

### Availability Zones
- Isolated data centers within a Region
- Connected by low-latency network
- Improve fault tolerance and availability

### IAM
- IAM Users
- IAM Groups
- IAM Policies
- IAM Roles
- Policy Inheritance
- MFA

### AWS CLI
- `aws configure`
- `aws --version`
- `aws sts get-caller-identity`

### IAM Roles
- Create Role
- Trusted Entity: EC2
- Attach permissions to EC2 without storing access keys
