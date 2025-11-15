# **🚀 Docker Course Content (Basic to Advanced)**

### *Perfect for DevOps, Cloud, and Microservices learners*

---

## **🔰 MODULE 1: Introduction to Docker (Basics)** 17-11-2025

### **1.1 What is Docker?**

* Why containerization?
* VM vs Containers
* Benefits of Docker in DevOps

### **1.2 Docker Architecture**

* Docker Engine
* Docker Daemon
* Docker CLI
* Docker Registry (Docker Hub, Private registry)
* Docker Objects (Images, Containers, Volumes, Networks)

### **1.3 Install & Setup Docker**

* Docker installation (Windows, Linux, Mac)
* Running first container: `docker run hello-world`
* Basic Docker commands

  * `docker ps`, `docker images`, `docker rm`, `docker rmi`

---

## **🔰 MODULE 2: Docker Images & Containers** 18-11-2025

### **2.1 Working with Docker Images**

* Pulling images
* Searching images
* Export/Import images
* Image layers & UnionFS

### **2.2 Building Your Own Images**

* Understanding **Dockerfile**
* Base image vs custom images
* Instructions overview

  * `FROM`, `RUN`, `COPY`, `ADD`, `EXPOSE`, `ENV`, `CMD`, `ENTRYPOINT`
* Multi-stage Dockerfile
* Best practices for writing Dockerfiles

### **2.3 Running Containers**

* Detached mode vs interactive mode
* Container lifecycle

  * start, stop, restart, pause, remove
* Logging inside containers
* Executing commands inside running containers

---

## **🔰 MODULE 3: Docker Storage** 19-11-2025

### **3.1 Docker Storage**

* Volume types:

  * Named Volume
  * Bind Mount
  * tmpfs mount
* Persistent storage
* Sharing data between containers

---

## **🔰 MODULE 4: Docker Storage & Networking** 20-11-2025

### **4.1 Docker Networking**

* Default networks: Bridge, Host, None
* Container-to-container communication
* Custom network creation
* Port mapping & exposing services
* DNS inside Docker

---

## **🔰 MODULE 5: Docker Compose (Multi-container Applications)** 21-11-2025

### **5.1 Introduction to Docker Compose**

* Why Compose?
* Use cases in real projects

### **5.2 docker-compose.yml**

* Services
* Environment variables
* Networks & volumes
* Dependencies between containers

### **5.3 Deploy Multi-container App**

* Sample project:

  * **Nginx + Python/NodeJS App + MySQL/PostgreSQL**
* Scaling services
* Compose commands

---

## **🔰 MODULE 6: Docker Registry & Image Management** 22-11-2025

### **6.1 Docker Hub**

* Tagging images
* Pushing & pulling images
* Private repositories

### **6.2 Private Docker Registry**

* Setup & configure
* Login and push images

### **6.3 Artifact Registries**

* AWS ECR
* Azure ACR
* GCP GAR/GCR

---

## **🔰 MODULE 7: Docker Security (Intermediate → Advanced)** 23-11-2025

### **7.1 Security Best Practices**

* Avoid root user
* Reduce image size
* Scan images for vulnerabilities

### **7.2 Secrets Management**

* Environment variables
* Docker secrets
* External secret stores (Vault, AWS Secrets Manager)

---

## **🔰 MODULE 8: Docker in CI/CD Pipelines** 24-11-2025

### **8.1 Docker with GitHub Actions** 24-11-2025

* Build & publish images from pipeline
* Automated versioning

### **8.2 Deploy & Test Containers in CI/CD** 24-11-2025

* Testing containerized apps
* Blue-green deployment
* Canary releases

### **8.3 Docker with Jenkins** 25-11-2025

* Build & publish images from pipeline
* Automated versioning

### **8.4 Deploy & Test Containers in CI/CD** 25-11-2025

* Testing containerized apps
* Blue-green deployment
* Canary releases

---

## **🔰 MODULE 9: Docker Swarm (Orchestration Beginner)** 26-11-2025

### **9.1 What is Swarm?**

* Need for orchestration
* Kubernetes vs Swarm

### **9.2 Swarm Cluster Setup**

* Manager & worker nodes
* Deploying services
* Scaling & load balancing

### **9.3 Rolling updates**

---

## **🔰 MODULE 10: Advanced Docker Concepts** 27-11-2025 & 28-11-2025

### **10.1 Resource Limits** 27-11-2025

* CPU & Memory limits
* Control groups (cgroups)

### **10.2 Namespaces** 27-11-2025

* Process isolation
* Network & storage namespaces

### **10.3 Multi-stage Builds** 28-11-2025

* Optimizing image size

### **10.4 Docker Internals** 28-11-2025

* Layering
* Overlay filesystem
* Garbage collection

---

## **🔰 MODULE 11: Real-time DevOps Projects** 29-11-2025 & 30-11-2025

### **11.1 Dockerizing Real Applications**

* Dockerize Java, Python, Node, .NET apps
* Dockerize microservices architecture

### **11.2 Docker with Kubernetes**

* Convert Docker Compose to Kubernetes YAML
* Workloads, Services, Ingress

---

## **🔰 MODULE 12: Monitoring (Advanced)**

* Prometheus + Grafana with Docker
* Logging using ELK 



++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

## **🔰 MODULE 12: Capstone Projects (Advanced)**

### **Project 1:** Deploy Full Stack App on Docker

### **Project 2:** Create CI/CD pipeline with Docker + Jenkins

### **Project 3:** Multi-container app with DB, cache, web

### **Project 4:** Setup private Docker Registry + Security scanning with Trivy

---

