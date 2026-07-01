# i2i Academy - Spring Boot Assignment 

This repository contains the production-ready Java Spring Boot backend service initialized and deployed as part of the i2i Academy technical engineering coursework.

---

## 🛠️ Tech Stack & Environment
* **Language:** Java 26 (OpenJDK 26.0.1)
* **Framework:** Spring Boot 3.4.3
* **Build Tool:** Apache Maven 3.9.16
* **Cloud Infrastructure:** Google Cloud Platform (GCP) Compute Engine
* **Container Port:** 8080 (HTTP)

---

## 🚀 Key Architectural Concepts Explained

### 1. Spring Boot & Opinionated Defaults
Spring Boot eliminates the complex, boilerplate XML configurations of traditional Spring ecosystems by implementing **Opinionated Defaults**. It pre-configures embedded servers (like Apache Tomcat 11) and foundational libraries automatically, allowing engineers to focus solely on business logic rather than infrastructure management.

### 2. The Role of `pom.xml`
The Project Object Model (`pom.xml`) acts as the configuration centerpiece for Maven. It explicitly declares external project dependencies (such as `spring-boot-starter-web`), controls global plugin orchestrations, and targets the native Java compilation environment (Java 26).

---

## 🏃‍♂️ Local Development Execution
To compile and spin up the microservice locally:
```bash
mvn spring-boot:run
```
Once initialized, the REST endpoint can be consumed at: http://localhost:8080

☁️ Cloud Deployment Setup (GCP)
The application is deployed on a Google Cloud Platform (GCP) Compute Engine Virtual Machine running Ubuntu 24.04 LTS.

Inbound Firewall Configuration
To expose the microservice to the public web, the GCP VPC firewall structure has been adjusted with the following network rule:

Target: All instances in the network

Source IP Filter: 0.0.0.0/0 (Any IPv4)

Protocol & Ports: tcp:8080

🛜 Production REST Endpoint
The live REST interface exposed on the cloud infrastructure returns the mandatory academy greeting string:

Endpoint: GET /

Response: "Welcome to i2i Academy!"


---
