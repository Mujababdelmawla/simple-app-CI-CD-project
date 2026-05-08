# DevOps CI/CD Demo — GitHub Actions (JS + Python + Load Test)

This repository demonstrates a complete multi-language CI/CD pipeline using GitHub Actions, including:

- JavaScript Unit Tests (Jest)
- Code Coverage Reporting
- Static Website Deployment to GitHub Pages
- Python-based Monitoring Script
- k6 Load Testing
- Student Participation (Real-Time Traffic Observation)

---

# Project Structure

```bash
my-cicd-demo/
├── index.html
├── sum.js
├── sum.test.js
├── monitor.py
├── loadtest.js
├── package.json
├── requirements.txt
└── .github/
    └── workflows/
        └── deploy.yml
```

---

# Setup Instructions

## 1. Enable GitHub Pages

After creating the repository:

- Go to **Repository Settings**
- Navigate to **Pages**
- Under **Source**, choose:

```text
GitHub Actions
```

This allows your workflow to deploy automatically.

---

## 2. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

---

## 3. Install Dependencies

### Node.js Dependencies

```bash
npm install
```

### Python Dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Make Changes

Modify files as needed:

- `index.html`
- `sum.js`
- `sum.test.js`
- `monitor.py`
- `loadtest.js`

Then commit and push:

```bash
git add .
git commit -m "Updated project"
git push origin main
```

---



---

# CI Pipeline — Tests + Coverage

The CI workflow runs automatically on every push.

## Features

- Executes Jest unit tests
- Generates coverage reports
- Uploads coverage reports as GitHub artifacts

---

# CD Pipeline — Deployment

After successful tests, the workflow automatically deploys the static website to GitHub Pages.

## Example URL

```text
https://USERNAME.github.io/REPOSITORY/
```

---

# Monitoring with Python

After deployment, a Python monitoring script checks:

- Response latency
- HTTP status code
- Content size
- Timestamp

The results are stored in:

```bash
metrics.json
```

You can download the generated artifact from GitHub Actions.

---

# Load Testing with k6

A lightweight load test runs automatically against the deployed website.

## Test Configuration

- 20 virtual users
- 20 seconds duration
- Targets the live GitHub Pages site

---

# Technologies Used

- GitHub Actions
- GitHub Pages
- Jest (Testing + Coverage)
- Python (Monitoring)
- k6 (Load Testing)

---

# Workflow Summary

```bash
Push Code
   ↓
Run Jest Tests
   ↓
Generate Coverage
   ↓
Deploy to GitHub Pages
   ↓
Run Monitoring Script
   ↓
Execute k6 Load Test
```

---

# Learning Outcomes

This project helps demonstrate:

- CI/CD fundamentals
- Automated testing pipelines
- Static site deployment
- Monitoring and observability
- Performance/load testing
- Multi-language workflow integration

---

# Author

Mujab Yousef : Developed as a DevOps CI/CD demonstration project using GitHub Actions.