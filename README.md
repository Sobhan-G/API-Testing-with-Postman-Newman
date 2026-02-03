# API Testing with Postman & Newman

![API Tests Status](https://github.com/Sobhan-G/API-Testing-with-Postman-Newman/actions/workflows/main.yml/badge.svg)

This project contains a suite of automated API tests. Originally built for ReqRes, it now uses **JSONPlaceholder** to demonstrate a robust CI/CD pipeline. The tests are created in Postman and automated via Newman and GitHub Actions.

## 🎯 Purpose
To demonstrate proficiency in API testing, error handling, and automation within the QA field. This project showcases a full CI/CD workflow where tests are automatically executed upon every code push.

## 🚀 Features
✅ **Automated CI/CD:** Integrated with GitHub Actions for continuous testing.
✅ **Login Validation:** Simulates successful and failed authentication flows.
✅ **User Management:** Fetching user lists and validating data structures.
✅ **Resource CRUD:** Creating and deleting resources with status code verification.
✅ **Stability:** Optimized assertions to handle dynamic API responses.

## 🧰 Tools Used
* **Postman:** Test development and script authoring.
* **Newman:** CLI-based test execution.
* **GitHub Actions:** Automated workflow and CI/CD integration.
* **JavaScript:** Assertion logic (Post-response scripts).
* **JSONPlaceholder:** The REST API used for stable test execution.

## 📦 Project Structure
```text
API-Testing-with-Postman-Newman/
├── .github/workflows/
│   └── main.yml           # GitHub Actions configuration
├── README.md              # Project documentation
└── QA Demo.postman_collection.json  # The main test suite

🛠️ Getting Started
1. Clone the project
Bash
git clone [https://github.com/Sobhan-G/API-Testing-with-Postman-Newman.git](https://github.com/Sobhan-G/API-Testing-with-Postman-Newman.git)
cd API-Testing-with-Postman-Newman

2. Install Newman
Bash
npm install -g newman

3. Run the test suite manually
Bash

Test Name,Endpoint,Description
Login - Success,POST /posts,Verifies successful resource creation (Status 201).
Login - Fail,POST /invalid,Validates error handling (Status 404).
Get Users,GET /users,Ensures user array is retrieved correctly (Status 200).
Create User,POST /users,Validates new user object creation.
Delete User,DELETE /users/1,Confirms successful resource removal.
newman run "QA Demo.postman_collection.json" -r cli

📚 Key Learnings
CI/CD Implementation: Successfully automated the testing lifecycle using GitHub Actions.

Environment Adaptation: Demonstrated ability to pivot and reconfigure tests for different API environments.

Problem Solving: Debugged "undefined" assertions and status code mismatches in a cloud-based runner.
