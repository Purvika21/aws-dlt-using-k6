# AWS Setup for Distributed Load Testing

## Overview
This document describes the AWS setup used to perform Distributed Load Testing using k6.

---

## Steps

### 1. Launch EC2 Instances
- Launch multiple EC2 instances using Amazon Linux
- Each instance acts as a load generator

### 2. Configure Security Groups
- Allow SSH (Port 22) from your IP
- Allow HTTP/HTTPS if required by the application

### 3. Connect to EC2
```bash
ssh -i <key-file>.pem ec2-user@<public-ip>

### 4.  Install k6
sudo dnf update -y
sudo dnf install -y https://dl.k6.io/rpm/repo.rpm
sudo dnf install -y k6

### 5.Run Distributed Tests
Copy k6 scripts to all EC2 instances
Execute the same script on all instances simultaneously

### 6.Monitoring
Monitor EC2 metrics using CloudWatch
Track CPU utilization, network traffic, and errors
