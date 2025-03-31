# 🚀 **ICTG Task - The Ultimate DevOps Adventure!**

## **1️⃣ Project Name**  
_The ICTG Task - Where DevOps Magic Happens!_

---

## **2️⃣ Project Description**  
Ever dreamt of a Flask API so smooth it practically deploys itself? Well, dream no more! This project is a **Flask API** running on **AWS EC2** with a PostgreSQL database, all wrapped up in a DevOps masterpiece. We wield **Terraform** to provision infrastructure, **Docker** to containerize everything, and **GitHub Actions** to automate deployment like a true DevOps wizard! ⚡

---

## **3️⃣ Objective**  
Why did we embark on this journey? Simple:
✅ **CI/CD Automation** – Because manual deployments are so last decade.  
✅ **Infrastructure as Code** – Terraform makes provisioning feel like casting spells.  
✅ **Containerization** – Packing up Flask & PostgreSQL for maximum portability.  
✅ **AWS Deployment** – EC2 on a budget, because we’re smart like that.  

---

## **🛠 4️⃣ Tech Stack & Tools Used**
### **1️⃣ Infrastructure & Deployment**
🔹 **AWS EC2** → Where our app lives rent-free (for now).  
🔹 **Terraform** → The Infrastructure Overlord.  
🔹 **GitHub Actions** → The Automation Guru.  
🔹 **Docker & Docker Compose** → Containers for every occasion.  
🔹 **SSH (appleboy/ssh-action)** → Because secure deployments matter.  

### **2️⃣ Backend & Database**
🔹 **Flask** → Python’s favorite lightweight web framework.  
🔹 **PostgreSQL** → The chosen one for relational data.  

### **3️⃣ Version Control & Registry**
🔹 **Git & GitHub** → Our code’s forever home.  
🔹 **Docker Hub** → Storing container images like prized possessions.  

### **4️⃣ Security & Networking**
🔹 **IAM Roles & Policies** → Because security is 🔑.  
🔹 **Security Groups** → Keeping the bad guys out.  

---

## **📌 5️⃣ Project Setup & Installation Guide**
Brace yourself – here’s how to get everything up and running! 🔥

### **🛠 1️⃣ Prerequisites**
Before you dive in, ensure you have these installed:
**On Your Local Machine:**
✅ **Git** → Because version control is life.  
✅ **Docker & Docker Compose** → We containerize everything.  
✅ **Python 3.x & pip** → Flask needs love.  
✅ **Terraform** → Infrastructure as Code for the win!  
✅ **AWS CLI** → Managing AWS like a boss.  

**On AWS EC2 Instance:**
✅ **Ubuntu 22.04** (or latest stable version).  
✅ **Docker & Docker Compose installed.**  
✅ **PostgreSQL installed manually or via Docker.**  

---

## **📂 6️⃣ Cloning the Repositories**
Get the code on your local machine:
```bash
# Clone the main project repo
git clone https://github.com/DestinyObs/ictg_task.git
cd ictg_task

# Clone the Terraform automation repo
git clone https://github.com/DestinyObs/ictg_automate_v2.git
cd ictg_automate_v2
```

---

## **⚙️ 7️⃣ Setting Up Infrastructure on AWS (Terraform)**
Time to let Terraform do the heavy lifting! 💪

### **🔹 Steps to Deploy EC2 Instance with Terraform:**
```bash
# Navigate to the Terraform repo
cd ictg_automate_v2

# Initialize Terraform (one-time setup)
terraform init

# Validate the configuration
terraform validate

# Plan the infrastructure (Check what will be created)
terraform plan

# Apply and deploy the infrastructure
terraform apply -auto-approve
```
🔹 After execution, Terraform will output the EC2 instance details (IP, security settings, etc.).

---

## **🐳 8️⃣ Containerizing the Application (Docker Setup)**
Docker keeps our app running smoothly across environments! 🎯

### **🔹 Steps to Build and Run Locally:**
```bash
# Navigate to the project directory
cd ictg_task

# Build and start the containers using Docker Compose
docker-compose up --build -d

# Verify that the containers are running
docker ps
```

📌 **After this:**
✅ Backend should be accessible at **http://localhost:8000**  
✅ Frontend should be accessible at **http://localhost:5173**  

---

## **🚀 9️⃣ Deploying the Application to EC2**
Terraform sets up the server, but GitHub Actions takes care of deploying the app like a well-oiled machine. 🏗️

🔹 **Manual Deployment via SSH (Optional Alternative to CI/CD)**
```bash
# SSH into the EC2 instance
ssh -i your-key.pem ubuntu@<EC2_PUBLIC_IP>

# Pull the latest Docker images from Docker Hub
docker pull destinyobs/ictg_task-backend:latest
docker pull destinyobs/ictg_task-frontend:latest

# Run the application using Docker
docker-compose up -d
```

---

## **🎯 1️⃣0️⃣ Conclusion**
This project isn’t just another API deployment – it’s a full-fledged DevOps **masterpiece**! With Terraform automating infrastructure, Docker ensuring portability, and GitHub Actions streamlining CI/CD, this is **THE** way to deploy applications like a pro. 🚀

💡 Now go ahead, deploy, and let the DevOps magic unfold! ✨

