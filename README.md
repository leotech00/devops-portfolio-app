# DevOps Project: Automated CI/CD Pipeline for a 2-Tier Flask Application on AWS

**Author:** Leornard Ngubeni
**Date:** March 2026

---

## Project Overview

This project demonstrates the deployment of a 2-tier web application (Flask + MySQL) on an AWS EC2 instance. The application is containerised using Docker and Docker Compose. A fully automated CI/CD pipeline is established using Jenkins to automatically build and deploy the application whenever new code is pushed to GitHub.

---

## Tech Stack

- **Cloud:** AWS EC2
- **Containerisation:** Docker, Docker Compose
- **CI/CD:** Jenkins
- **Backend:** Python, Flask
- **Database:** MySQL
- **Version Control:** Git, GitHub
- **OS:** Ubuntu 24.04

---

## Architecture
```
+-----------------+      +----------------------+      +-----------------------------+
|   Developer     |----->|     GitHub Repo      |----->|        Jenkins Server       |
| (pushes code)   |      | (Source Code Mgmt)   |      |  (on AWS EC2)               |
+-----------------+      +----------------------+      |                             |
                                                       | 1. Clones Repo              |
                                                       | 2. Builds Docker Image      |
                                                       | 3. Runs Docker Compose      |
                                                       +--------------+--------------+
                                                                      |
                                                                      v
                                                       +-----------------------------+
                                                       |      Application Server     |
                                                       |      (Same AWS EC2)         |
                                                       |                             |
                                                       | +-------------------------+ |
                                                       | | Docker Container: Flask | |
                                                       | +-------------------------+ |
                                                       |              |              |
                                                       |              v              |
                                                       | +-------------------------+ |
                                                       | | Docker Container: MySQL | |
                                                       | +-------------------------+ |
                                                       +-----------------------------+
```

---

## What I Built

- Launched and configured an **AWS EC2** instance with proper security groups
- Installed and configured **Docker** and **Docker Compose** for containerisation
- Set up **Jenkins** as a CI/CD server to automate deployments
- Built a **Flask + MySQL** two-tier web application
- Created a **Jenkinsfile** to define the pipeline as code
- Automated the full build and deploy process on every GitHub push

---

## How to Run

1. Clone the repo:
```bash
git clone https://github.com/leotech00/devops-portfolio-app.git
```

2. Deploy with Docker Compose:
```bash
docker compose up -d --build
```

3. Access the app at `http://localhost:5000`

---

## Author

**Leornard Ngubeni** — BSc Information Technology Graduate  
- GitHub: [github.com/leotech00](https://github.com/leotech00)  
- LinkedIn: [linkedin.com/in/leornard-ngubeni-3783b7287](https://www.linkedin.com/in/leornard-ngubeni-3783b7287/)  
- Email: Leonarduniverse2@gmail.com