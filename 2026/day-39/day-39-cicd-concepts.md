#  Day 39 – What is CI/CD?

##  Task
Understand why CI/CD exists and how it works before writing pipelines.

---

##  Task 1: The Problem

###  What can go wrong?

- Code conflicts between developers  
- Manual deployment errors  
- Bugs reaching production  
- No proper testing before release  
- Version inconsistency  

---

###  "It works on my machine"

- Code works locally but fails in other environments  
- Due to different dependencies, configs, or OS  
- CI/CD solves this by running code in a standard environment  

---

###  Manual Deployment Limit

- Safe deployments: 1–2 times/day (max)  
- Risk increases with frequency  
- Errors are hard to track and rollback  

---

##  Task 2: CI vs CD

### 🔹 Continuous Integration (CI)
- Developers frequently push code to a shared repo  
- Automated build + test runs on each push  
- Catches bugs early  

Example: Push code → tests run automatically  

---

### 🔹 Continuous Delivery (CD)
- Code is always in a deployable state  
- Deployment is manual but ready anytime  

Example: Build passes → ready for production deployment  

---

### 🔹 Continuous Deployment
- Fully automated deployment to production  
- No manual approval  

Example: Push → test → auto deploy to production  

---

##  Task 3: Pipeline Anatomy

- Trigger → Starts pipeline (push/PR)
- Stage → Phase (build, test, deploy)
- Job → Group of steps
- Step → Single command
- Runner → Machine executing jobs
- Artifact → Output (build, logs, image)

---

##  Task 4: Pipeline Diagram

```
Developer Push (GitHub)
        ↓
   Build Stage
        ↓
   Test Stage
        ↓
   Docker Build
        ↓
   Deploy to Staging
```
---

##  Task 5: GitHub Research

Repo: https://github.com/tiangolo/fastapi  

- Trigger: push & pull request  
- Jobs: lint, test, build  
- Purpose: validate code before merge  

---

##  Key Learnings

- CI/CD is a process, not a tool  
- Automates build, test, deploy  
- Reduces errors  
- Enables fast delivery  

---

