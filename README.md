## 📂 Projects

### 🚀 Ansible, Jenkins, and Docker Automation Project

This capstone project demonstrates end-to-end automation using **Ansible**, **Jenkins**, **Docker**, and **GitHub** across three Ubuntu EC2 instances: **Master**, **Test**, and **Production**. The project handles software installation, Jenkins agent setup, CI/CD pipeline automation, and Dockerized web app deployment.

#### 🔧 Tools & Technologies:
- AWS EC2
- Ansible
- Jenkins
- Docker
- GitHub
- Ubuntu Server 22.04

#### 🛠️ Key Features:
- Provisioned 3 EC2 Ubuntu servers (Master, Test, Production)
- Automated software installation using Ansible playbooks
- Installed and configured Jenkins on Master, set up Test and Prod as Jenkins agents
- CI/CD Pipeline:
  - Build Docker images on code push to **master** or **develop**
  - Deploy to Test environment (port 82/83)
  - Auto-trigger final release to Production (port 80)
- Used GitHub webhooks to automate build triggers

#### 📦 CI/CD Workflow:
- `Job 1: mastertesting_82`: On `master` branch push → Build Docker image → Deploy to **Test** (port 82)
- `Job 2: testingdevelop_83`: On `develop` branch push → Build & deploy to **Test** (port 83)
- `Job 3: finalrelease`: Auto-triggered post-success of Job 1 → Deploys to **Production** (port 80)

#### 🔗 GitHub Repository:
[🔗 Project Repo](https://github.com/ajithpethanan/website)


