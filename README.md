# QA Automation Orchestrator

## Overview

The **QA Automation Orchestrator** is the central repository responsible for coordinating the execution of automated testing workflows across multiple repositories using **GitHub Actions Reusable Workflows**.

This project does not contain test scripts. Instead, it acts as an orchestration layer that triggers remote workflows for different testing frameworks, keeping each implementation isolated and independently maintainable.

---

## Architecture

```text
                    QA Automation Orchestrator
                               │
          ┌────────────────────┴────────────────────┐
          │                                         │
          ▼                                         ▼
     Playwright Repository                 k6 Repository
 Functional UI Testing               Performance Testing
          │                                         │
          ▼                                         ▼
      GitHub Actions                         GitHub Actions
```

---

## Project Structure

```text
QA_Automation_Orchestrator
│
├── .github
│   └── workflows
│       ├── playwright.yml
│       └── k6.yml
│
└── README.md
```

---

## Features

- Centralized execution of automated testing workflows.
- Reusable GitHub Actions workflows.
- Separation of concerns between functional and performance testing.
- Independent repositories for each testing framework.
- Scalable architecture for adding additional testing frameworks.

---

## Remote Repositories

### Playwright Repository

Responsible for executing functional UI automation tests using Playwright.

### k6 Repository

Responsible for executing performance and load tests using k6.

---

## Workflow Execution

The orchestrator repository contains two independent workflows:

### Playwright Workflow

- Triggers the reusable workflow hosted in the Playwright repository.
- Executes functional UI tests remotely.

### k6 Workflow

- Triggers the reusable workflow hosted in the k6 repository.
- Executes performance testing remotely.

This architecture allows each testing framework to evolve independently while providing a single entry point for automated quality assurance execution.

---

## Technologies

- GitHub Actions
- GitHub Reusable Workflows
- Playwright
- k6
- YAML
- CI/CD

---

## Benefits

- Modular architecture
- Easy maintenance
- Reusable pipelines
- Centralized orchestration
- Better scalability
- Improved DevOps practices

---

## Future Improvements

- Execute Playwright and k6 workflows in parallel.
- Add workflow status notifications.
- Generate consolidated test reports.
- Integrate code coverage metrics.
- Add scheduled workflow execution.
- Support additional testing frameworks.

---

## Author

**Ana Centeno**

QA Automation | Performance Testing | Data Analytics
