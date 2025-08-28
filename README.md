# AWS IaC – Secure 2-Tier

CloudFormation template that deploys a secure 2-tier LAMP-style architecture:

- **Web Tier (Public Subnet):** EC2 instance with Apache + PHP
- **Database Tier (Private Subnet):** EC2 instance with MySQL, no public IP
- **Networking:** VPC, public/private subnets, IGW, NAT Gateway, route tables
- **Security:** Web SG (HTTP/SSH), DB SG (MySQL only from Web SG)
- **Automation:** UserData installs Apache/PHP on web, MySQL on DB with sample schema & data

# Outputs 

- Elastic IP of web server
- Private IP of web server
- Private IP of DB server

# What I Learned

- VPC design with isolated subnets
- Security group design for least privilege
- CloudFormation modular resource creation
- Automating software installs via EC2 UserData
