# 🔗 AWS VPC Peering Project

## 📌 Project Overview
This project demonstrates how to establish a secure connection between two Virtual Private Clouds (VPCs) using VPC Peering in AWS. It allows EC2 instances in different VPCs to communicate privately without using the internet.

---

## 🎯 Objective
- Create two VPCs with different CIDR blocks
- Launch EC2 instances in each VPC
- Establish VPC Peering connection
- Enable private communication using route tables

---

## 🏗️ Architecture

VPC-1 (10.0.0.0/16)
│
├── Public Subnet (10.0.1.0/24)
│   └── EC2 Instance

VPC-2 (192.168.0.0/16)
│
├── Public Subnet (192.168.1.0/24)
│   └── EC2 Instance

VPC Peering Connection between VPC-1 and VPC-2

---

## 🧭 Steps Involved

### 1. Create VPCs
- VPC-1 → 10.0.0.0/16
- VPC-2 → 192.168.0.0/16

### 2. Create Subnets
- VPC-1 → 10.0.1.0/24
- VPC-2 → 192.168.1.0/24

### 3. Launch EC2 Instances
- Enable public IP
- Allow SSH (port 22) and ICMP (ping)

### 4. Create VPC Peering
- Request from VPC-1
- Accept in VPC-2

### 5. Update Route Tables
- VPC-1 → 192.168.0.0/16 via Peering
- VPC-2 → 10.0.0.0/16 via Peering

### 6. Update Security Groups
- Allow ICMP and SSH traffic

### 7. Test Connectivity

ping
