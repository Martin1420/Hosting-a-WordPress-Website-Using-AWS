
# WordPress Hosting on AWS

This repository contains resources and scripts used to deploy a WordPress website on AWS, leveraging various AWS services to ensure scalability, fault tolerance, and security.The project is showcased through my website, martinvalentines.com, which serves as a live demonstration of the deployment and configurations detailed here.

## Project Overview

The project involves setting up a robust WordPress hosting environment on AWS. It includes configuring AWS services and resources such as EC2, VPC, RDS, EFS, and more to create a scalable and secure web application platform.

### Key Features

- **VPC Configuration**: Set up with public and private subnets across two availability zones for enhanced fault tolerance.
- **Internet Connectivity**: Deployment of an Internet Gateway and NAT Gateway to ensure internet access for instances within the VPC.
- **Security**: Utilization of Security Groups as a firewall and EC2 Instance Connect for secure SSH access.
- **High Availability**: Use of multiple Availability Zones, an Application Load Balancer, and an Auto Scaling Group to distribute traffic and ensure availability.
- **Data Management**: Integration with RDS for database services and EFS for a shared file system.
- **Monitoring and Notification**: Configuration of SNS for activity alerts related to the Auto Scaling Group.
- **Domain Management**: Domain registration and DNS setup with Route 53.

## Prerequisites

Before you begin, ensure you have:

- An AWS account
- Basic knowledge of AWS services (EC2, VPC, RDS, EFS, etc.)
- Familiarity with Linux commands and environment

## Deployment Steps

1. **VPC Setup**: Follow the AWS documentation to create a VPC with public and private subnets across two Availability Zones.
2. **Internet Gateway & NAT Gateway**: Deploy these to provide internet access to instances in your VPC.
3. **Security Groups**: Configure as per the project requirements to secure your resources.
4. **EC2 Instances**: Launch EC2 instances within the private subnets for your web servers.
5. **Load Balancer & Auto Scaling**: Set up an Application Load Balancer and an Auto Scaling Group as described in the AWS documentation.
6. **RDS & EFS**: Create an RDS instance for the database and an EFS for shared storage.
7. **Route 53**: Register a domain and configure DNS settings.

## Scripts Usage

### WordPress Installation

1. Update packages and install Apache, PHP, and MySQL on your EC2 instance.
2. Mount the EFS to your EC2 instance for shared WordPress files storage.
3. Download and configure WordPress.

```bash
# Example command
sudo yum update -y
```

Repeat the installation steps as described in the script comments for detailed instructions.

### Auto Scaling Group Launch Template

Use this script for setting up new EC2 instances within the Auto Scaling Group. It includes package updates, Apache, PHP, MySQL installations, and EFS mounting.

## Contributing

Feel free to fork this repository and contribute by submitting a pull request. We appreciate your input in improving this project!


