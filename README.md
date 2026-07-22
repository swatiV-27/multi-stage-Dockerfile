# How DevOps Changed the IT World

A web application that explains how DevOps transformed modern software development and IT operations. The application is containerized using a Docker Multi-Stage Build with Node.js as the build stage and Nginx as the production stage.

## Project Overview

This project demonstrates:

* Docker Multi-Stage Builds
* Node.js Build Environment
* Nginx Web Server
* Static Website Hosting
* Container Optimization
* DevOps Concepts and Tools

The website provides information about:

* DevOps Evolution
* CI/CD
* Docker
* Kubernetes
* Terraform
* Jenkins
* AWS
* Modern Software Delivery Practices

---

## Project Structure

```text
devops-world-project/
│
├── src/
│   ├── index.html
│   ├── style.css
│   └── app.js
│
├── Dockerfile
├── nginx.conf
├── package.json
├── .dockerignore
└── README.md
```

---

## Architecture

```text
Developer
    │
    ▼
Node.js Build Stage
    │
    ▼
Docker Multi-Stage Build
    │
    ▼
Nginx Runtime Container
    │
    ▼
Web Browser
```

---

## Multi-Stage Docker Build

### Stage 1 – Builder

* Uses Node.js image
* Installs dependencies
* Builds the application
* Generates static files

### Stage 2 – Production

* Uses lightweight Nginx image
* Copies only build artifacts
* Serves the application on port 80

Benefits:

* Smaller image size
* Faster deployments
* Improved security
* Reduced attack surface

---

## Build Docker Image

```bash
docker build -t devops-info:v1 .
```

---

## Run Container

```bash
docker run -d -p 80:80 --name devops-app devops-info:v1
```

---

## Verify Running Container

```bash
docker ps
```

---

## Access Application

Local Environment:

```text
http://localhost
```

AWS EC2:

```text
http://<EC2-Public-IP>
```

---

## Technologies Used

* HTML
* CSS
* JavaScript
* Node.js
* Nginx
* Docker

---

## Future Enhancements

* Jenkins CI/CD Pipeline
* GitHub Webhooks
* Docker Hub Integration
* Kubernetes Deployment
* Terraform Infrastructure Provisioning
* AWS EC2 Automation
* Monitoring with Prometheus and Grafana

---

## Author

Swati Verma

DevOps Engineer
