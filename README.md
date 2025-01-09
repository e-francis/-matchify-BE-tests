# API Test Documentation

## Overview
Automated API tests for Profile Creation and Login endpoints using Postman, Newman, and Allure reporting.

## Test Reports Location
- **GitHub Actions Artifacts**: 
 - `test-reports/allure-report/`: Allure test reports
 - `test-reports/profile-report.html`: Profile creation test results
 - `test-reports/login-report.html`: Login test results

- **GitHub Pages**:
 - Allure reports automatically deployed to: `https://{username}.github.io/{repo-name}`

## Accessing Reports
1. **GitHub Actions**:
  - Go to Actions tab
  - Select workflow run
  - Download artifacts from "Artifacts" section

2. **GitHub Pages**:
  - Access published Allure report via GitHub Pages URL
  - Report updates on every workflow run

## Report Features
- Test execution summary
- Failed test details
- Response validations
- Environment details
- Timeline view
- Trends analysis

## CI/CD Pipeline
Automated test execution and reporting on:
- Push to main
- Pull requests
- Manual workflow dispatch

## Environment Setup
Required secrets in GitHub:
```json
{
 "POSTMAN_API_URL": "API base URL",
 "TEST_EMAIL": "Test email",
 "TEST_PASSCODE": "Test passcode",
 "GITHUB_TOKEN": "For GitHub Pages deployment"
}
