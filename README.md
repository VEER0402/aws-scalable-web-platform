# 🚀 AWS Production Architecture with Auto Scaling & Load Balancer


<img width="419" height="329" alt="image" src="https://github.com/user-attachments/assets/c0190d52-5bc1-4ddd-950a-828bf7d52ad3" />


## 📌 Project Overview

Designed and implemented a scalable AWS infrastructure using Auto Scaling Group, Application Load Balancer, and secure access via Bastion Host.

The project demonstrates real-world challenges in deploying applications across private instances and handling traffic routing issues.



---


# 🏗️ Architecture Overview

<img width="2816" height="1536" alt="dj" src="https://github.com/user-attachments/assets/54569e2f-664c-4063-9d04-6068a097c4df" />


---

# ⚡ Key Features

- Auto Scaling Group with private EC2 instances
- Application Load Balancer for traffic distribution
- Bastion Host for secure administrative access
- Public and private subnet architecture
- Security Group based traffic control
- High availability focused deployment design
- Real-world load balancing troubleshooting scenario

---

# ☁️ AWS Services Used

- VPC
- EC2
- Auto Scaling Group
- Application Load Balancer
- Bastion Host
- Security Groups
- Route Tables
- Internet Gateway

---

# 🔐 Security Design

- Private EC2 instances without public IPs
- SSH access restricted through Bastion Host
- Controlled inbound/outbound traffic using Security Groups
- Network isolation between public and private infrastructure layers

---

# ⚙️ Deployment Workflow

1. Create VPC and subnet architecture
2. Launch Bastion Host in public subnet
3. Deploy EC2 instances in private subnet
4. Configure Auto Scaling Group
5. Attach instances to Application Load Balancer
6. Configure routing and health checks
7. Validate application accessibility

---

# 🚨 Real-World Challenge Faced

Initially, the application was deployed on only one EC2 instance while the Load Balancer distributed traffic across multiple instances.

This caused intermittent failures because some targets did not have the application running.

### Debugging Performed
- Verified target group health checks
- Checked application availability across instances
- Investigated ALB routing behavior
- Validated EC2 connectivity and deployment consistency

### Resolution
The deployment strategy was updated to ensure application availability across all instances in the Auto Scaling Group.

---

# 📊 Future Improvements

- Terraform-based infrastructure provisioning
- CloudWatch monitoring and alerting
- Automated application deployment using user_data
- CI/CD integration for infrastructure automation
- Launch Templates for immutable deployments
- HTTPS integration using ACM

---

# 🛠️ Tech Stack

- AWS
- Linux
- Python (Flask)
- Bash
- Networking & Security Concepts

---

# 📌 Key Learnings

- Private subnet deployment strategies
- Load balancing behavior and traffic routing
- Secure infrastructure access patterns
- High availability architecture concepts
- Troubleshooting distributed deployments
- Scaling and deployment consistency challenges



# ⚠️ Failure Scenarios Considered

- Application deployed on partial instances
- Unhealthy target group instances
- Incorrect Security Group rules
- ALB health check failures
- SSH access issues through Bastion Host
- Traffic routing inconsistencies
