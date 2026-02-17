# AWS Task 2: Custom VPC and EC2 Deployment

## Project Description
This task involves setting up a custom AWS networking environment (VPC) and deploying a Linux EC2 instance within a public subnet to demonstrate foundational cloud networking skills.
- **VPC CIDR**: `10.0.0.0/16`
- **Internet Gateway**: Created and attached `awstaks2-igw` to allow external connectivity.
- **Subnets**:
    - **Public Subnet**: `10.0.1.0/24` (Associated with a Route Table pointing to the IGW).
    - **Private Subnet**: `10.0.2.0/24` (Isolated from direct internet access).
- **Route Table**: Configured `awstaks2-public-rt` with a route to `0.0.0.0/0` via the Internet Gateway.
- **Instance Type**: `t2.micro`
- **AMI**: Amazon Linux 2023
- **Network**: Launched into the custom Public Subnet with a **Public IPv4 address (13.127.195.55)**.
- **Security Group**: 
    - Port 22 (SSH) allowed from My IP.
    - Port 80 (HTTP) allowed from Anywhere.
- Successfully connected to the instance via SSH using the `.pem` key.
- Verified that the instance is correctly routed through the custom VPC Internet Gateway.
