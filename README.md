# 🧱 Tier 1: Webserver Layer – AWS Serverless 3-Tier Architecture

This repository documents the **first layer** of a fully **serverless 3-tier AWS architecture** for hosting a dynamic, containerized e-commerce web application.

---

## 📌 Overview

**Tier 1** serves as the **Webserver Layer**—the main entry point for user traffic. It's designed to be secure, highly available, and scalable, without the overhead of managing traditional web servers.

---

## 🧭 Architecture Components

| Component                      | Purpose                                                    |
|-------------------------------|------------------------------------------------------------|
| **Amazon Route 53**           | Domain name system routing and traffic distribution        |
| **AWS WAF**                   | Web application firewall to protect against common exploits |
| **Application Load Balancer** | Distributes traffic across two Availability Zones          |
| **Dockerized Web App**        | Front-end hosted in containers behind the ALB              |
| **HTTPS / TLS**               | Ensures secure traffic to the application                  |

---

## 🌎 Region & Availability

- **Region:** `us-east-1 (N. Virginia)`
- **Availability Zones:** 2 (for high availability)
- **Subnets:** Public subnets only in this tier

---

## 📂 Folder Structure


---

## 🔐 Security Considerations

- **AWS WAF** is configured with AWS-managed rule sets (SQLi, XSS, etc.)
- **HTTPS** termination is handled at the ALB
- **Least privilege IAM roles** should be used across all layers

---

## 🚧 Next Layer

Next week: [Tier 2 – Application Layer](../Tier2-Application-Layer/README.md)  
This is where we’ll host the business logic, APIs, and core services that power the front end.






