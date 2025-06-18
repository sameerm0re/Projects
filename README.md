## 🚀 EC2 Web App with Auto Scaling and Load Balancer

## 📌 Overview
This project demonstrates how to deploy a highly available, auto-scaled web application on AWS using EC2 instances behind an Application Load Balancer (ALB). It includes configuring Auto Scaling Groups, Launch Templates, and setting up a custom startup script to install a web server.

---

## 🛠️ Tech Stack
- AWS EC2
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- Launch Template
- Amazon Machine Image (AMI)
- User Data (Shell script)
- Amazon CloudWatch (optional)

---

## ⚙️ Architecture

```plaintext
                    Internet
                       │
                  [Route 53] (optional)
                       │
                ┌──────▼──────┐
                │ Application │
                │ Load Balancer│
                └──────┬──────┘
                       │
              ┌────────┴────────┐
        ┌─────▼─────┐     ┌─────▼─────┐
        │ EC2 Instance │  │ EC2 Instance │
        └────────────┘    └────────────┘
              (Auto Scaling Group)
