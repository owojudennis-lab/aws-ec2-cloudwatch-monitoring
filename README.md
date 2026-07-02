# AWS EC2 Monitoring with CloudWatch, IAM, and SNS
## Overview

This project demonstrates how to deploy and monitor an Ubuntu EC2 instance on AWS using production-style monitoring practices.

The environment hosts an Nginx web server and uses Amazon CloudWatch Agent to collect operating system metrics including CPU, memory, disk, and network utilization. CloudWatch Dashboards provide real-time visualization of metrics and enable rapid detection of anomalies.

The project emphasizes secure authentication using IAM Roles instead of long-term AWS credentials.

## Architecture

<p align="center">
  <img src="architecture/architecture-diagram.png" alt="AWS EC2 Monitoring Architecture" width="800">
</p>

## AWS Services

- Amazon EC2
- Amazon CloudWatch
- Amazon CloudWatch Agent
- Amazon SNS
- AWS IAM
- Amazon VPC
- Security Groups

## Skills Demonstrated

- Linux Server Administration
- EC2 Deployment
- IAM Role Configuration
- Nginx Installation
- CloudWatch Monitoring
- CloudWatch Dashboards
- CloudWatch Alarms
- Amazon SNS Notifications
- Infrastructure Troubleshooting

## Validation

Monitoring was validated by generating CPU load using:

yes > /dev/null &
yes > /dev/null &

## Lessons Learned

- CloudWatch does not collect memory metrics by default.
- The CloudWatch Agent is required for operating system metrics such as memory and disk utilization.
- IAM Roles eliminate the need to store AWS access keys on EC2 instances.
- CloudWatch CPUUtilization is averaged across all available vCPUs.
- Monitoring should always be validated by generating real workload rather than assuming the configuration is correct.
