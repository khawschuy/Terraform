# Terraform Project Setup Guide

This guide will help you set up and deploy the infrastructure using Terraform. Follow the steps below to get started.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Terraform**: Download and install Terraform from the [official website](https://www.terraform.io/downloads.html).
- **AWS CLI**: Install the AWS Command Line Interface and configure it with your AWS credentials. You can find installation instructions [here](https://aws.amazon.com/cli/).
- **SSH Key**: Generate SSH key pairs for accessing EC2 instances. This is necessary for secure access to your instances.

## SSH Key Generation

Navigate to the `EC2` directory and run the following command to generate SSH keys:
```
cd module_EC2
ssh-keygen 
```

This will create a private key (`nhom20key`) and a public key (`nhom20key.pub`) in the `module_EC2` directory.

## Deployment Steps

1. **Initialize the Terraform Project**:
   Open a terminal, navigate to the project directory, and run:
```
terraform init
```

2. **Review Planned Changes**:
   Before applying changes, review what Terraform will do by running:
```
terraform plan
```

3. **Apply the Configuration**:
   Deploy the infrastructure by applying the configuration:
```
terraform apply
```
   Confirm the action when prompted.

4. **Destroy the Infrastructure**:
   When you no longer need the infrastructure, you can destroy it by running:
```
terraform destroy
```
   Confirm the action when prompted.

## Important Notes

- Always review changes with `terraform plan` before applying them with `terraform apply`.
- Use `terraform state` to manage the state of your infrastructure.
- Ensure sensitive information in `terraform.tfvars` is kept secure.

## Project Structure

- **main.tf**: Defines the main modules and their dependencies.
- **module_VPC**: Contains resources for VPC, subnets, and internet gateway.
- **module_NatGateway**: Manages the NAT Gateway and its Elastic IP.
- **module_RouteTable**: Configures route tables for public and private subnets.
- **module_SCG**: Sets up security groups for SSH and internal communication.
- **module_EC2**: Provisions EC2 instances with the specified key pairs and security groups.
