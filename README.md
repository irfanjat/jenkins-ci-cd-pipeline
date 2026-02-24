# ☕ Java Maven CI Pipeline with Jenkins

> Automating build, test, and reporting for a Java application using Jenkins CI and Maven.

---

## 📌 Overview

This project demonstrates a **Java Maven application integrated with a Jenkins CI pipeline**. Whenever code is pushed to GitHub, Jenkins automatically pulls the latest source, builds the application with Maven, runs unit tests, and generates a build report — showcasing real-world **Continuous Integration (CI)** best practices.

---

## 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| **Java** | Application programming language |
| **Maven** | Build automation and dependency management |
| **Jenkins** | CI pipeline orchestration |
| **GitHub** | Version control and source trigger |
| **JUnit** | Unit testing framework |

---

## 📁 Project Structure

```
java-maven-ci/
│
├── src/
│   ├── main/
│   │   └── java/
│   │       └── App.java          # Main application (Hello World)
│   └── test/
│       └── java/
│           └── AppTest.java      # JUnit unit tests
├── pom.xml                       # Maven project configuration
├── Jenkinsfile                   # Jenkins pipeline definition
└── README.md                     # Project documentation
```

---

## ⚙️ How It Works

```
Developer Pushes Code to GitHub
            ↓
   Jenkins Detects the Commit
            ↓
   Maven Pulls Dependencies
            ↓
     Maven Builds the App
            ↓
      JUnit Tests Execute
            ↓
  Build Status Report Generated
            ↓
   Results Visible on Jenkins Dashboard
```

### What the Jenkins Pipeline Does

1. **Pulls** the latest source code from GitHub
2. **Builds** the application using `mvn clean package`
3. **Runs** all JUnit unit tests automatically
4. **Generates** test reports viewable in the Jenkins dashboard
5. **Reports** build success or failure with detailed logs

---

## 🚀 How to Run Locally

### Prerequisites

- [ ] Java JDK installed (`java -version`)
- [ ] Apache Maven installed (`mvn -version`)

### Build the Application

```bash
mvn clean package
```

### Run the Application

```bash
java -jar target/*.jar
```

Expected output:

```
Hello World!
```

### Run Tests Only

```bash
mvn test
```

---

## 🔄 Jenkins Setup

### Prerequisites

- [ ] Jenkins installed and running (port `8080`)
- [ ] Java & Maven configured in Jenkins Global Tool Configuration
- [ ] GitHub repository connected via webhook or polling

### Steps

1. Create a **New Pipeline** job in Jenkins
2. Point it to your GitHub repository
3. Set the pipeline script path to `Jenkinsfile`
4. Enable **GitHub webhook** or **Poll SCM** as the build trigger
5. Click **Build Now** to run the first pipeline

> From this point, every `git push` will automatically trigger the pipeline.

---

## 📊 Test Reports

JUnit test results are generated automatically during every Jenkins build and are accessible directly in the Jenkins dashboard under:

```
Jenkins Job → Build History → Test Results
```

| Report Type | Location |
|---|---|
| JUnit XML Report | `target/surefire-reports/` |
| Jenkins Test View | Jenkins Dashboard → Build → Test Results |

---

## 🧠 Key Learnings

- Creating and managing **Jenkins pipelines** using `Jenkinsfile`
- Automating **Maven builds** in a CI environment
- Running and reporting **JUnit unit tests** through Jenkins
- Understanding **CI workflows** used in real-world DevOps pipelines
- Integrating **GitHub with Jenkins** via webhooks for automatic triggers

---

## 🎯 Future Improvements

- [ ] Add a **Docker build stage** to containerize the application
- [ ] Integrate **SonarQube** for static code quality analysis
- [ ] Extend to a full **CI/CD pipeline** with automated deployment
- [ ] Add **Slack/email notifications** on build success or failure
- [ ] Implement **multi-branch pipeline** support for feature branches

---

## 👨‍💻 Author

**Irfan Ali** — Aspiring DevOps Engineer

[![GitHub](https://img.shields.io/badge/GitHub-irfanjat-181717?style=flat&logo=github)](https://github.com/irfanjat)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-irfanjat-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/irfanjat/)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<p align="center">⭐ If you found this project helpful, please consider starring the repository!</p>
<p align="center">Made with ❤️ by <a href="https://github.com/irfanjat">Irfan Ali</a></p>
