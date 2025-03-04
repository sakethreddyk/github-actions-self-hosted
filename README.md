# Deploy a Simple Webpage using GitHub Actions on EC2

## Overview
This project demonstrates how to deploy a simple webpage to an EC2 instance using GitHub Actions and a self-hosted runner. The webpage will be served using Apache.

## Prerequisites

- **AWS Account**: You need an AWS account to create and manage EC2 instances.
- **GitHub Repository**: You need a GitHub repository for hosting the code.
- **EC2 Instance**: A running EC2 instance with a public IP (or DNS name).
- **GitHub Actions**: Basic knowledge of GitHub Actions workflows.
- **SSH Access to EC2**: You need to be able to SSH into the EC2 instance.

## Steps to Set Up

### 1. Launch an EC2 Instance on AWS
1. Log in to the [AWS Console](https://console.aws.amazon.com/).
2. Open the EC2 Dashboard and click **Launch Instance**.
3. **Choose an AMI**: Select **Ubuntu 22.04 LTS**.
4. **Instance Type**: Select `t2.micro` (free-tier eligible).
5. **Configure Security Group**: Allow **SSH (port 22)** and **HTTP (port 80)**.
6. **Launch** the instance and note down the **Public IP** or **DNS**.

### 2. Connect to the EC2 Instance
1. Open your terminal and SSH into the instance using the public IP and your key pair:
   ```sh
   ssh -i your-key.pem ubuntu@your-ec2-public-ip

### 3. Install and Configure GitHub Runner
1. In the github site go to settings --> Actions --> runners.
2. Create one self-hosted runners by clicking linux.
3. Follow the steps that mentioned there in the ec2 instance terminal.
4. Make sure to not share token information with anyone.
5. After running all the commands in the terminal it will take runners directory in terminal.

### If you commit any changes in the code then it gets automated with respective change. To check whether it is automated there is a yellow dot in github takes time to green tick mark. In the meanwhile terminal is running with the jobs and give the output as it is succeed or not.

