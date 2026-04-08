# 🚀 Highly Available Web Application with Auto Scaling & Monitoring

## 📌 Project Overview
This project demonstrates how to build a **highly available, scalable, and monitored web application** using AWS services.

The architecture ensures that the application remains available even during high traffic by automatically scaling resources and distributing load efficiently.

---

## 🎯 Objective
- Deploy a web application on AWS EC2
- Achieve high availability using Load Balancer
- Implement Auto Scaling based on demand
- Monitor system performance using CloudWatch
- Send alerts using SNS

---

## 🛠️ Technologies & Services Used
- AWS EC2 (Elastic Compute Cloud)
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- Launch Template
- Amazon Machine Image (AMI)
- CloudWatch (Monitoring)
- SNS (Notifications)
- Apache / Nginx Web Server
- Git & GitHub

---


---

## 🛠️ Technologies & Services Used
- AWS EC2 (Elastic Compute Cloud)
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- Launch Template
- Amazon Machine Image (AMI)
- CloudWatch (Monitoring)
- SNS (Notifications)
- Apache / Nginx Web Server
- Git & GitHub

---

## 🏗️ Architecture Diagram


User → Load Balancer → Auto Scaling Group → EC2 Instances (Web App)
↓
CloudWatch → SNS → Email Alerts


---

## 🔄 Workflow

1. Launch an EC2 instance and install web server (Apache/Nginx)
2. Deploy application using Git
3. Create AMI from configured instance
4. Create Target Group (HTTP:80)
5. Create Application Load Balancer
6. Create Launch Template using AMI
7. Create Auto Scaling Group (Min: 2, Max: 4)
8. Attach Load Balancer to Auto Scaling Group
9. Configure scaling policies based on CPU
10. Setup CloudWatch alarms
11. Configure SNS for email notifications

---

## ⚙️ Setup Steps

### 🔹 Step 1: EC2 Setup
- Launch EC2 instance
- Install Apache:
  
  sudo yum install httpd -y
  sudo systemctl start httpd
Install Git and clone project

Step 2: Deploy Application

git clone <your-repo-url>
cd project-folder
cp -r * /var/www/html/

🔹 Step 3: Create AMI
Go to EC2 → Actions → Create Image
Name: webserver-ami
🔹 Step 4: Load Balancer
Create Target Group (HTTP:80)
Create Application Load Balancer
Attach target group
🔹 Step 5: Launch Template
Select created AMI
Configure instance type, security group
🔹 Step 6: Auto Scaling Group
Min instances: 2
Max instances: 4
Attach Load Balancer
🔹 Step 7: Scaling Policy
Scale out when CPU > 70%
Scale in when CPU < 30%
🔹 Step 8: Monitoring & Alerts
Create CloudWatch alarm
Create SNS topic
Subscribe email for notifications

✅ Key Features
High availability
Automatic scaling
Load balancing
Real-time monitoring
Email alert system
📈 Benefits
Handles traffic spikes automatically
Improves reliability
Reduces downtime
Cost-efficient resource usage
🚀 Future Enhancements
Add CI/CD pipeline integration
Use Docker containers
Implement Kubernetes (EKS)
Add HTTPS with SSL certificate
Integrate monitoring dashboards (Grafana)

👨‍💻 Author

Harshavardhan
BCA Student | Aspiring Cloud & DevOps Engineer
