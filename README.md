# 🔄 QA Automation CI/CD Pipeline

## 📌 Project Overview

This project demonstrates the implementation of a **Continuous Integration and Continuous Deployment (CI/CD) pipeline** using **GitHub Actions** to automatically execute QA automation workflows.

The purpose of this project is to integrate automated testing into the software development lifecycle, ensuring that quality checks can be executed automatically whenever changes are pushed to the repository.

This project is part of my **QA Automation Portfolio**, showcasing practical experience with:

- Version control using Git and GitHub
- CI/CD pipeline implementation
- Automated test execution
- Workflow configuration using YAML
- QA automation best practices

---

# 🎯 Project Objectives

The main objectives of this project are:

- Create and configure a CI/CD pipeline using GitHub Actions.
- Automate the execution of QA testing workflows.
- Connect a GitHub repository with automated processes.
- Configure workflow execution through YAML files.
- Validate successful pipeline execution using GitHub Actions.
- Understand how automation integrates into modern software development practices.

---

# 🛠️ Technologies & Tools

| Technology | Purpose |
|---|---|
| Git | Version control system |
| GitHub | Repository hosting and collaboration platform |
| GitHub Actions | CI/CD automation platform |
| YAML | Workflow configuration language |
| Node.js | Runtime environment for automation tools |
| npm | Package manager for project dependencies |
| Playwright | Test automation framework integration |

---

## 📂 Project Structure

```text
QA_Automation_CI_CD
│
├── .github
│   └── workflows
│       ├── execute-playwright.yml
│       └── execute-k6.yml
│
└── README.md
```

### 🔄 Workflows Description

Each workflow includes:

```text
.github/workflows
│
├── execute-playwright.yml
│   → Triggers the Playwright automation test workflow from the remote repository.
│
└── execute-k6.yml
    → Triggers the k6 performance testing workflow from the remote repository.
```
---

# ⚙️ CI/CD Pipeline Workflow

The GitHub Actions pipeline automates the execution process by following these steps:

## 1️⃣ Trigger Pipeline

The workflow is triggered automatically when changes are pushed to the `main` branch.

Example:

```yaml
on:
  push:
    branches:
      - main
```

---

## 2️⃣ Setup Environment

GitHub Actions creates a virtual machine environment using Ubuntu.

The pipeline prepares the required environment to execute automated tests.

Example:

```yaml
runs-on: ubuntu-latest
```

---

## 3️⃣ Checkout Repository

The repository code is downloaded into the GitHub Actions runner.

Example:

```yaml
- name: Checkout Repository
  uses: actions/checkout@v4
```

---

## 4️⃣ Install Dependencies

The required project dependencies are installed using npm.

Example:

```yaml
- name: Install Dependencies
  run: npm install
```

---

## 5️⃣ Execute Automated Tests

The Playwright test suite is executed automatically.

Example:

```yaml
- name: Run Tests
  run: npx playwright test
```

---

## 6️⃣ Generate Execution Results

After execution, GitHub Actions provides:

- Pipeline status
- Test execution results
- Error details in case of failure
- Execution history

---

# 🚀 GitHub Actions Workflow Configuration

Example workflow file:

`.github/workflows/playwright.yml`

```yaml
name: Playwright Tests

on:
  push:
    branches:
      - main

jobs:

  test:

    runs-on: ubuntu-latest

    steps:

      - name: Checkout Repository
        uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 20

      - name: Install Dependencies
        run: npm install

      - name: Install Playwright Browsers
        run: npx playwright install --with-deps

      - name: Run Playwright Tests
        run: npx playwright test
```

---

# 🔄 CI/CD Process Flow

```text
Developer Push
      |
      ↓
GitHub Repository
      |
      ↓
GitHub Actions Trigger
      |
      ↓
Environment Setup
      |
      ↓
Install Dependencies
      |
      ↓
Execute Automated Tests
      |
      ↓
Generate Test Results
      |
      ↓
Pipeline Status Report
```

---

# ✅ Project Results

The CI/CD pipeline was successfully implemented and validated.

Achievements:

✔ GitHub repository connected with GitHub Actions  
✔ Automated workflow created using YAML  
✔ QA automation execution integrated into CI/CD  
✔ Successful pipeline execution verified through GitHub Actions  
✔ Improved understanding of continuous integration practices  

---

# 📸 Execution Evidence

The workflow execution can be verified from the GitHub Actions section.

Example validation:

✅ Workflow completed successfully  
✅ Pipeline status: Passed  
✅ Automated tests executed successfully  

---

# 📚 What I Learned

Through this project, I gained hands-on experience with:

- Continuous Integration and Continuous Deployment concepts.
- GitHub Actions workflow creation.
- YAML configuration for automation pipelines.
- Integrating automated testing into CI/CD environments.
- Managing QA automation projects using Git and GitHub.
- Applying industry practices used by QA Automation Engineers.

---

# 🌟 Portfolio Value

This project demonstrates my ability to:

- Build automation workflows.
- Integrate testing into development pipelines.
- Work with modern QA automation tools.
- Understand the relationship between testing and software delivery processes.

It complements my other QA Automation projects:

- 🎭 Playwright Enterprise Framework
- 📬 API Testing with Postman
- ⚡ Performance Testing with k6
- 📱 Mobile Automation with Appium *(in progress)*

---

# 👩‍💻 Author

**Ana Centeno**

QA Automation Engineer | Data Analyst | BI Developer

---

## 🔗 Links

GitHub:  
https://github.com/AnaCenteno-DA

LinkedIn:  
https://www.linkedin.com/in/ana-centeno-tech/
