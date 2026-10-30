AWS VPC Peering Project

A hands-on AWS networking project demonstrating secure communication between two isolated Virtual Private Clouds (VPCs) using VPC Peering.

Project Overview

This project establishes private network connectivity between two AWS VPCs in the Sydney region ("ap-southeast-2").

Architecture

- VPC-A: "10.10.0.0/16"
- VPC-B: "10.20.0.0/16"
- VPC Peering: Active
- Bastion Host: Public EC2 instance in VPC-A
- Private EC2-A: "10.10.2.154"
- Private EC2-B: "10.20.2.25"

AWS Services Used

- Amazon VPC
- VPC Peering
- Amazon EC2
- Security Groups
- Route Tables
- Internet Gateway
- AWS Systems Manager / EC2 Instance Connect

Implementation

1. Created two VPCs with non-overlapping CIDR blocks.
2. Configured public and private subnets.
3. Created and accepted a VPC Peering connection.
4. Configured route tables for inter-VPC communication.
5. Configured security groups for SSH and ICMP traffic.
6. Launched three EC2 instances, including a bastion host.
7. Established SSH connectivity to private instances through the bastion host.
8. Tested bidirectional ICMP communication between private instances.

Connectivity Test Results

Test| Result
Bastion to private EC2-A, TCP 22| Successful
Bastion to private EC2-B, TCP 22| Successful
VPC-B private EC2 to VPC-A private EC2, ICMP| Successful
VPC-A private EC2 to VPC-B private EC2, ICMP| Successful

Both ICMP tests returned 4 packets received with 0% packet loss.

Evidence

See the ""screenshots"" (screenshots/) folder for AWS configuration and connectivity test screenshots.

Key Learning Outcomes

- VPC networking and subnet design
- VPC Peering configuration
- Route table management
- Security group configuration
- Bastion-host-based SSH access
- Private network connectivity troubleshooting

Author

Sohan Jana

GitHub: "@sohanjana" (https://github.com/sohanjana)
