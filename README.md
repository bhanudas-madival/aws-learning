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

# AWS SAA-C03 - EC2 Fundamentals

## AWS Budget
- Learned how AWS Budgets help monitor costs and usage
- Understood budgets can be used to receive spending alerts

## Amazon EC2
- Learned EC2 (Elastic Compute Cloud) provides virtual servers in AWS
- Understood the basic EC2 instance launch workflow

## EC2 Instance Launch
- Launched EC2 instances through the AWS Console
- Selected AMI for the operating system
- Selected appropriate Instance Type
- Created and used a Key Pair
- Configured Security Groups
- Configured storage and networking options
- Added User Data during instance launch

## EC2 User Data
- Learned User Data executes automatically during the first instance boot
- Used User Data to automatically deploy a web server
- Verified the deployed website through the browser

## EC2 Instance Types
- Learned the EC2 naming convention
- Studied instance families:
  - General Purpose
  - Compute Optimized
  - Memory Optimized
  - Storage Optimized
- Understood when each family should be selected

## Security Groups
- Learned Security Groups act as stateful virtual firewalls
- Configured Inbound and Outbound Rules
- Understood Security Groups contain only Allow rules
- Practiced allowing HTTP and SSH access
- Reviewed common ports:
  - SSH (22)
  - FTP (21)
  - HTTP (80)
  - HTTPS (443)
  - RDP (3389)

## EC2 Connectivity
- Learned multiple methods to connect to EC2 instances:
  - SSH
  - OpenSSH (Windows 10/11)
  - PuTTY
  - EC2 Instance Connect
- Practiced SSH connectivity
- Learned common SSH troubleshooting steps

## IAM Roles for EC2
- Learned how IAM Roles provide temporary credentials to EC2 instances
- Understood why IAM Roles are preferred over Access Keys on EC2

## EC2 Purchasing Options
- Learned On-Demand Instances
- Learned Spot Instances
- Compared use cases and cost differences
- Performed hands-on with EC2 launch options

## Section Completion
- Completed Section 5: EC2 Fundamentals
- Created a minimal Anki deck covering important concepts and practical labs for long-term retention

# AWS SAA-C03 - EC2 Solutions Architect Associate Level

## Public IP vs Private IP vs Elastic IP
- Learned the differences between Private IP, Public IP and Elastic IP
- Understood when each IP type is assigned and used
- Practiced allocating and associating an Elastic IP with an EC2 instance
- Learned Elastic IPs are static public IPv4 addresses

## EC2 Placement Groups
- Learned the purpose of Placement Groups
- Studied the three placement strategies:
  - Cluster
  - Spread
  - Partition
- Understood the use cases and trade-offs of each strategy
- Performed hands-on creating and testing Placement Groups

## Elastic Network Interface (ENI)
- Learned what an ENI is and its purpose
- Understood primary and secondary private IP addresses
- Learned ENIs can be detached and attached to supported EC2 instances
- Performed hands-on working with ENIs

## EC2 Hibernate
- Learned the difference between Stop, Terminate and Hibernate
- Understood that Hibernate preserves the in-memory (RAM) state
- Learned Hibernate requirements and limitations
- Performed hands-on hibernating and resuming an EC2 instance

## Section Completion
- Completed Section 6: EC2 – Solutions Architect Associate Level
- Completed all hands-on labs and quiz

# AWS SAA-C03 - EC2 Instance Storage

## Amazon EBS (Elastic Block Store)
- Learned EBS provides persistent block storage for EC2 instances
- Understood EBS volumes are network-attached storage
- Learned EBS volumes are limited to a single Availability Zone
- Practiced creating, attaching, detaching and deleting EBS volumes
- Learned Delete-on-Termination behavior for root and additional volumes

## EBS Snapshots
- Learned snapshots provide point-in-time backups of EBS volumes
- Practiced creating and restoring EBS snapshots
- Learned snapshots can be copied across Availability Zones and Regions
- Studied Snapshot Archive, Recycle Bin and Fast Snapshot Restore (FSR)

## Amazon Machine Images (AMI)
- Learned an AMI is a customized template used to launch EC2 instances
- Practiced creating a custom AMI from an EC2 instance
- Launched a new EC2 instance from the custom AMI
- Learned AMIs are Region-specific and can be copied to other Regions

## EC2 Instance Store
- Learned the difference between Instance Store and EBS
- Understood Instance Store provides high-performance temporary local storage
- Learned Instance Store data is lost when the instance stops or hardware fails
- Identified suitable use cases such as cache, buffers and temporary data

## EBS Volume Types
- Studied General Purpose SSD (gp2, gp3)
- Studied Provisioned IOPS SSD (io1, io2)
- Studied Throughput Optimized HDD (st1)
- Studied Cold HDD (sc1)
- Learned appropriate workloads and performance characteristics for each volume type

## EBS Multi-Attach
- Learned io1/io2 volumes support Multi-Attach
- Understood a single EBS volume can be attached to multiple EC2 instances within the same Availability Zone
- Learned cluster-aware file systems are required

## EBS Encryption
- Learned EBS encryption uses AWS KMS
- Understood encryption protects data at rest, snapshots and data in transit between EC2 and EBS
- Learned how to encrypt an existing unencrypted volume using snapshots

## Amazon EFS (Elastic File System)
- Learned EFS is a managed NFS file system
- Understood EFS can be mounted by multiple EC2 instances across multiple Availability Zones
- Practiced creating and mounting an EFS file system
- Learned EFS uses Security Groups to control network access
- Compared EFS with EBS and identified appropriate use cases for each

## Section Completion
- Completed Section 7: EC2 Instance Storage
- Completed all hands-on labs, cleanup and quiz

Complete GitHub Pull Request workflow and collaboration practice

- Practiced feature branch workflow on GitHub
- Created and pushed a feature branch
- Opened a real Pull Request
- Reviewed Pull Request architecture and GitHub interface
- Explored Conversation, Commits, Files Changed, and Review workflow
- Merged a Pull Request into the main branch
- Practiced remote branch cleanup and synchronization
- Reinforced fork, origin/upstream, and GitHub collaboration concepts
AWS Fundamentals & IAM

**Date:** 27 July 2026

### Topics Covered

#### AWS Cloud Fundamentals
- AWS Cloud History
- AWS Cloud Facts
- AWS Cloud Use Cases

#### AWS Global Infrastructure
- AWS Regions
- Availability Zones (AZs)
- Edge Locations / Points of Presence
- Choosing the Right AWS Region
- Global vs Regional AWS Services

#### Identity & Access Management (IAM)
- IAM Users
- IAM Groups
- IAM Policies
- IAM Policy Structure
- IAM Policy Inheritance
- IAM Roles
- Password Policies
- Multi-Factor Authentication (MFA)
- MFA Device Options
- Access Keys
- AWS CLI
- AWS SDK
- IAM Security Tools
- IAM Best Practices

### Key Concepts Learned

- Difference between Regions, AZs, and Edge Locations
- Factors for selecting an AWS Region
- Global services vs Regional services
- IAM authentication and authorization
- Principle of Least Privilege
- IAM Users, Groups, Policies, and Roles
- Password policies and MFA for enhanced security
- Programmatic access using Access Keys
- Difference between AWS Management Console, CLI, and SDK
- IAM security recommendations and best practices

### Status

- ✅ Completed theory
- ⏳ Hands-on practice planned
