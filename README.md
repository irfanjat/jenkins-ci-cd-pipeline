# 🚀 Java Maven CI Pipeline with Jenkins

This repository contains a **Java Maven application integrated with a Jenkins CI pipeline**.
The project demonstrates how to automate build and test processes using Jenkins
whenever code is pushed to GitHub.

This is a hands-on DevOps project focused on **Continuous Integration (CI)** best practices.!

---

## 🔧 Tech Stack
- Java
- Maven
- Jenkins
- GitHub
- JUnit

---

## 📦 Project Overview
The application is a simple Java program that prints **"Hello World!"**
and includes unit tests to verify application behavior.

The Jenkins pipeline automatically:
- Pulls source code from GitHub
- Builds the application using Maven
- Runs unit tests
- Generates test reports

---

## 🔄 CI Pipeline Flow

```text
GitHub Commit
     ↓
Jenkins Trigger
     ↓
Maven Build
     ↓
Unit Tests
     ↓
Build Status Report

▶️ How to Run Locally

Make sure Java and Maven are installed:

mvn clean package


Run the application:

java -jar target/*.jar

📊 Test Reports

JUnit test results are generated automatically during the Jenkins build
and can be viewed directly in the Jenkins dashboard.

🎯 Learning Outcomes

Creating Jenkins pipelines using Jenkinsfile

Automating Maven builds

Running unit tests in CI

Understanding CI workflows in real-world DevOps environments

📌 Future Improvements

Add Docker build stage

Integrate SonarQube for code quality

Extend CI to full CI/CD with deployment
