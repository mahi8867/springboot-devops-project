# 🚀 SpringBoot DevOps CI/CD Pipeline



![Java](https://img.shields.io/badge/Java-SpringBoot-brightgreen)




![Jenkins](https://img.shields.io/badge/CI%2FCD-Jenkins-red)




![Docker](https://img.shields.io/badge/Container-Docker-blue)




![DockerHub](https://img.shields.io/badge/Registry-DockerHub-blue)




![AWS](https://img.shields.io/badge/Cloud-AWS%20EC2-orange)



---

## 📌 About This Project

This project demonstrates a **complete CI/CD pipeline** for a Java SpringBoot application.  
The application is automatically built using **Jenkins**, containerized using **Docker**,  
and deployed on **AWS EC2** cloud infrastructure.

---

## 🏗️ CI/CD Pipeline Architecture
---

## 🛠️ Tech Stack

| Tool        | Purpose                            |
|-------------|------------------------------------|
| SpringBoot  | Java Web Application Framework     |
| Maven       | Build Tool (compile + package)     |
| Jenkins     | CI/CD Automation Server            |
| Docker      | Containerization                   |
| DockerHub   | Docker Image Registry              |
| AWS EC2     | Cloud Server for Deployment        |
| GitHub      | Source Code Management             |

---

## 📁 Project Structure
---

## 🐳 Dockerfile Overview

The Dockerfile:
- Uses an official Java base image
- Copies the built JAR file into the container
- Exposes the application port
- Runs the SpringBoot application

---

## ⚙️ Jenkins Pipeline Steps

1. **Clone** — Jenkins pulls latest code from GitHub
2. **Build** — Maven compiles and packages the app (`mvn clean package`)
3. **Docker Build** — Jenkins builds Docker image from Dockerfile
4. **Docker Push** — Image is pushed to DockerHub registry
5. **Deploy** — Container is run on AWS EC2 instance

---

## 🚀 How to Run This Project Locally

### Prerequisites
- Java 11+
- Maven
- Docker

### Steps

```bash
# Step 1: Clone the repository
git clone https://github.com/mahi8867/springboot-devops-project.git
cd springboot-devops-project

# Step 2: Build the JAR using Maven
mvn clean package

# Step 3: Build Docker image
docker build -t springboot-app .

# Step 4: Run the container
docker run -d -p 8080:8080 springboot-app

# Step 5: Access the application
# Open browser → http://localhost:8080

