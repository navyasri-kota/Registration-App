# 🚀 Jenkins CI/CD Pipeline Using Docker

## 📌 Project Overview

This project demonstrates the implementation of a **Continuous Integration and Continuous Deployment (CI/CD)** pipeline using **Jenkins** and **Docker** for a Java web application.

The pipeline automatically builds and deploys the application whenever code is pushed to GitHub, reducing manual effort and ensuring faster, reliable deployments.

---

## 🎯 Objectives

- Automate software build and deployment
- Integrate GitHub with Jenkins
- Containerize the application using Docker
- Deploy the application on Apache Tomcat
- Reduce deployment time and manual errors
- Demonstrate DevOps CI/CD workflow

---

## 🛠️ Technologies Used

- Java
- Maven
- Git
- GitHub
- Jenkins
- Docker
- Apache Tomcat
- Ubuntu Linux
- SSH
- AWS EC2

---

## 📂 Project Structure

```
Registration-App/
│── webapp/
│── Dockerfile
│── Jenkinsfile (if available)
│── pom.xml
│── README.md
```

---

## ⚙️ CI/CD Workflow

1. Developer pushes code to GitHub.
2. Jenkins detects changes using Poll SCM/Webhook.
3. Jenkins clones the latest source code.
4. Maven builds the project.
5. Docker creates a new image.
6. Existing container is stopped and removed.
7. A new Docker container is started.
8. Application is deployed on Apache Tomcat.
9. Users access the application through a web browser.

---

## 🔄 Pipeline Flow

```
Developer
      │
      ▼
 GitHub Repository
      │
      ▼
 Jenkins Pipeline
      │
      ▼
 Maven Build
      │
      ▼
 Docker Image
      │
      ▼
 Docker Container
      │
      ▼
 Apache Tomcat
      │
      ▼
 Web Application
```

---

## 🐳 Docker Commands

Build Docker Image

```bash
docker build -t webapp:v1 .
```

Run Container

```bash
docker run -d --name Registration-App -p 8086:8080 webapp:v1
```

Stop Container

```bash
docker stop Registration-App
```

Remove Container

```bash
docker rm Registration-App
```

Check Running Containers

```bash
docker ps
```

---

## 🔧 Jenkins Build Commands

```bash
mvn clean package

docker build -t webapp:v1 .

docker stop Registration-App || true

docker rm Registration-App || true

docker run -d --name Registration-App -p 8086:8080 webapp:v1
```

---

## ▶️ How to Run

### Clone Repository

```bash
git clone https://github.com/navyasri-kota/Registration-App.git
```

### Move into Project

```bash
cd Registration-App
```

### Build Project

```bash
mvn clean package
```

### Build Docker Image

```bash
docker build -t webapp:v1 .
```

### Run Docker Container

```bash
docker run -d --name Registration-App -p 8086:8080 webapp:v1
```

### Open Browser

```
http://<EC2-Public-IP>:8086/Registration-App
```

---

## ✨ Features

- Automated CI/CD Pipeline
- GitHub Integration
- Docker Containerization
- Automated Deployment
- Apache Tomcat Hosting
- Reduced Manual Deployment
- Faster Software Delivery
- Consistent Runtime Environment

---

## 📊 Results

- Successfully automated the build process.
- Integrated GitHub with Jenkins.
- Created Docker images automatically.
- Deployed application inside Docker container.
- Hosted application using Apache Tomcat.
- Reduced deployment time.
- Improved deployment reliability.
- Demonstrated real-world DevOps practices.

---

## 👨‍💻 Team Members

- Kota Navya Sri
- Mekala Pavan Kalyan
- Gullapalli Aparna
- Patapati Sai Abhishek
- Kattamuri Rishitha Indira Lakshmi

---

## 📚 Future Enhancements

- Jenkins Pipeline as Code
- Automated Unit Testing
- Kubernetes Deployment
- AWS ECS/EKS Deployment
- Monitoring using Prometheus & Grafana
- Notifications using Slack/Email

itory.
