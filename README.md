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
