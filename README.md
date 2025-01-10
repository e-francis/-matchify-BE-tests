# Machify API Test Documentation

## Overview

Automated API tests for **Profile Creation** and **Login** endpoints using **Postman**, **Newman**, and **HTML Extra Reporting**.

## Test Reports Location

- **GitHub Actions Artifacts**:
  - `api-test-reports/profile-test-report.html`: Profile creation test results
  - `api-test-reports/auth-test-report.html`: Login test results
  - `updated-environment/updated-env.json`: Exported environment variables from tests

## Accessing Reports

1. **GitHub Actions**:
   - Navigate to the **Actions** tab in the repository.
   - Select the relevant workflow run.
   - Download the test reports from the **Artifacts** section.

## Report Features

- Test execution summary
- Failed test details with response validation
- Environment details
- Interactive HTML reports with enhanced visuals

## CI/CD Pipeline

Automated test execution and reporting occur on:

- **Push** to the `main` branch
- **Pull requests** to the `main` branch

## Test Coverage

### Profile API Tests (`Profile.postman_collection.json`)

- **Positive Tests:**

  - Successful Profile Creation

- **Negative Tests:**

  - Empty Request Body
  - Missing Required Fields
  - Invalid Passcode
  - Invalid Picture Upload
  - More than 5 Interests
  - Invalid Gender Value
  - Future Date of Birth (DOB)
  - Invalid Email Format
  - Invalid Date Format
  - Underage Registration

### Auth API Tests (`AUTH.postman_collection.json`)

- **Valid Login Tests:**

  - Successful Login

- **Negative Login Tests:**

  - First Failed Login Attempt Before Attempt Reset
  - Reset After Successful Attempt
  - First Failed Attempt
  - Second Failed Attempt
  - Third Failed Attempt
  - Account Locked
  - Login with Non-existent Account
  - Empty Request Body
  - Empty Request Body Variables
  - Empty Request Body Passcode Variable
  - Empty Request Body Email Variable


## CI/CD Workflow Overview

1. **Install Dependencies:** Newman and the HTML Extra reporter are installed.
2. **Run Profile API Tests:** Executes profile tests and exports dynamic environment variables.
3. **Run Auth API Tests:** Uses updated environment variables for login tests.
4. **Upload Reports:** Test reports and updated environment files are uploaded as GitHub Action artifacts.

---

This workflow ensures consistent and automated API testing with dynamic data handling across Profile and Auth endpoints.

