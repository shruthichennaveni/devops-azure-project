# 🚀 Azure DevOps Project using Terraform

## 📌 Overview

This project demonstrates an end-to-end deployment of a Python Flask application on Microsoft Azure using Terraform for infrastructure provisioning and NGINX as a reverse proxy.

---

## 🛠️ Tech Stack

* Terraform
* Microsoft Azure
* Linux (Ubuntu VM)
* Python (Flask)
* NGINX

---

## 🧱 Infrastructure Setup

Provisioned using Terraform:

* Resource Group
* Virtual Network (10.0.0.0/16)
* Subnet (10.0.1.0/24)
* Network Interface
* Linux Virtual Machine

---

## 🌐 Networking

* Public IP assigned to VM
* Network Security Group (NSG) configured:

  * Port 22 → SSH
  * Port 80 → Web traffic
  * Port 8080 → Application

---

## 🚀 Application Deployment

1. Connected to VM via SSH
2. Installed Python & dependencies
3. Created Flask application
4. Ran application on port 8080

---

## 🔁 NGINX Configuration

* Installed NGINX
* Configured reverse proxy to Flask app (port 8080)
* Restarted service

---

## 🌍 Output

Application accessible via:

http://<public-ip>

---

## ❗ Challenges & Fixes

### 1. Azure VM SKU Not Available

* Cause: Region capacity limitation
* Fix: Changed VM size/region

### 2. Terraform Dependency Issues

* Cause: Subnet not ready before NIC
* Fix: Used `depends_on`

### 3. GitHub Large File Error

* Cause: `.terraform` files pushed
* Fix: Cleaned Git history + added `.gitignore`

### 4. 502 Bad Gateway (NGINX)

* Cause: Flask app not running
* Fix: Restarted application using nohup

---

## 📚 Key Learnings

* Infrastructure as Code using Terraform
* Azure networking and security
* Debugging real-world cloud issues
* Reverse proxy setup using NGINX
* Git best practices (.gitignore, history cleanup)

---

## 🚀 Future Enhancements

* CI/CD pipeline using GitHub Actions
* Gunicorn for production deployment
* systemd service for app auto-start
* Monitoring using Azure Monitor

---

## 👩‍💻 Author

Shruthi
