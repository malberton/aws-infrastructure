# AWS Infrastructure
---

This repo contains 3 sections:

#### Cloudformation

AWS Cloudformation code (written in YAML) to provision a base level of infrastructure. Currently contains:
  - VPC
  - Internet Gateway (IGW) and attachment to VPC
  - Four subnets: two public and two private. One of each is in an availability zone (Az0 and Az1)
  - NAT Gateway and allocated elastic IP
  - Public and private route tables with routes to IGW and NAT Gateway, respectively
  - Subnet associations to respective route tables (e.g. public subnet associated with public route table)

#### Deepstream

A service used for fast, scalable data syncing. This section is separate to highlight that one is a base infrastructure setup that is useful generally, whereas this Deepstream section is intended for a specific use-case

#### Ansible

A configuration management tool used to set up the Deepstream instances/auto-scaling groups once the infrastructure has been provisioned

---
## Remaining

#### Cloudformation

Some of these still need to be built, others are being mentioned here but won't be built to avoid publishing public IP addresses
- DHCP
- VPC Customer Gateway
- VPC Private Gateway
- VPN Connection and Attachment
- VPN Gateway Route Propagation
- Private Hosted Zone
- VPC Endpoint
- VPC Security Group(s)
- Public key

#### Deepstream

- All

#### Ansible

- All
