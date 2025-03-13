## **2️⃣ AWS Global Infrastructure (Regions & Availability Zones)**
AWS is designed to provide **high availability & low latency** using **Regions** and **Availability Zones (AZs)**.

✅ **AWS Regions**  
   - A **geographical area** with multiple data centers.  
   - Examples: `us-east-1` (Virginia), `ap-south-1` (Mumbai).  
   - AWS has **30+ regions worldwide**.  

✅ **Availability Zones (AZs)**  
   - A region consists of **multiple AZs** (separate data centers).  
   - Example: `us-east-1a`, `us-east-1b`, `us-east-1c` are different AZs in **us-east-1** region.  
   - Ensures **fault tolerance**—if one AZ fails, others keep running.  

✅ **AWS Edge Locations & Content Delivery**  
   - Used for **faster content delivery** via **AWS CloudFront (CDN)**.  
   - Example: A user in India gets content from the nearest AWS Edge Location instead of the US.  

---

Now that you understand the **prerequisites**, let's dive into **AWS EC2 (Elastic Compute Cloud)** step by step.
---

## **1️⃣ Introduction to AWS EC2**  
✅ **What is AWS EC2?**  
   - Amazon EC2 provides **scalable virtual servers (instances)** in the cloud.  
   - You can launch, configure, and manage virtual machines with full control.  
   - EC2 replaces traditional physical servers with **on-demand, pay-as-you-go** infrastructure.  

✅ **Key EC2 Concepts:**  
   - **Instances** → Virtual machines running on AWS.  
   - **Amazon Machine Image (AMI)** → Pre-configured OS + software.  
   - **Instance Types** → Different configurations for compute, memory, storage, and networking.  
   - **Elastic Block Store (EBS)** → Persistent storage for EC2.  
   - **Security Groups** → Firewall rules for EC2.  
   - **Key Pairs** → Used for SSH access.  
---

## **2️⃣ Setting Up Your First EC2 Instance**  
✅ **Step 1: Login to AWS Console**  
   - Go to **AWS Management Console** → Navigate to **EC2 Dashboard**.  

✅ **Step 2: Launch an EC2 Instance**  
   - Click **"Launch Instance"**.  
   - Choose an **Amazon Machine Image (AMI)** (e.g., Amazon Linux, Ubuntu, Windows Server).  
   - Select an **Instance Type** (e.g., `t2.micro` for free tier).  
   - Configure instance details (e.g., number of instances, networking settings).  
   - Add **storage (EBS volumes)**.  
   - Configure **Security Groups** (open ports like `22` for SSH, `80` for HTTP).  
   - Choose **Key Pair** (download `.pem` file for SSH access).  
   - Click **"Launch"**! 🚀  

✅ **Step 3: Connect to the EC2 Instance**  
   - **For Linux EC2 Instance:**  
     ```bash
     ssh -i my-key.pem ec2-user@public-ip
     ```
   - **For Windows EC2 Instance:**  
     - Use **RDP (Remote Desktop Protocol)** to connect.  

✅ **Step 4: Install Software & Manage EC2**  
   - Use `yum` or `apt` to install software on Linux instances.  
   - Configure security settings, firewall rules, and updates.  

---

## **3️⃣ EC2 Storage Options**  
✅ **Elastic Block Store (EBS)**  
   - Persistent storage attached to EC2 instances.  
   - Types: **gp3 (general-purpose), io1/io2 (high-performance), st1/sc1 (cost-efficient)**.  

✅ **Amazon S3 (Simple Storage Service)**  
   - Object storage for **images, backups, and large files**.  

✅ **Instance Store**  
   - Temporary storage that **resets on instance stop/restart**.  

✅ **EFS (Elastic File System)**  
   - Shared storage across multiple EC2 instances.  

---

## **4️⃣ EC2 Security & Networking**  
✅ **Security Groups**  
   - Control **inbound and outbound traffic**.  
   - Example: Open port `22` for SSH, `80` for HTTP.  

✅ **IAM Roles for EC2**  
   - Manage AWS access **without storing credentials**.  
   - Example: Allow an EC2 instance to access **S3, DynamoDB, or RDS**.  

✅ **Elastic IP**  
   - A **static public IP** for EC2.  

✅ **Load Balancing with ELB (Elastic Load Balancer)**  
   - Distributes traffic to multiple instances.  

✅ **Auto Scaling**  
   - Dynamically **adds or removes instances** based on demand.  

---

## **5️⃣ Advanced EC2 Features**  
✅ **Spot Instances** → Cheap, temporary instances (good for batch processing).  
✅ **Reserved Instances** → Discounted instances for long-term workloads.  
✅ **Dedicated Hosts** → Full physical server for compliance needs.  
✅ **AWS EC2 Auto Recovery** → Automatically restarts failed instances.  
✅ **EC2 Instance Connect** → Browser-based SSH for Linux instances.  

---
✅ **Attach an EBS volume & mount it**.  
✅ **Set up EC2 Auto Scaling & Load Balancing**.  
✅ **Use IAM roles & security best practices** (disable root login, enable MFA).  
✅ **Monitor EC2 with CloudWatch**.  

---
