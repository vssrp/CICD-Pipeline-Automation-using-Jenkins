# CICD-Pipeline-Automation-using-Jenkins

## Overview
This project introduces **Continuous Integration (CI)** using **Jenkins**, automating the process of **code building, testing, and deployment**. CI ensures that merged code is immediately tested, preventing integration conflicts and improving software development efficiency.

## Challenges Addressed
- **Merged but not integrated:** Code merges often result in conflicts, bugs, and errors that delay development.
- **Manual Build & Deployment:** Developers manually handle code compilation and integration, leading to inefficiencies.
- **Integration Complexity:** Multiple developers pushing code leads to untested integrations.
- **Long Debugging Times:** Resolving conflicts manually takes significant time and halts progress.

## Jenkins-Based CI Solution
- **Automated Builds:** Jenkins triggers builds from Version Control Systems (VCS) like Git after every commit.
- **Pipeline as Code:** Uses **Jenkinsfile** to define stages in the CI/CD pipeline.
- **Extensible with Plugins:** Supports VCS, Build, Cloud, and Testing plugins.
- **Automated Testing:** Runs test cases before deployment.
- **Integration with Nexus:** Stores artifacts in a repository manager.

## Features
- **Open-source and Extensible** via plugins.
- **Supports Multiple OS Environments.**
- **Distributed Builds with Master/Slave Architecture.**
- **Pipeline as Code:** Uses **Declarative and Scripted Pipelines.**

## CI/CD Pipeline Overview
A typical **Jenkins pipeline** follows these stages:

```groovy
pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                // Build step
            }
        }
        stage('Test') { 
            steps {
                // Test step
            }
        }
        stage('Deploy') { 
            steps {
                // Deployment step
            }
        }
    }
}
```

## Jenkins Tools & Integrations
- **Version Control Systems (VCS):** Git, SVN.
- **Build Tools:** Maven, Ant.
- **Testing Tools:** SonarQube, OWASP Scanner.
- **Artifact Storage:** Nexus Repository Manager.
- **Infrastructure:** Docker, Kubernetes integration.

## Jenkins Master/Slave Architecture
- **Master Node:** Handles job scheduling and execution.
- **Slave Nodes:** Perform builds, testing, and deployments in distributed environments.
- **Supports Cross-Platform Builds:** Windows, Linux, macOS.

## Security & User Management
- **User Authentication:** Supports Jenkins database and LDAP.
- **Permissions & Roles:** Admin, Read, Jobs, Credentials, Plugins.
- **Job-Level Permissions:** View, Build, Delete, Configure.

## Automating Jenkins Jobs
- **Build Triggers:**
  - Trigger jobs remotely via API.
  - Execute builds after another job completes.
  - Scheduled jobs using Cron format.
  - Poll SCM for changes and trigger builds.
