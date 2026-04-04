# 🚀 AWS Production-Style Architecture with Auto Scaling & Load Balancer


<img width="419" height="329" alt="image" src="https://github.com/user-attachments/assets/c0190d52-5bc1-4ddd-950a-828bf7d52ad3" />


## 📌 Project Overview

Designed and implemented a scalable AWS infrastructure using Auto Scaling Group, Application Load Balancer, and secure access via Bastion Host.

The project demonstrates real-world challenges in deploying applications across private instances and handling traffic routing issues.



---

## 🏗 Architecture Design

* **Auto Scaling Group**

  * Created EC2 instances in private subnet (no public IP)
  * Ensured high availability across instances



* **Bastion Host**

  * Launched in public subnet for secure SSH access
  * Used as a jump server to connect private instances


* **Application Load Balancer**

  * Configured to distribute incoming traffic across instances



* **Security Groups**

  * Defined inbound/outbound rules for controlled access



## ⚙️ Implementation Details

1. Created Auto Scaling Group with private EC2 instances
2. Verified instances had only private IPs (no direct internet access)
3. Created a Bastion Host for secure access
4. Used SCP to transfer PEM key securely to Bastion
5. Connected to private EC2 via Bastion using SSH
6. Deployed Python application on one instance only
7. Configured Load Balancer to route traffic



---



## ⚠️ Challenges Faced

* ❌ Initially deployed application on only ONE instance
  → Load balancer sent traffic to both instances
  → Result: **Intermittent failures / errors**



* 🔍 Debugged issue by:

  * Checking target group health
  * Verifying application availability on instances




## 🔐 Security Design

* Private EC2 instances have no public access
* SSH access only via Bastion Host
* Controlled access using Security Groups

---




## 🛠 Tech Stack

* AWS EC2
* VPC
* Auto Scaling Group
* Application Load Balancer
* Bastion Host
* Security Groups
* Python (Flask)
